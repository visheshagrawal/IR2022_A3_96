# IR2022_A3_96

## Question 1
## Question 2
We have used the "NetworkX" python library to calculate the page rank, Hub and Authority scores on the Wiki-Vote.txt dataset.
### page rank
- It is the algorithm used by search engines to rank the results as a tool to measure the importance of each result
- We have taken the default value of the damping factor (0.85)
- We get the results as follows: 
![image](https://user-images.githubusercontent.com/43749564/163863141-d2da958f-a11d-4698-944d-512a51dfb71c.png)

### Hub and Authority Scores
- The authority score of each node is defined as per the incoming nodes fron the Hubs. Hub score of each node is defined by the outgoing links which link it to the authority nodes.
- Authority and Hub Scores are calculated for each node using Hyperlink-Induced Topic Search (HITS) algorithm
- We get the results as follows: 
- Authority
- ![image](https://user-images.githubusercontent.com/43749564/163863165-01c4f5ba-e2c5-4bea-a4ba-dca3bf04c04f.png)

- Hub score
- ![image](https://user-images.githubusercontent.com/43749564/163863409-3002ea48-cb26-4c05-bd46-5151de7e0e4d.png)

### Comparison
- When we compare the output we can observe that different nodes are given as important by both of the scoring metrics.
This can be probably due to the fact that the authority scores are high in magnitude only for those nodes who have incoming links from a high number of hubs. When we analyse the hub score, we observe the node and its outgoing nodes (max out degree) and we can notice that the node ____as observed in the previous question which has the highest out degreee has the highest score here as well.
- While on the other hand, Page rank takes the indegree into account and the node____  (max. indegree in question1) has the maximum page rank.
