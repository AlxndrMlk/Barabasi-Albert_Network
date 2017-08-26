# Step-by-Step Barabási–Albert Model in Python 3
#### by Aleksander Molak (06.2017)
email: aleksander.molak@gmail.com 

### What is Barabási–Albert Network?
   The **Barabási–Albert (BA)** model is an algorithm for generating random scale-free networks 
using a preferential attachment mechanism.
Several natural and human-made systems, including the Internet, the world wide web, citation networks, 
and some social networks are thought to be approximately scale-free and certainly contain few nodes (called hubs) 
with unusually high degree as compared to the other nodes of the network. 
The BA model tries to explain the existence of such nodes in real networks. 
The algorithm is named for its inventors Albert-László Barabási and Réka Albert 
and is a special case of a more general model called Price's model.
(source: https://en.wikipedia.org/wiki/Barab%C3%A1si%E2%80%93Albert_model)

### What is this project about?
   The goal of this project was to built a step-by-step Barabási–Albert Network Model. 
I used Python 3 and networkx library to meet this objective.

### How does it work?
   When you run the script you are asked to specify network parameters:

* Initial number of nodes (<a href="https://www.codecogs.com/eqnedit.php?latex=m_0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?m_0" title="m_0" /></a>)

* Final number of nodes

* Initial number of edges: **m** parameter (where <a href="https://www.codecogs.com/eqnedit.php?latex=m\leq&space;m_0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?m\leq&space;m_0" title="m\leq m_0" /></a>)

   When the script reaches final number of nodes you can visualize your network. For example you can use:
   
```python
nx.draw(G, node_size=50, with_labels=0, alpha=0.6, node_color="#40a6d1", edge_color="#52bced")
```

and you should get a visualization similar to this:

![Network Visualization](./pics/net_4_500_2.png)

![net_4_500_2](https://user-images.githubusercontent.com/28199898/29740901-0c37361a-8a62-11e7-8dc0-5c7abe6f2423.png)

Network visualization function in based on animation script by Abdallah Sobehy:
https://github.com/Abdallah-Sobehy/barabasi_albert/blob/master/BA.py
