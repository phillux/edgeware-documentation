# Treasury

Edgeware uses a treasury mechanism to achieve self-sustainability and permit creative incentivization of all stakeholders in the ecosystem, including core and dapp development, ecosystem support and much more. 

These funds can be deployed through a Treasury Spend action which is subject to council approval but can be proposed by any EDG holder. 

{% hint style="info" %}
Substrate Documentation for the Treasury Module is found at [https://substrate.dev/rustdocs/master/pallet\_treasury/index.html](https://substrate.dev/rustdocs/master/pallet_treasury/index.html)
{% endhint %}

## EDG Accrual to the Treasury

The treasury obtains funds in several ways that mimic governments - minting, fees and taxes.

1. **Minting:** A portion of the EDG produced with each block goes to the treasury.
2. **Slashing:** When a validator is slashed for any reason, the slashed amount is sent to the Treasury. Slashed EDG may also accrue to the treasury through failed governance proposals.
3. **Transaction fees**: A portion of each block's transaction fees goes to the Treasury, with the remainder going to the block author.
4. **Staking inefficiency:** [Inflation](https://wiki.polkadot.network/docs/en/learn-staking#inflation) is designed to be ~20% in the first year, and the ideal staking ratio is set at 80%, meaning 80% of all tokens should be locked in staking. Any deviation from this ratio will cause a proportional amount of the inflation to go to the Treasury. In other words, if 80% of all tokens are staked, then 100% of the inflation goes to the validators as reward. If the staking rate is greater than or less than 80%, then the validators will receive less, with the remainder going to the Treasury.
5. **Lost Deposits:** These may be abandoned bonds from voting, proposals or otherwise.

{% hint style="info" %}
**Parameter Note:** The _ideal staking ratio_ used in the Edgeware economic model is currently 80%.  _Inflation_ is currently set to about 20%, or 158 EDG per block.
{% endhint %}

\*\*\*\*

## Conducting a Treasury Spend Proposal

Once you have an idea that might be appropriate for funding from the Edgeware Treasury, you can complete several steps to test the public interest, convey your argument, and then submit your formal treasury proposal.  This guide is written as a recommendation both to proposers and decision-makers, and will track best practices over time as they emerge.  

Similar to [traditional RFP](https://en.wikipedia.org/wiki/Request_for_proposal)s \(request for proposals\) that governments use to solicit bids for work, treasury spends optimize the productive value of the EDG and seek to extract maximum work for their recipients. Proposers should be prepared to defend their position or experience competitive bids for the same or similar work. 

### Technical Process of a Treasury Spend

1. Pre-Proposal Stage - Planning, writing, advocacy, outreach, discussion.
2. Treasury Spend Proposed On-chain
3. Council either adopts or refuses the proposal.
4. If approved, it enters a queue within a budget period of 24 days. 
   1. The treasury attempts to fulfill as many spends in the queue within this time period.
   2. At the end of a budget period, the remaining treasury balance is subject to a small percentage burn. This incentivizes the usage of funds and creates deflation through the destruction of EDG.
5. If refused, the treasury proposal remains able to be accepted until the end of the 24 day period, then it is removed from the consideration table but can be resubmitted.

### Plausible Project Concepts 

Projects that serve the broader Edgeware ecosystem are much more likely to succeed than other kinds of efforts. 

* **Open source** projects; some closed source may be successful depending on the case.
* Tooling and Developer experience
* User Experience, wallets, DEXs, clients
* Infrastructure
* Monitoring, auditing, security operations
* Cross-chain collaborations
* Events, meetups, hackathons
* Primitive Development
* Bridges and Interoperability
* Governance Improvements
* Cryptography
* Core Development
* Identity projects
* Smart Contract resources
* Validation resources
* Brand and marketing campaigns
* Community organization efforts

This list is not exhaustive, but it gives you a sense of what sorts of things are good propositions.

### Proposal Description Document

The first step is to describe the proposal in full to the community.  A great place to start is a single document that contains all the following information. Once the document is ready, create the on-chain spend in the next step, then share the document after.

{% hint style="info" %}
Proposals are best understood when they focus on one main project or goal at a time. Multi-goal proposals should be segmented into milestones with payment segmented accordingly.
{% endhint %}

1. Date of Proposal
2. Who is proposing? 
   1. What is their motivation?
   2. Do they have any conflicts of interest?
   3. To who do these payments go?
      1. For building, who will be handling what? 
      2. What is their background and expertise? Describe the whole team.
3. What is the historical context of this proposal?
   1. What previous actions does this proposal relate to?
   2. Does it have any impacts on future actions to note?
4. Clear, short Problem Statement and Proposed Solution 
   1. Evidence for that Solution 
   2. Who does this solution help?
5. Describe, if relevant, the Milestone Structure of goals and disbursements.
6. Financial Details for all Proposed Transfers
   1. Amount/s requested
   2. Financial timeline  - when are installments due?
   3. What are the Addresses of the fund recipients?
   4. Who will be managing the funds, how can we contact them?
   5. How will the manager of the funds report on status proactively? Where we can follow progress and ask questions?
7. License \(if applicable\)



### Propose The Spend On-Chain

To propose a treasury spend, **a deposit totaling 5% of the proposed spend amount, with a minimum of 1000 EDG is required.This deposit will be slashed if the proposal is rejected,** and returned if the proposal was accepted.

One way to create the proposal is to use the Polkadot JS Apps [website](https://polkadot.js.org/apps). From the website, use either the [extrinsics tab](https://polkadot.js.org/apps/#/extrinsics) and select the Treasury pallet, then `proposeSpend` and enter the desired amount and recipient, **or** use the [Treasury tab](https://polkadot.js.org/apps/#/treasury) and its dedicated Submit Proposal button:

![](../../.gitbook/assets/image%20%289%29.png)

The system will automatically take the required deposit, picking the **higher** of the following two values: 1000 EDG or 5% of the requested amount. If the user cannot pay the deposit, an error will be returned and the proposal creation will fail.

![A proposal ready for the council to consider](../../.gitbook/assets/image%20%288%29.png)

Once created, your proposal will become visible in the Treasury screen and the council can start voting on it.

**Note the on-chain \# of your treasury proposal-** shown as a large number on the left of the row \(11 in the image above\), you'll want it for the next step. 

Now the council can take action, either turning it into a motion to approve or a motion to reject. 51% or more of the council must agree to take an action on any treasury spend.

{% hint style="info" %}
**Parameter Note:**  The _Treasury Spend Deposit_ is 5% of the proposed spend action, with a minimum of 1000 EDG. _Treasury Spends_ require 51% of the council to agree.
{% endhint %}

### Speak with the Community

Because the formal spend proposal lacks metadata for efficiency, sharing the details about the proposal off-chain is essential. We recommend using [Commonwealth.im/Edgeware](https://commonwealth.im/edgeware/discussions) and the community channels including telegram and discord.

* Post a discussion thread on Commonwealth
* Tag the title and body with **EDG\_TP\_\#** where \# is the official number of your treasury proposal, found on block explorers or Polkadot UI. 
* Announce the thread in other channels like Telegram to encourage awareness and debate.

Tagging helps users understand what module is being activated and what threads connect to what actions. Expect questions, challenges, and other remarks.  This can begin before or after you create your formal treasury proposal on-chain, but you won't know the TP\# until then.

