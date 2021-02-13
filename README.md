# A Step-by-Step Barabási–Albert Model in Python 3
#### by Aleksander Molak (06.2017)
email: aleksander.molak@gmail.com 

***NOTE**: to make sure the code from this repo works, please check your libraries versions with `requirements.txt`. Good luck and have fun!* 😊

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

**Note:** This implementation hasn't been optimized for computational speed or memory usage; feel free to reuse and improve this code.

### How does it work?
   When you run the script you are asked to specify network parameters:

* Initial number of nodes (<a href="https://www.codecogs.com/eqnedit.php?latex=m_0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?m_0" title="m_0" /></a>), where <a href="https://www.codecogs.com/eqnedit.php?latex=m>1" target="_blank"><img src="https://latex.codecogs.com/gif.latex?m>1" title="m>1" /></a>

* Final number of nodes

* **m** parameter (where <a href="https://www.codecogs.com/eqnedit.php?latex=m\leq&space;m_0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?m\leq&space;m_0" title="m\leq m_0" /></a>); This parameter controls how many new edges will every new node create


When the script reaches final number of nodes you can visualize your network. For example you can use:
   
```python
nx.draw(G, node_size=50, with_labels=0, alpha=0.6, node_color="#40a6d1", edge_color="#52bced")
```

and you should get a visualization similar to this:

![net_4_500_2](https://user-images.githubusercontent.com/28199898/29740901-0c37361a-8a62-11e7-8dc0-5c7abe6f2423.png)

You can also visualize degree distribution, using `k_distr()` function using linear or log-log scale. 

Degree distribution of **Barabási–Albert** network is `k**(-3)` and so it gives a straight line in log-log scale.

#### Examples:


* Linear scale example

```python
k_distrib(graph=G, colour='#40a6d1', alpha=.8)
```

![net_4_500_2_distr_lin](https://user-images.githubusercontent.com/28199898/29740902-0c398046-8a62-11e7-9a30-2d0a00751f22.png)

* Log-log scale example

```python
k_distrib(graph=G, colour='#40a6d1', scale='log', alpha=.8, fit_line=True, expct_lo=3, expct_hi=14, expct_const=8)
```

![net_4_500_2_distr_log](https://user-images.githubusercontent.com/28199898/29740900-0c371298-8a62-11e7-887a-8241533fd6c4.png)

***Note:** `expct_lo`, `expct_hi` and `expct_const` parameters are used to manually adjust theoretical distribution line in the plot*

Network visualization function `k_distr()` in based on the animation script by Abdallah Sobehy:
https://github.com/Abdallah-Sobehy/barabasi_albert/blob/master/BA.py


To see a few models I made with this Python script check these ![visualizations](./Aleksander_Molak_BA.pdf).

In case of any questions or if you simply wanna say hello, feel free to contact me 
<aleksander.molak@gmail.com>


Have fun! :)
