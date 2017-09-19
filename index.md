---
layout: default
---

# Overview

![PADS]({{ site.url }}/images/Intro-PADS.png "PADS Architecture") 
{: .pull-right}

We propose *PADS*, a strategy-proof differentially private auction mechanism that allows cloud providers to privately trade resources with cloud consumers in such a way that individual bidding information of the cloud consumers is not exposed by the auction mechanism. 
We demonstrate that *PADS* achieves differential privacy and approximate truthfulness guarantees while maintaining good performance in terms of revenue gains and allocation efficiency.
We evaluate *PADS* through extensive simulation experiments that demonstrate that in comparison to traditional auction mechanisms, *PADS* achieves relatively high revenues for cloud providers while guaranteeing the privacy of the participating consumers.

## What is the challenge? 
 + Protect Every Individual User's Privacy from Infering by the Adversaries
 + Involving Randomness but Also Keep High Utilities For Every Participant

## How the System Works?
 + PADS-ADP:
   + Iterative Exponential Mechanism: in every iteration, the mechanism chooses one winner from the bidders with Exponential Mechanism proportional to 
   $$Pr[ W \gets W \cup \{i\} ]_i = \frac{\exp(\epsilon^\prime b_i)}{\sum_{i\in R} \exp(\epsilon^\prime b_i)}$$
     Where \$$ \epsilon^\prime=\frac{\epsilon}{(e-1)\Delta \ln(e/\delta)}$$ is the intermediate differential private parameter in one iteration. 
     We choose one winner for each iteration until all the bids are selected or the VMs are all allocated. 
   + Approximate Differential Privacy: *PADS-ADP* can provide $(\epsilon,\delta)$-differential privacy. 
   + Truthfulness: *PADS-ADP* is truthfullness no matter what strategies are used by the bidders.
 + PADS-DP:
   + Grouping Exponential Mechanism: the bids are grouped by the possible prices. For each group, we calculate the score function: 
   $$F(S_i, \rho_i) = \rho_i |S_i|$$
     Based on the utility (the result of the score function) we calculate the probabiltiy of each group:
   $$ Pr_i = \frac{\exp(\frac{\epsilon}{2\Delta} \rho_i |S_i|)}{\sum_{\rho_j\in P} \exp(\frac{\epsilon}{2\Delta} \rho_j |S_i|)} $$
     Based on the probabiltiy, we randomly choose the winner group. 
   + Differential Privacy: *PADS-DP* can provide $\epsilon$-differential privacy. 
   + Approximate Truthfulness: *PADS-DP* is $\epsilon\Delta$-truthfullness no matter what strategies are used by the bidders.

**Publications**

 + Jinlai Xu, Balaji Palanisamy, Yuzhe Tang, S.D. Madhu Kumar (2017). [PADS: Privacy-preserving Auction Design for Allocating Dynamically Priced Cloud Resources](https://www.researchgate.net/publication/319910839_PADS_Privacy-preserving_Auction_Design_for_Allocating_Dynamically_Priced_Cloud_Resources), IEEE CIC 2017.
 
