# Federation Credit Burn Formula: Technical Standard

This document defines the mathematical specification for the progressive burn formula used in the annual federation credit reconciliation. It is a federation-level technical standard referenced by Governance Article 6 (Economy). It may be amended only through federation-level governance. All Societies are bound by the version in effect at the time of each annual reconciliation.

---

## Symbol Definitions

| Symbol | Meaning |
|--------|---------|
| N | Total number of Societies participating in the federation |
| i | Index for a specific Society (i = 1 to N) |
| H_i | Total federation credits held by Society i: the sum of its federation treasury balance and all individual member balances on its ledger segment. Credits committed to pending unsettled transactions are included. |
| T | Total federation credits outstanding across all Societies: T = Σ H_i |
| D | Desired supply: D = 60,000 × total federation members |
| B | Required burn: B = T − D (only calculated when T > D; when T ≤ D, no burn occurs and the federation mints the difference D − T instead) |
| r | Pressure ratio: r = B / D |
| α | Progressivity exponent (calculated per reconciliation; see below) |
| α_max | Maximum progressivity parameter (federation policy; current value defined in Section 5) |
| obligation_i | Burn obligation assigned to Society i |
| rate_i | Burn rate for Society i: the fraction of H_i that Society i must burn |

---

## 1. Determining Whether a Burn Is Required

At each annual reconciliation:

1. Calculate D = 60,000 × (total members across all Societies on the reconciliation date)
2. Calculate T = Σ H_i across all Societies
3. If T ≤ D: no burn. The federation mints (D − T) credits and distributes them to Societies proportional to their current membership. Reconciliation is complete.
4. If T > D: a burn is required. Set B = T − D and proceed to Section 2.

---

## 2. Calculating the Progressivity Exponent

The exponent α scales with the pressure ratio r, so that mild excess produces a gentle distribution and large excess produces a steeply progressive one.

**r = B / D**

**α = 1 + r × (α_max − 1)**

When r = 0: α = 1 (flat distribution — all Societies burn the same percentage)
When r = 1: α = α_max (maximum progressivity)
When r > 1: α is capped at α_max (the formula does not become more progressive beyond this point regardless of excess magnitude)

Therefore: **α = 1 + min(r, 1) × (α_max − 1)**

---

## 3. Calculating Burn Obligations

Each Society's burn obligation is:

**obligation_i = B × H_i^α / Σ(H_j^α)**

where the sum in the denominator is taken over all N Societies (j = 1 to N).

The burn rate for Society i — the fraction of its holdings it must burn — is:

**rate_i = obligation_i / H_i = B × H_i^(α−1) / Σ(H_j^α)**

Properties of this formula:
- Obligations sum to B exactly: Σ obligation_i = B × Σ(H_i^α) / Σ(H_j^α) = B ✓
- The poorest Society (smallest H_i) has the smallest obligation, approaching zero as H_i approaches zero ✓
- The wealthiest Society (largest H_i) has the largest rate and the largest obligation ✓
- No Society's obligation exceeds its holdings (see Section 4) ✓

---

## 4. No-Insolvency Guarantee

**Claim:** For all i, obligation_i ≤ H_i.

**Proof:**

obligation_i = B × H_i^α / Σ(H_j^α)

For this to exceed H_i:
B × H_i^α / Σ(H_j^α) > H_i
B × H_i^(α−1) > Σ(H_j^α) / H_i^? ...

More directly: obligation_i ≤ H_i requires B ≤ Σ(H_j^α) / H_i^(α−1).

Since Σ(H_j^α) ≥ H_i^α (the sum includes the H_i^α term itself):
Σ(H_j^α) / H_i^(α−1) ≥ H_i^α / H_i^(α−1) = H_i

Therefore obligation_i ≤ B is required. Since B ≤ T = Σ H_j and obligation_i is a fraction of B, it remains to confirm obligation_i ≤ H_i.

The binding constraint is on the wealthiest Society. Let H_max = max(H_i). Then:

obligation_max = B × H_max^α / Σ(H_j^α) ≤ B × H_max^α / H_max^α = B ≤ T

Since H_max ≤ T (one Society cannot hold more than all credits), and B ≤ T:

obligation_max = B × H_max^α / Σ(H_j^α)

Because Σ(H_j^α) ≥ H_max^(α−1) × T (by the power mean inequality for α ≥ 1):

obligation_max ≤ B × H_max^α / (H_max^(α−1) × T) = B × H_max / T ≤ H_max

Therefore obligation_max ≤ H_max, and by the same argument, obligation_i ≤ H_i for all i. No Society can be made insolvent. □

