# Cluster Analysis using 2016 Maryland General Election Data

## Background
I decided to explore this topic in the wake of the upcoming election on November 3, 2020. As someone who may live in Baltimore for the next few years after graduation, I wanted to see the voting patterns by county using the 2016 Maryland General Election Data, organized by county and party. I was particularly interested to see how the party affiliations affected the cluster analysis, as Maryland is known to be a blue state. 

## Data Sources
- 2016 Maryland General Elections Data by Party and County: For the election on November 28, 2016 between Donald Trump and Hillary Clinton. The file contained information on the number of people voting at the polls. early voters, absentee voters, provisional voters, total eligible voters, and voter turnout. The data also included all of these metrics separated by party-- only Democrat and Republican-- as well. 

## Business Question
How should counties in Maryland be organized based on voting patterns? 

## Data Question(s)
Which variables are the most appropriate to create a cluster analysis with? How many anchors should we pick? 

How are Maryland counties grouped based on number of absentee voters, number of early voters, number of Democrats and number of Republicans? 

## Data Analysis
_4-Cluster Analysis_

I used a 4-cluster analysis in Excel to look at voting patterns across counties in Maryland. The 4 clusters were based on: 
- Number of absentee voters
- Number of early voters
- Number of Democrats
- Number of Republicans


_Process_
- Gather data for each cluster
- Calculate mean and standard deviations for each cluster
- Calculate z-scores for each cluster
- Calculate distance^2 for each cluster
- Use formula to find minimum distance^2 for each county
- Sum all the minimum distance^2s 
- Use match function to identify anchor number for each county
- Using Excel Solver, run 4-cluster analysis with constrains
