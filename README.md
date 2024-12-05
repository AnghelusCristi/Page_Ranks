# Destabilize The Page Ranks
The objective of this project was to study the stability of the following 3 page ranking algorithms:
- In-Degree
- PageRank
- HITS

An algorithm is called ***stable*** if and only if small changes in the underlying graph will cause only small changes in the page ranks.<br><br>
A ***change*** in a graph G is a new graph G' with a link distance (minimum number of links that we need to add and/or remove in order to change one graph into the other), which is also called the size of the change.
A change may affect only a few of the nodes in G: those nodes whose incoming links have changed in any way.<br><br>

As part of the project, we tried to answer the following questions:
- What is the largest change in the rank vector, for each algorithm, that you can cause by making a change of size k in any graph of n nodes?
- What are the most vulnerable graphs we found, for each ranking algorithm, and what type of link change mattered most?
- Which ranking algorithm for web pages is most and least stable?

To answer the questions, we need a way to compare the page ranks. For this, we used the **Euclidean distance** to compute the difference between two ranking vectors.
We also needed to implement the ranking algorithms (implementation in the Python Notebooks).<br>

The first and second questions are answered in the corresponding Python Notebooks, which can generate the graphs and plots that support the conclusion. 
Additionally, for the 2nd question, the plots are already generated as pictures in the `plots` folder.

# Conclusions
- As k number approaches to n<sup>2</sup> the ranking distance increases for all algorithms.
- The In-Degree seems to be the most stable algorithm.
- The HITS seems the most unstable algorithm.
- The PageRank seems to be in between the 2 others.
- The Grid Graph is, by far, the most vulnerable graph for all the ranking algorithms.
- The Cycle, Tree, Complete and Disconnected graphs can also be quite vulnerable in general.
- The Small-World and Scale-Free graphs seem the least vulnerable.
- For HITS and In-Degree, adding changes (adding edges to the graph) seem slightly more influential, and for PageRank - removing changes (removing edges from the graph), but generally no big difference.

 These findings are subject to a degree of uncertainty due to their dependence on the graph's structure and the nature of the introduced changes.

