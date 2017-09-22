---
layout: default
---

# Overview

![PADS]({{ site.url }}/images/Intro-PADS.png "PADS Architecture") 
{: .pull-right}

*PADS* is a strategy-proof differentially private auction mechanism designed to allow cloud providers to trade resources with consumers in such a way that individual bidding information of the consumers do not get exposed through the auction mechanism. 
*PADS* provides differential privacy and approximate truthfulness guarantees while maintaining good performance in terms of revenue earned and allocation efficiency.


## What is the challenge? 
 + Protect Each User's Bidding Information through the Auctioning Mechanism.
 + Randomize to achieve Differential Privacy while also ensuring Higher Resource Allocation Utility.

## How the System Works?
 + PADS-ADP Scheme:
   + Iterative Exponential Mechanism: in every iteration, the mechanism chooses one winner from the bidders using an Exponential Mechanism until all bids are selected or all the resources get allocated. 
   + Approximate Differential Privacy: *PADS-ADP* can provide $(\epsilon,\delta)$-differential privacy. 
   + Truthfulness: *PADS-ADP* is truthful independent of the strategies used by the bidders.
 + PADS-DP:
   + Grouping Exponential Mechanism: the bids are grouped by the possible price outcomes.
   + Differential Privacy: *PADS-DP* can provide $\epsilon$-differential privacy. 
   + Approximate Truthfulness: *PADS-DP* is $\epsilon\Delta$-truthful and it is independentof the strategies used by the bidders.

**Publications**

 + Jinlai Xu, Balaji Palanisamy, Yuzhe Tang, S.D. Madhu Kumar (2017). [PADS: Privacy-preserving Auction Design for Allocating Dynamically Priced Cloud Resources](https://www.researchgate.net/publication/319910839_PADS_Privacy-preserving_Auction_Design_for_Allocating_Dynamically_Priced_Cloud_Resources), IEEE CIC 2017.
 
