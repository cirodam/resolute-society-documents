# Ledger Division — Master Plan

## Mission

The Ledger Division exists to maintain accurate, complete, and publicly accessible records of the Society's two credit systems — the society credit ledger and the federation credit ledger segment — and to serve as the Society's designated point of contact for all inter-society ledger coordination.

The division is a steward of the record, not a governor of the economy. Every economic decision — what the treasury spends, whether an allowance is established, how demurrage is set — belongs to the membership through normal democratic processes. The Ledger Division's role is to ensure that those decisions are accurately recorded, that the records are visible to every member, and that any Society reaching out to settle a transaction or resolve a discrepancy has a known counterpart to contact.

Accurate records are not administrative paperwork. They are the substrate on which the Society's internal economy functions. A member who does not trust that their balance is accurately recorded will not participate in the credit economy. A Society whose ledger cannot be audited by other Societies cannot participate honestly in the federation. The Ledger Division's work is foundational to both.

## Mandate

The division is responsible for four things:

- That the society credit ledger is accurate, complete, and accessible to all members at all times
- That the federation credit ledger segment is accurate, complete, and published to federation standards on the required schedule
- That the Society has a functioning, reachable point of contact for inter-society transaction settlement, reconciliation, and ledger disputes
- That disputes about the accuracy of recorded balances are resolved reliably, with clear appeal to the membership

## Core Functions

- **Society Credit Ledger Maintenance** — recording all minting and burning events, demurrage charges, allowance distributions, member-to-member transactions, and treasury movements in the society credit system
- **Federation Credit Ledger Segment Maintenance** — recording all federation credit entries in which this Society is a party: inter-society transactions, intra-society federation credit use, treasury movements, and annual reconciliation adjustments
- **Public Record Publication** — publishing the required summaries of both credit systems on the schedules defined in the Economy governance document
- **Inter-Society Transaction Settlement** — coordinating with counterpart Ledger Divisions in other Societies to settle inter-society federation credit transactions and resolve discrepancies between ledger segments
- **Annual Reconciliation Participation** — contributing this Society's ledger figures to the federation's annual reconciliation process and executing the Society's assigned burn or receiving its assigned mint
- **Dispute Resolution** — resolving disputes about the accuracy of recorded balances within the Society, and escalating inter-society ledger disputes to the federation's dispute resolution process

---

## Society Credit Ledger

The society credit ledger is the authoritative record of the Society's internal economy. It records every event that changes a credit balance — every entry is permanent and traceable to its source.

**What the ledger records:**

- **Member balances** — the current credit balance of every member in good standing, updated in real time as transactions occur
- **Treasury balance** — the current balance of the Society's credit treasury
- **Minting events** — the issuance of sixty thousand credits upon each new member's admission, recorded as a treasury credit
- **Burning events** — the retirement of credits upon member departure, recorded as a debit against the individual balance and, where shortfall collection is required, against remaining member balances proportionally
- **Demurrage charges** — the monthly holding cost applied to all individual member balances at the close of each month, recorded individually per member and in aggregate to the treasury
- **Allowance distributions** — monthly credits from the treasury to each member's individual balance, if an allowance is established, recorded per member
- **Member-to-member transactions** — credits transferred between individual members in exchange for goods, labor, or services, recorded as a debit against the sender and a credit to the receiver
- **Treasury disbursements** — credits paid from the treasury for labor, goods, services, or authorized expenditure, recorded as a treasury debit and a credit to the receiving member

**Balance integrity:** The total of the treasury balance plus all individual member balances must equal sixty thousand times current membership at all times. Any discrepancy is an error requiring immediate investigation and correction. The Ledger Division should verify this aggregate relationship at regular intervals and after every batch of events — departure processing, monthly demurrage — that touches multiple balances simultaneously.

**Balance ceiling enforcement:** No individual member balance may exceed sixty thousand credits. Any transaction or distribution that would cause a balance to exceed this ceiling is split: the amount that would bring the balance to sixty thousand is credited to the member, and the remainder is redirected to the treasury. The ledger records both entries.

**Departure processing:** Member departure triggers a specific sequence of ledger events that must be executed in the correct order and recorded completely. The Ledger Division executes departure processing and notifies all affected members of any departure demurrage charge applied to their balances before the charge is applied.

## Federation Credit Ledger Segment

