# Community Detection in the Twitter Network of the U.S. Congress using the Louvain Algorithm

By: Armand Aryasatya Prakarsa (armand.arsap@gmail.com) and Team!

This project was conducted as part of the Social Media Analytics course to analyze community structures within a Twitter interaction network. Specifically, we examined how members of the U.S. Congress engage with one another through retweets, mentions, and replies. The objective was to identify clusters of highly connected individuals and understand their interaction patterns using Social Network Analysis (SNA).

# Domain Overview
This project falls under the domain of Social Media Analytics and Network Science, specifically focusing on:

- Social Network Analysis (SNA)

- Community Detection in Social Media

- Political Communication & Digital Influence

With the increasing use of Twitter (X) as a platform for political discourse, understanding the patterns of interaction and community formation among political figures is essential for analyzing information flow, ideological clustering, and digital influence.

# Problem Statement
Twitter serves as a key platform for political discussions, where members of U.S. Congress engage in debates, share policy updates, and communicate with the public. However, interactions on social media often lead to political clustering and the formation of echo chambers, limiting exposure to diverse viewpoints.
This project aims to:
- Analyze Twitter interactions among U.S. Congress members.
- Detect communities within the network using the Louvain Algorithm.
- Identify key influencers and their roles in shaping political discourse.
- Evaluate network modularity to understand how strong these communities are.
By detecting hidden structures in the network, we can gain insights into partisan behavior, ideological polarization, and digital political influence.


# Research Scope
Network Formation:
- Construct a directed graph where nodes = Congress members and edges = interactions (retweets, mentions, replies).
- Identify highly connected nodes (hubs) and their influence in the network.
  
Community Detection:
- Apply Louvain Algorithm to segment the network into distinct communities.
- Evaluate modularity score to measure the strength of detected communities.
  
Network Influence Analysis:
- Identify key central nodes that act as bridges between communities.
- Analyze engagement patterns and potential echo chambers in the network.

# Technical Approach
- Graph-based Social Network Analysis (SNA) using NetworkX
- Community Detection using Louvain Algorithm (modularity optimization)
- Graph Visualization & Data Processing (Python, Pandas, Matplotlib)
- Network Influence Metrics (Degree Centrality, Betweenness Centrality)

# Expected Outcomes
- Identification of four major communities within the network.
- Analysis of central nodes influencing information flow.
- Evaluation of modularity score to measure network clustering.
- Insights into partisan clustering & digital political discourse.

# Dataset
![image alt](https://github.com/aarsyp/Community-Detection/blob/main/Community%20Detection%20Dataset.png?raw=true)

This study uses the “Twitter Interaction Network for the US Congress” dataset, downloaded from the Standford Network Analysis Project (SNAP). This dataset consists of 475 nodes (congressmen) and 13,289 interactions (edges) covering three main types of interactions, namely retweets, mentions, and quotes, taken from the official Twitter accounts of senators and representatives.
