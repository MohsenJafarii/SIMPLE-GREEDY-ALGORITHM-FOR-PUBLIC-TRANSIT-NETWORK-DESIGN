# Simple Greedy Algorithm for Public Transit Network Design

Total Direct Passengers 𝒅𝒔_𝒊𝒋 for bus line 𝒍:<br>
𝑑𝑠_𝑖𝑗=∑2_(𝑚𝜖𝑁_𝑙)∑2_(𝑛𝜖𝑁_𝑙)𝑑_𝑚𝑛                                                    

Matrix of Total Direct Passengers:<br>
𝐷𝑆={𝑑𝑠_𝑖𝑗 |𝑖,𝑗𝜖[1,2,…,|𝑁|}                                                

![image](https://github.com/user-attachments/assets/827aa513-b1ce-4c44-8472-54122bae42c0)
Bus line whose terminals are located in the nodes 𝑖 and 𝑗. 𝑁_𝑙 the set of nodes connected by the line 𝑙. Bus line 𝑙 contains all nodes that belong to the shortest path between 𝑖 and 𝑗. <br>

Step 1: Prescribe the total number of bus lines NBL in the network. Denote the set of bus lines by 𝑌 (set 𝑚=0).<br>
Step 2: Identify the highest 𝑑𝑠_𝑖𝑗 pair, set terminals (a, b), find the shortest path between these two nodes, and add line 𝑙 to Y.<br>
Step 3: Update the matrix DS, without taking into account passenger travel demands that are already satisfied.<br>
Step 4: If 𝑚=𝑁𝐵𝐿, stop; otherwise, set 𝑚=𝑚+1 and return to Step 2. <br>