The Society's federation credit ledger segment is its portion of the federation's distributed ledger. It contains every federation credit entry in which this Society is a party. No Society's segment is authoritative for entries outside its own participation — but every Society is fully authoritative for the entries on its own segment.

**What the segment records:**

- **Federation treasury balance** — the current balance of the Society's unallocated federation credits
- **Individual member balances** — federation credits held by individual members, if the Society distributes federation credits to member accounts
- **Total federation credits outstanding** — the net sum of all federation credit entries on this segment: federation treasury balance plus individual member balances plus any credits committed to pending unsettled transactions
- **Incoming transactions** — federation credits received from another Society, recorded as a credit to this Society's federation treasury or designated account
- **Outgoing transactions** — federation credits sent to another Society, recorded as a debit against this Society's federation treasury or designated account
- **Pending transactions** — transactions initiated but not yet settled, held in a pending state until both legs are confirmed; credits committed to pending transactions are included in total outstanding
- **Intra-society federation credit use** — federation credit transactions between members within this Society, recorded entirely on this segment with both legs
- **Annual reconciliation adjustments** — the burn obligation or mint distribution assigned to this Society at each reconciliation, recorded as a debit (burn) or credit (mint) against the segment

**Transaction settlement:** Every inter-society federation credit transaction has two legs: an outgoing entry on the sending Society's segment and an incoming entry on the receiving Society's segment. A transaction is not complete until both Ledger Divisions have confirmed their respective entries. The Ledger Division initiates outgoing transactions, acknowledges incoming transactions from other Societies, and marks transactions complete only when both legs are confirmed. Discrepancies — where one Society's segment records an entry that the other's does not — are escalated to the federation's dispute resolution process.

**Pending transaction management:** Credits committed to unsettled outgoing transactions are held in a pending state and included in total outstanding. They may not be spent again until the transaction settles or is voided. The Ledger Division monitors open pending transactions and follows up with counterpart Ledger Divisions to ensure timely settlement.

## Public Record Publication

The Ledger Division publishes two sets of records on distinct schedules. Both are non-negotiable governance obligations.

**Society credit records — published quarterly:**

- Total credit supply outstanding (must equal 60,000 × current membership)
- Treasury balance
- Total individual balances outstanding
- Monthly demurrage collected (for each month in the quarter)
- Allowance distributed (for each month in the quarter, if applicable)

These figures are published to all members. No member's individual balance may be concealed from the membership. The division maintains and makes accessible the full member balance ledger, not just the aggregate summary.

**Federation credit records — published weekly:**

- Total federation credits outstanding: the net sum of all federation credit entries on the Society's segment, including federation treasury balance, individual member balances, and credits committed to pending transactions
- Credits currently in account: the balance held in the Society's federation treasury alone, not including individual member balances or pending transactions

These two figures are the inputs any other Society or observer needs to apply the federation's progressive burn formula and calculate this Society's theoretical reconciliation obligation at any moment. They are published for the federation as a whole, not only for the Society's own membership. A Society that fails to publish current figures, or that publishes figures that do not reconcile with its segment upon inspection, is in breach of federation standards.

The Ledger Division is responsible for publishing both. Publication means making the figures accessible to any member, any other Society's Ledger Division, or any federation observer who requests them — not merely filing them internally.

## Inter-Society Coordination

The Ledger Division is this Society's sole designated point of contact for all inter-society ledger matters. Other Societies direct all federation credit transaction requests, settlement confirmations, reconciliation coordination, and dispute notifications to the Ledger Division. The division must be reachable by any other Society's Ledger Division without requiring that Society to navigate the Society's internal structure.

**Incoming transaction requests:** When another Society initiates a federation credit transaction to this Society, their Ledger Division contacts this division to confirm the incoming leg. The Ledger Division verifies the transaction details, records the incoming entry, and confirms settlement to the sending Society.

**Outgoing transaction initiation:** When this Society sends federation credits to another Society, the Ledger Division records the outgoing entry as pending, contacts the receiving Society's Ledger Division, and awaits their confirmation of the incoming leg before marking the transaction complete.

**Discrepancy resolution:** When a ledger discrepancy arises — an entry recorded on one Society's segment but not the other's, or two segments recording different amounts — the two Ledger Divisions work together to identify the source. If the two divisions cannot resolve the discrepancy directly, it is escalated to the federation's dispute resolution process. Neither Society's record is presumed correct.

