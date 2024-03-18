---
title: "Detecting Fringe Behaviour in Companies"
draft: false
image: "/images/projects/tax.jpg"
---

By Alejandro Beltran

## Project description

Complicated company ownership structures are often set up to obfuscate the identification of beneficial owners.
These strategies are considered to be on the fringe of legitimacy and legality, so detecting them is important to regulators and society in general.
We combine economic theory, network analysis, and machine learning to unearth the patterns that such behaviours leave behind in large-scale administrative datasets.
This allows us to identify clusters of companies that specialise in such strategies, and to formulate models about their potential adaptation to future legal reforms. 
This project provides policymakers with guidance on how company ownership evolves over time as clusters that specialise in fringe behaviour learn and adapt to government enforcement mechanisms.  

## Birds of a feather


> "Using networks and machine learning to identify clusters of suspicious companies."


### Problem
* Over £30 billion in taxes lost to shell companies, £87.9 billion laundered through the UK.
* Companies House (CH) is a publicly accessible database of companies (incl. information like beneficial ownership).
* Difficult for CH to validate self-reported information, limited resources.

> * Can we use networks of firm directors to find suspicious companies?


### Method

* ICIJ dataset of companies appearing in Panama, Pandora, Paradise, Off-Shore leaks.
* Identify leaked companies operating in UK using Companies Houe API.
* Generate networks of firm directors. 
* Random forest algorithm to identify suspicious companies based on firm and network features 
> - Shared address, shared directors, compliance, audits, industry, business age. 

### Random Forest

|  | | Truth    |        |
| ---  | ---  | ---   | ---     |
|  | | leaked | not leaked |
| Prediction | leaked    | 7,625  | 70,310   |
| | not leaked    | 3,224   | 298,924     |

- Too many false positives.
> * Community detection to verify false positive and reduce false negatives. 


### Network analysis
#### Small community
* Example of a small community of firms directed by the same individiaul, pink squares are suspicious firms per model.
{{< shinyapps "https://rawcdn.githack.com/AlejandroBeltranA/firm-vis/6228d8b60748526fc4460c2036b5f627b150df70/community_154_pred.html">}}

#### Large community

* Example of a large cluster of firms directed by various individuals, pink squares are suspicious firms per model.

{{< shinyapps "https://rawcdn.githack.com/AlejandroBeltranA/firm-vis/43be8d95139001f55edfb3d2aba46a3f042e552c/community_25_spec.html">}}

#### Identifying suspicious communities

* Estimate the normalized degree centrality of a suspicious node. 
> * How important is the suspicious node within a community?

{{< shinyapps "https://rawcdn.githack.com/AlejandroBeltranA/firm-vis/3ca93140172e5b608d7f7c2732451dbebba5b419/degree_graph.html">}}

#### Visualizing suspicious communities

* Now we can focus our analysis on communities where suspicious nodes are central. 

{{< shinyapps "https://rawcdn.githack.com/AlejandroBeltranA/firm-vis/3ca93140172e5b608d7f7c2732451dbebba5b419/fringe_communities.html">}}


## Conclusion

* ~5.5 million firms registered with CH, 800,000 dissolved each year. 
* Many firms dissolved within the first year.
* Tracking, validating, and confirming their status is a data intensive task.
* Using leaks of companies appearing as clients of suspicious firms an effective approach.
* Pending: Analysis of all records, including dissolved firms from 2010 through today.



## People

* [Alejandro Beltran]({{< ref "/people/ab" >}}) 
* [Kathyrn R. Fair]({{< ref "/people/krf" >}}) 
* [Ben Klemens](https://ben.klemens.org/) 
* [Leonardo Castro Gonzalez]({{< ref "/people/lcg" >}}) 
* [Omar A. Guerrero]({{< ref "/people/oag" >}}) 

## Publications

Pre-print (forthcoming)

## Resources

Online repository (forthcoming)