---

## 5. Federation Policy Parameter

**α_max = 3**

This value produces strong progressivity at maximum pressure: a Society with twice the holdings of another bears approximately four times the burn obligation (since 2^(3−1) = 4). A Society with ten times the holdings bears approximately one hundred times the obligation.

α_max may be adjusted by federation-level governance. Increasing α_max increases progressivity at high pressure; decreasing it toward 1 flattens the distribution. α_max must be greater than 1; a value of 1 would make the formula flat regardless of pressure.

---

## 6. Worked Example

**Setup:**
- 3 Societies: A, B, C
- Total federation members: 100
- D = 60,000 × 100 = 6,000,000
- Holdings: H_A = 500,000 | H_B = 1,500,000 | H_C = 4,200,000
- T = 6,200,000
- B = T − D = 200,000
- r = 200,000 / 6,000,000 ≈ 0.033
- α = 1 + min(0.033, 1) × (3 − 1) = 1 + 0.033 × 2 ≈ 1.067

**Weighted holdings (H_i^α):**
- H_A^1.067 = 500,000^1.067 ≈ 763,000
- H_B^1.067 = 1,500,000^1.067 ≈ 2,483,000
- H_C^1.067 = 4,200,000^1.067 ≈ 7,269,000
- Σ = 10,515,000

**Obligations:**
- obligation_A = 200,000 × 763,000 / 10,515,000 ≈ 14,500 (rate ≈ 2.9% of holdings)
- obligation_B = 200,000 × 2,483,000 / 10,515,000 ≈ 47,200 (rate ≈ 3.1% of holdings)
- obligation_C = 200,000 × 7,269,000 / 10,515,000 ≈ 138,300 (rate ≈ 3.3% of holdings)
- Total ≈ 200,000 ✓

*Note: with low pressure (r ≈ 0.033), α is close to 1 and the distribution is nearly flat — rates are 2.9%, 3.1%, and 3.3%. The progressivity becomes much steeper as excess grows.*

**High-pressure example (same Societies, B = 3,000,000):**
- r = 3,000,000 / 6,000,000 = 0.5
- α = 1 + 0.5 × 2 = 2.0

Weighted holdings (H_i^2):
- H_A^2 = 2.5 × 10^11
- H_B^2 = 2.25 × 10^12
- H_C^2 = 1.764 × 10^13
- Σ ≈ 2.039 × 10^13

Obligations:
- obligation_A = 3,000,000 × (2.5×10^11 / 2.039×10^13) ≈ 36,800 (rate ≈ 7.4%)
- obligation_B = 3,000,000 × (2.25×10^12 / 2.039×10^13) ≈ 331,000 (rate ≈ 22.1%)
- obligation_C = 3,000,000 × (1.764×10^13 / 2.039×10^13) ≈ 2,595,000 (rate ≈ 61.8%)
- Total = 3,000,000 ✓ (rounding aside)

At higher pressure, Society C (wealthiest) bears 86.5% of the total burn while Society A bears only 1.2%.

---

## 7. Edge Cases

**Only one Society in the federation:**
N = 1. obligation_1 = B × H_1^α / H_1^α = B. The single Society bears the full burn. Since B ≤ T = H_1, the no-insolvency guarantee holds.

**A Society holds zero credits (H_i = 0):**
H_i^α = 0 for all α > 0. obligation_i = 0. The Society burns nothing.

**All Societies hold equal credits (H_i = T/N for all i):**
All H_i^α are equal, so all obligations are equal: obligation_i = B/N. The distribution is flat regardless of α — when all Societies are equally wealthy, progressivity has nothing to act on.

**Very large α_max:**
As α_max increases, at high pressure the entire burden concentrates on the single wealthiest Society. The no-insolvency guarantee still holds because obligation_max ≤ H_max (proven in Section 4). However, very high α_max values may be politically destabilizing and should be chosen with care.

---

## 8. Verification

Any Society, member, or observer may verify the burn distribution for any reconciliation as follows:

1. Collect each Society's publicly published total holdings (H_i) from their public records
2. Sum all holdings to obtain T
3. Obtain D from the federation's published member count: D = 60,000 × total members
4. If T > D: B = T − D; r = B / D; α = 1 + min(r, 1) × (α_max − 1)
5. For each Society i: compute H_i^α
6. Sum all H_i^α to obtain the denominator
7. Each Society's obligation = B × H_i^α / Σ(H_j^α)

No information beyond publicly available figures and this standard is required to verify any burn distribution. Any discrepancy between a published burn distribution and the formula output should be reported to the federation's dispute resolution process.
