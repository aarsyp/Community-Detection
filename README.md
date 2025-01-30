# Community Detection in the Twitter Network of the U.S. Congress using the Louvain Algorithm

By: 

Armand Aryasatya Prakarsa (armand.arsap@gmail.com)

Abror Muhammad Hazim (abrormhazim@gmail.com)

Ikhwan Wahyudin

This project was conducted as part of the Social Media Analytics course to analyze community structures within a Twitter interaction network. Specifically, we examined how members of the U.S. Congress engage with one another through retweets, mentions, and replies. The objective was to identify clusters of highly connected individuals and understand their interaction patterns using Social Network Analysis (SNA).

## Domain Overview
This project falls under the domain of Social Media Analytics and Network Science, specifically focusing on:

- Social Network Analysis (SNA)

- Community Detection in Social Media

- Political Communication & Digital Influence

With the increasing use of Twitter (X) as a platform for political discourse, understanding the patterns of interaction and community formation among political figures is essential for analyzing information flow, ideological clustering, and digital influence.

## Problem Statement
Twitter serves as a key platform for political discussions, where members of U.S. Congress engage in debates, share policy updates, and communicate with the public. However, interactions on social media often lead to political clustering and the formation of echo chambers, limiting exposure to diverse viewpoints.
This project aims to:
- Analyze Twitter interactions among U.S. Congress members.
- Detect communities within the network using the Louvain Algorithm.
- Identify key influencers and their roles in shaping political discourse.
- Evaluate network modularity to understand how strong these communities are.
By detecting hidden structures in the network, we can gain insights into partisan behavior, ideological polarization, and digital political influence.


## Research Scope
Network Formation:
- Construct a directed graph where nodes = Congress members and edges = interactions (retweets, mentions, replies).
- Identify highly connected nodes (hubs) and their influence in the network.
  
Community Detection:
- Apply Louvain Algorithm to segment the network into distinct communities.
- Evaluate modularity score to measure the strength of detected communities.
  
Network Influence Analysis:
- Identify key central nodes that act as bridges between communities.
- Analyze engagement patterns and potential echo chambers in the network.

## Technical Approach
- Graph-based Social Network Analysis (SNA) using NetworkX
- Community Detection using Louvain Algorithm (modularity optimization)
- Graph Visualization & Data Processing (Python, Pandas, Matplotlib)
- Network Influence Metrics (Degree Centrality, Betweenness Centrality)

## Expected Outcomes
- Identification of four major communities within the network.
- Analysis of central nodes influencing information flow.
- Evaluation of modularity score to measure network clustering.
- Insights into partisan clustering & digital political discourse.

## Dataset
![Image](https://github.com/user-attachments/assets/9f5d0ef5-04e5-4fd8-b08a-bc5e3a818adf)

This study uses the “Twitter Interaction Network for the US Congress” dataset, downloaded from the Standford Network Analysis Project (SNAP). This dataset consists of 475 nodes (congressmen) and 13,289 interactions (edges) covering three main types of interactions, namely retweets, mentions, and quotes, taken from the official Twitter accounts of senators and representatives.

### Dataset Statistics  

| Feature           | Value  |
|------------------|--------|
| Directed Graph  | Yes    |
| Node Features   | No     |
| Edge Features   | Yes    |
| Number of Nodes | 475    |
| Number of Edges | 13,289 |
| Format         | JSON   |


## Data Preprocessing

B.	Data Preprocessing
During data preprocessing phase, we examined the dataset for missing values and identified the data types of each column. The following summary provides an overview of the dataset structure after preprocessing:

| #   | Column        | Non-Null Count | Type  |
| --- | ------------- | -------------- | ----- |
| 0   | username      | 475 non-null   | object |
| 1   | In_connection | 475 non-null   | object |
| 2   | Out_connection| 475 non-null   | object |


As shown, all columns contain 475 non-null entries, indicating that there are no missing values in the dataset. The data type for each column is identified as object, which typically represents string or categorical data.

## Data Exploratory

In the Data Exploratory phase, we analyze the degree statistics of the dataset. The following table summarizes the degree statistics:

| Degree Type   | Count | Mean  | Std Dev | Min | 25%  | 50%  | 75%  | Max  |
|---------------|-------|-------|---------|-----|------|------|------|------|
| in_degree     | 475   | 27.98 | 21.99   | 0   | 13   | 22   | 37   | 127  |
| out_degree    | 475   | 27.98 | 18.35   | 1   | 17   | 24   | 35   | 210  |
| total_degree  | 475   | 55.95 | 34.83   | 2   | 33   | 48   | 69   | 284  |

Insights:
- The mean in-degree and out-degree are both around 27.98, while the total-degree mean is 55.95.
- High standard deviations indicate a wide variation in node connections.
- A few nodes have significantly higher degrees (max values of 127 for in-degree, 210 for out-degree, and 284 for total-degree).

## Total Degree

![Image](https://github.com/user-attachments/assets/33a2bb3c-739f-48ee-b952-9f7658ff32b9)

The histogram of total-degree shows a positively skewed distribution, with most nodes having a degree between 30-50. A small number of nodes have much higher degrees, peaking above 100, indicating a few highly connected members with broad networks. This long tail suggests that some members of Congress play a more central role in the network, likely influencing discussions and information flow. This degree distribution is typical of social networks, where most individuals have moderate connections, but a few "hubs" dominate.

## Community Characteristics

The community analysis reveals four distinct communities with varying sizes. The following table summarizes the communities, their total members, and a preview of some members:

| Community | Total Members | Preview Members                                                            |
|-----------|---------------|----------------------------------------------------------------------------|
| 1         | 175           | Robert_Aderholt, RepRickAllen, RepArmstrongND                             |
| 2         | 93            | SenatorBaldwin, SenJohnBarrasso, SenatorBennet                            |
| 3         | 186           | SenatorCantwell, SenDuckworth, SenMarkey                                  |
| 4         | 21            | SenatorCardin, ChrisVanHollen, MarkWarner                                 |

## Community Detection Visualization
![Image](https://github.com/user-attachments/assets/8824f3a3-7d32-4530-8ee9-93a0269c276b)

### Insights:
- Community 1 has 175 members, Community 2 has 93 members, Community 3 has 186 members, and Community 4 is the smallest with 21 members.
- The modularity score of the partition is **0.4375**, indicating a moderately strong community structure, meaning the graph is well-segmented into distinct subgroups.


## Conclusion

Based on the results of experiments the application of the Louvain algorithm for community detection on the constructed graph has provided valuable insights into the network's structure. The algorithm successfully partitioned the graph into four distinct communities, with varying sizes, and achieved a modularity score of 0.4375, indicating a moderately strong community structure. This finding suggests that the network, which represents the U.S. Congress, is composed of subgroups that could be influenced by factors such as political party affiliations, policy interests, or levels of member interaction. The identification of these communities is significant as it enhances our understanding of the complex relationships and collaborative dynamics within the legislative body. Future research could explore the characteristics and interactions within these subgroups in greater depth, examining how these community structures influence decision-making, policy formulation, and overall legislative processes. This study lays the groundwork for further analysis into the political and social structures that drive collaboration and competition in the context of U.S. governance.

