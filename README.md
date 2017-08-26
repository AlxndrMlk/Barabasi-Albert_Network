# A Step-by-Step Barabási–Albert Model in Python 3
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
   In this project I built a step-by-step Barabási–Albert Network Model using Python 3 and networkx library.

When you run a program you are asked to specify network parameters:

* Initial number of nodes (m_0)

* Final number of nodes

* (m<=m_0): 2


Network visualization function in based on animation script by Abdallah Sobehy:
https://github.com/Abdallah-Sobehy/barabasi_albert/blob/master/BA.py