**Reconciliation coordination:** The annual reconciliation requires each Society to contribute its total holdings figure to the federation's calculation and to execute its assigned burn or accept its assigned mint. The Ledger Division submits this Society's figures, confirms the reconciliation output, and executes the corresponding ledger adjustments on this Society's segment.

## Dispute Resolution

**Internal disputes — society credit ledger:** A member who believes their recorded balance is incorrect brings the dispute to the Ledger Division. The division examines the ledger history for the member's account, identifies the source of the discrepancy, and corrects it if an error is found. Corrections are recorded as adjustment entries with a notation of the source error. If the division finds no error and the member disputes the finding, the matter is appealed to the membership through the Society's normal governance process.

**Internal disputes — federation credit segment:** A member who believes their recorded federation credit balance is incorrect follows the same process.

**Inter-society disputes:** Disputes between Societies about the validity of a transaction are not resolved by either Ledger Division alone. The dispute is escalated to the federation's dispute resolution process, which examines both segments and the underlying transaction record. The Ledger Division's role in this process is to produce the relevant segment entries completely and accurately and to cooperate with the process. Neither Society's record is presumed correct going in.

## Division Relationships

**Membership and Governance**
The Ledger Division serves the membership. Treasury expenditure decisions, allowance levels, and demurrage rates are set through democratic governance — the division records the outcomes of those decisions, not the decisions themselves. The division should provide any credit economy figures the membership needs to make informed decisions, and should flag any governance outcome that cannot be legally recorded under the Economy governance document.

**Other Societies' Ledger Divisions**
The division's primary external relationship is with counterpart Ledger Divisions across the federation. These relationships should be established and maintained before they are urgently needed. Knowing who to contact at each Society's Ledger Division, and having an established communication channel, is necessary for timely transaction settlement and discrepancy resolution.

**Federation Dispute Resolution**
The Ledger Division is the Society's representative in any federation-level ledger dispute. It is responsible for producing complete and accurate segment records when requested and for cooperating fully with the federation process.

## Operational Posture

The Ledger Division operates continuously. The ledger does not close between governance cycles. Transactions occur, balances change, and the record must reflect current reality at all times.

Monthly obligations — demurrage collection, allowance distribution if established — are time-sensitive and must be executed and recorded at the close of each month without delay. The weekly publication of federation credit figures must go out on schedule regardless of other division activity.

The annual reconciliation is the division's most complex single event. Preparation begins before the reconciliation date: verifying the segment is complete and current, computing total holdings, and confirming the publication of required figures. The division should treat reconciliation as a planned event requiring preparation, not a reactive obligation.

## Establishment Priorities

**1. Build the ledger from the first member**
The ledger must exist before the first credit transaction. The division's first task is establishing its record-keeping system — whatever form it takes — and recording the initial minting event upon the Society's first membership admission. Beginning with accurate records from day one is far easier than reconstructing records after the fact.

**2. Establish inter-society contact relationships**
As the federation grows, the division registers itself as the Society's Ledger Division contact with the federation and establishes direct communication with counterpart Ledger Divisions in other Societies. These relationships should be established before any inter-society transaction is needed.

**3. Begin weekly federation credit publication**
The weekly publication obligation begins when the Society joins the federation. The division establishes its publication process early and maintains the schedule consistently — a Society that publishes irregularly or on request rather than on schedule is not meeting federation standards.

**4. Establish member-facing balance access**
Every member must be able to see their own balance and the treasury balance at any time. The division establishes how members access this information — a posted ledger, a shared record, a designated time and place — and maintains it consistently.

## Division Documents

The Ledger Division is responsible for producing and maintaining the following documents.

**Society Credit Ledger** — the complete and current record of all society credit balances and events. Accessible to all members at all times.

**Federation Credit Ledger Segment** — the complete and current record of all federation credit entries in which this Society is a party. The authoritative record for all inter-society coordination and reconciliation.

**Quarterly Society Credit Summary** — the published summary of the society credit economy for each quarter: total supply, treasury balance, total individual balances, demurrage collected, and allowance distributed.

**Weekly Federation Credit Publication** — the two published figures required by federation standards: total federation credits outstanding and credits currently in the federation treasury account.

**Transaction Record** — a log of every inter-society federation credit transaction: date, counterpart Society, amount, status (pending or settled), and confirmation from both ledger segments. The working record for settlement coordination and discrepancy identification.

**Reconciliation Record** — documentation of each annual reconciliation: the figures submitted, the reconciliation output received, and the adjustments executed on the segment. Retained permanently.
