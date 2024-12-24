# Simple Greedy Algorithm for Public Transit Network Design


### Total Direct Passengers $$\(ds_{ij}\)$$ for Bus Line \(l\):
$$
ds_{ij} = \sum_{m \in N_l} \sum_{n \in N_l} d_{mn}
$$

### Matrix of Total Direct Passengers:
$$
D_S = \{ ds_{ij} \mid i, j \in [1, 2, \ldots, |N|] \}
$$
                         

![image](https://github.com/user-attachments/assets/827aa513-b1ce-4c44-8472-54122bae42c0)
Bus line whose terminals are located in the nodes 𝑖 and 𝑗. $$N_{l}$$ the set of nodes connected by the line 𝑙. Bus line 𝑙 contains all nodes that belong to the shortest path between 𝑖 and 𝑗. <br>

Step 1: Prescribe the total number of bus lines NBL in the network. Denote the set of bus lines by 𝑌 (set 𝑚=0).<br>
Step 2: Identify the highest $$\(ds_{ij}\)$$ pair, set terminals (a, b), find the shortest path between these two nodes, and add line 𝑙 to Y.<br>
Step 3: Update the matrix DS, without taking into account passenger travel demands that are already satisfied.<br>
Step 4: If 𝑚=𝑁𝐵𝐿, stop; otherwise, set 𝑚=𝑚+1 and return to Step 2. <br>
