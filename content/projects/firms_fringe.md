---
title: "Detecting Fringe Behaviour in Companies"
draft: false
image: "/images/projects/tax.jpg"
---


## Project description

Complicated company ownership structures are often set up to obfuscate the identification of beneficial owners.
These strategies are considered to be on the fringe of legitimacy and legality, so detecting them is important to regulators and society in general.
We combine economic theory, network analysis, and machine learning to unearth the patterns that such behaviours leave behind in large-scale administrative datasets.
This allows us to identify clusters of companies that specialise in such strategies, and to formulate models about their potential adaptation to future legal reforms. 
This project provides policymakers with guidance on how company ownership evolves over time as clusters that specialise in fringe behaviour learn and adapt to government enforcement mechanisms. 

## Birds of a feather



> "Using netowrks and machine learning to identify clusters of suspicious companies."


### Problem
* Over £30 billion in taxes lost to shell companies, £87.9 billion laundered through the UK 
* Companies House (CH) is the first publicly accessible database of companies (incl. information like beneficial ownership)
* No meaningful consequences for providing inaccurate info, limited resources for verification
> * Can we use firm ownership networks to find suspicious companies?

### Method

* ICIJ dataset of companies appearing in Panama, Pandora, Paradise, Off-Shore leaks
* ID leaked companies operating in UK using Companies Houe API
* Generate networks of firm ownership
* Random forest algorithm to ID suspicious companies based on firm and network features

### Visualizations

* Example of a small cluster of firms owned by the same individiaul, pink squares are suspicious firms per RF.
{{< shinyapps "https://rawcdn.githack.com/AlejandroBeltranA/firm-vis/6228d8b60748526fc4460c2036b5f627b150df70/community_154_pred.html">}}

* Example of a large cluster of firms owned by various individiauls, pink squares are suspicious firms per RF.

{{< shinyapps "https://rawcdn.githack.com/AlejandroBeltranA/firm-vis/43be8d95139001f55edfb3d2aba46a3f042e552c/community_25_spec.html">}}



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
