# Cluster Analysis using 2016 Maryland General Election Data

## Background
I decided to explore this topic in the wake of the upcoming election on November 3, 2020. As someone who may live in Baltimore for the next few years after graduation, I wanted to see the voting patterns by county using the 2016 Maryland General Election Data, organized by county and party. I was particularly interested to see how the party affiliations affected the cluster analysis, as Maryland is known to be a blue state. 

## Business Question
How is party affiliation information useful to a candidate running for local office? Are there any counties with a high amount of absentee voters that will be likely to use mail-in voting for the upcoming election? 


## Data Sources
- [2016 Maryland General Elections Data by Party and County](https://github.com/vickidecastro/maryland-election-data-cluster-analysis/blob/main/party%20county%20election%20data.xlsx): For the general election on November 28, 2016. The file contained information on the number of people voting at the polls. early voters, absentee voters, provisional voters, total eligible voters, and voter turnout. The data also included all of these metrics separated by party-- Democrat and Republican-- as well. 

## Data Question(s)
How should counties be organized using voting patterns in Maryland? 

Which variables are the most appropriate to create a cluster analysis with? How many anchors should we pick? 

How are Maryland counties grouped based on number of absentee voters, number of early voters, number of Democrats and number of Republicans? 

## Data Analysis
_4-Cluster Analysis_

I used a 4-cluster analysis in Excel to look at voting patterns across counties in Maryland. The 4 clusters were based on: 
- Number of absentee voters
- Number of early voters
- Number of Democrats
- Number of Republicans

<img width="581" alt="Screen Shot 2020-10-19 at 12 11 41 PM" src="https://user-images.githubusercontent.com/70858878/96477519-9beb7280-1204-11eb-8e49-3213f75a7f21.png">
Figure 1: 4 clusters using absentee voters, early voters, Democrats, and Republicans


_Process_
- Gather data for each cluster
- Calculate mean and standard deviations for each cluster
- Calculate z-scores for each cluster
- Calculate distance^2 for each cluster
- Use formula to find minimum distance^2 for each county
- Sum all the minimum distance^2s 
- Use match function to identify anchor number for each county
- Using Excel Solver, run 4-cluster analysis with constraints

<img width="1061" alt="Screen Shot 2020-10-19 at 12 13 22 PM" src="https://user-images.githubusercontent.com/70858878/96477496-9130dd80-1204-11eb-9d66-a8cc72bd50fb.png">
Figure 2: cluster analysis process using Excel Solver

# Summary
Using Excel Solver to do a 4-cluster analysis, we found the 4 clusters to be Howard County, Worcester County, Prince George's County, and Baltimore County. The 4 variables chosen were number of absenee voters, number of early voters, number of Democrats, and number of Republicans. We found that Howard County, the first cluster, has an average number of absentee voters, a high amount of early voters, an average amount of Democrats, and a high amount of Republicans. In Worcester County, the second cluster, we found a low amount of absentee voters, a low amount of early voters, a low amount of Democrats, and a low amount of Republicans. In Prince George's County, the third cluster, there is a high amount of absentee voters, a high amount of eraly voters, a lot of Democrats, and a low amount of Republicans. In Baltimore County, the fourth cluster, there is a high amount for all four variables. 

<img width="783" alt="Screen Shot 2020-10-19 at 1 08 57 PM" src="https://user-images.githubusercontent.com/70858878/96488624-44e99b80-120c-11eb-9a9b-3123290d68ec.png">
Figure 3: data visualization of counties within each cluster



These results were very interesting. In terms of party affiliation, the information on z-scores for Democrats and Republicans would be useful for candidates who are running for a position within the local or state government, such as governor or county comissioner. Those running for office in the local government could look at the results of the cluster analysis and see which counties have high (or low) z-scores for number of Democrats and number of Republicans. If the z-score is low, the candidate may want to direct more resources and campaigning to those areas to capture more voters. 

Cluster 2 is the largest cluster in the analysis, and it has low Democrats and low Republicans, and this informatino is useful for a candidate running for local office that wants to sway counties to favor him/her.

Out of Maryland, it may be beneficial to do a cluster analysis using party affiliation for swing states, as a candidate could again look at the z-scores for party affiliation and increase rallying and campaigning in the districts/counties that have low scores. 

In terms of absentee ballots, this data is useful for local governments that are considering automatically sending mail-in ballots to individuals within a county. Using a cluster analysis, local officials could see which counties have a high amount of people using absentee ballots, which likely means they would vote-by-mail if given the option. Thus, local officials could send mail-in ballots to individuals in counties with a high z-score for absentee voting. Clusters 3 and 4 have high absentee voters, so local governments may want to consider automatically sending mail-in ballots to individuals in these counties as they may be more open to vote-by-mail. 

I find voting behaviors to be a very interesting topic, and if I were to add more clusters to the mix, I would add age as a cluster to my analysis. 

![image](https://user-images.githubusercontent.com/70858878/96489627-ac541b00-120d-11eb-9e07-4b9cac390115.png)
