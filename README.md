# IR2022_A3_96
We have used the Wiki-Vote.txt network dataset, it can be described as follows:-
The network contains all the Wikipedia voting data from the inception of Wikipedia till January 2008. Nodes in the network represent wikipedia users and a directed edge from node i to node j represents that user i voted on user j.

![image](https://user-images.githubusercontent.com/43749564/164520339-fda64802-f4d7-42f8-aed8-638c60ec4b7e.png)
- Network Graph
- ![image](https://user-images.githubusercontent.com/43749564/164522848-6b0a7482-13a1-478b-8dfc-fd70af9aa5d9.png)
- Link to the Dataset- https://snap.stanford.edu/data/wiki-Vote.html
## Question 1
1. Number of Nodes= 7115
2. Number of Edges= 103689
3. Avg In-degree = 14.573295853829936
4. Avg. Out-Degree = 14.573295853829936
5. Node with Max In-degree= 4037
6. Node with Max out-degree = 2565
7. The density of the network = 0.0020485375110809584

### In-degree 
![image](https://user-images.githubusercontent.com/48515800/164524203-a16ad147-3246-43f8-b3d6-beb554fd6c69.png)

### Out-Degree Distribution
![image](https://user-images.githubusercontent.com/48515800/164524518-5a3691d5-63c4-4387-b9c4-44f03873927c.png)

### Local Clustering Coefficient
![image](https://user-images.githubusercontent.com/48515800/164524641-ed6b3171-2541-4aa2-bcc7-e9fc78c311a1.png)

### Formulas

1. Number of Nodes= len(node_set)
2. Number of Edges= total number of directed edges. len(edge_set)
3. Avg In-degree = In degree is the number of nodes where edge directs towards the node. Average in-degree is total in-degree divided by number of nodes
4. Avg. Out-Degree = Out degree is the number of nodes where edge directs away the node. Average out-degree is total out-degree divided by number of nodes
5. Node with Max In-degree= max(in_degree from in_degree list)
6. Node with Max out-degree = max(out_degree from in_degree list)
7. The density of the network = No. of Observed Edges/(Total number of possible edges)= m/n*(n-1)
8. Local Clustering Coefficient= ![image](https://user-images.githubusercontent.com/48515800/164527510-fe076161-349f-4bb3-9108-7169d4c8e101.png) Here vk and vk are vertices which are in the neighbourhood of node. And there is an edge between them. ki is the number of neighbours. So essentially this formula is number of connected neighbours divided by total possible neighbour edges.


## Question 2
We have used the "NetworkX" python library to calculate the page rank, Hub and Authority scores on the Wiki-Vote network dataset.

### page rank
- It is the algorithm used by search engines to rank the results as a tool to measure the importance of each result
- We have taken the default value of the damping factor (0.85)
- We get the results as follows: 
![image](https://user-images.githubusercontent.com/43749564/164520981-49a0a756-2b43-4865-9fab-aca9a5f0ee9b.png)
### Hub and Authority Scores
- The authority score of each node is defined as per the incoming nodes fron the Hubs. Hub score of each node is defined by the outgoing links which link it to the authority nodes.
- Authority and Hub Scores are calculated for each node using Hyperlink-Induced Topic Search (HITS) algorithm
- We get the results as follows: 
- Authority
- ![image](https://user-images.githubusercontent.com/43749564/164521072-eb9a52e7-859b-490a-b89d-bdf6a3ae029d.png)
- 
- Hub score
- ![image](https://user-images.githubusercontent.com/43749564/164521016-a9eda3aa-9344-46aa-8880-ca821e1d86bb.png)
### Comparison
- When we compare the output we can observe that different nodes are given as important by both of the scoring metrics.
This can be probably due to the fact that the authority scores are high in magnitude only for those nodes who have incoming links from a high number of hubs. When we analyse the hub score, we observe the node and its outgoing nodes (max out degree) and we can notice that the node 2565 as observed in the previous question which has the highest out degreee has the highest score here as well.
- While on the other hand, Page rank takes the indegree into account and the node 4037 (max. indegree in question1) has the maximum page rank.
