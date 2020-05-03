# Digital_Media_Coursework
DELIVERABLE 2 EXTENSION: 
The extra analysis specified below needs to be conducted in addition to the network analysis that you selected for your chosen dataset (initial deliverable 2). 

The following work should supplement the literature review/results sections of your report. It should have a subheading in that section to clearly delineate it from the original work. This work should consume 2-4 pages of your report.

 Lit review/background: 
 Include in your literature/background section a brief outline on one of the following: 
1. How we generate random networks. Why do we compare things to random networks?
2. Robustness methods. How to study the robustness of a network?
3. PageRank and its application to network analysis. 
4. Cascades and how network structure impacts the flow of information.

Work: 
For Tasks 1 to 3 below, compare your network to 3 generated random networks (Erdos-Renyi or any other) based on the statistics of your dataset, i.e. you will need to maintain the same number of nodes and edges (or very close to) as the original dataset.  In answering/doing the below analysis, you should perform the task on your dataset and the 3 generated networks (the presented results should be the average seen across these 3).

●	Task 1. What are the differences between path length and clustering coefficients? 

●	Task 2. Which is more robust? To do this, you should remove edges based on tie strength (weak/strong) or some other measure (edge weight), or remove nodes (e.g. based on node degree), and plot what happens to the size of the giant component as you remove more and more edges/nodes.

●	Task 3. Calculate the pageranks for the network related to your dataset and the 3 generated random graphs. Compare the pageranks of the dataset network with the average pageranks of the 3 generated random graphs (present and discuss a graph or histogram).


Task 4. [This task has to be conducted on your dataset network only, not on the generated random graphs].
How cascade friendly is your network? Explore 2 different seed nodes (e.g. lowest degree centrality and direct neighbor, a node with average degree centrality and direct neighbor, highest degree centrality and direct neighbor, a random node and direct neighbor), or 2 different fractions of reached/infected nodes, in combination with 2 different thresholds (e.g. 0.1, 0.25, 0.5, 0.75), to determine how information flows/disease spreads through your network. 
Are there areas which are more likely to cause cascades than others when the initial reached/infected nodes belong to them? You can report the percentage or number of nodes reached/infected for each setting (e.g. table or graph).

If you solve this task without programming, using e.g. Gephi and a manual inspection of the cascades, you should use a smaller subset of your network (~30-50 nodes). If you choose to do this, ensure you state your sampling method (you will need to choose a sampling method like random walk) and ensure that your graphs remain connected.

Reports will be graded as follows:

Introduction and problem definition	10%

Related work
●	This should include information and background about the two seperate areas of analysis (The original background plus the chosen topic for extension).	20%

Dataset and algorithm/model description	20%

Results and findings
●	This should include information and background about the two seperate areas of analysis (The original results and finding plus the extra analysis).	40%

Style and Writing	10%

Groups should submit to QMPlus the PDF paper as detailed above.
Other information
You are free to use any data analysis tool, e.g. R, Matlab, Gephi, and can even calculate measurements by yourselves.

Supporting materials:

+ Software
1.	R and Data mining : Yanchang Zhao, Chap 10&11, http://www.rdatamining.com/home
2.	R language: Computing for Data Analysis https://www.coursera.org/course/compdata
3.	iGraph with R: http://www.r-bloggers.com/network-visualization-in-r-with-the-igraph-package/
4.	Gephi : Gephi - The Open Graph Viz Platformhttps://gephi.org/
Network analysis with Gephi: 10:55Gephi Tutorial - How to use Gephi for Network Analysis

+ Random graphs

●	The discussion of the paper “Structure and tie strength in mobile communications network” in the DMSN Week 2 Slides (27-35) provides an example of this kind of comparison (https://www.pnas.org/content/104/18/7332)
●	How to generate Random Graph in Gephi: Gephi Tutorials
https://www.youtube.com/watch?v=2KEl4zcAnO0
●	How to compare a graph to a random graph of the same number of nodes/edges in Python:
https://github.com/narnolddd/DMSNTutorials/blob/master/Week1/Week1.ipynb 

Note: when generating a Random Graph with Gephi, Gephi will generate a directed graph by default. If the network you would like to compare the random graph to is undirected, you should do the comparison using an undirected random graph. To obtain an undirected version of the random graph in Gephi, export the random graph file (File → Export) and then reimport it (File → Open) by selecting Graph type: undirected.

+ Robustness analysis

The structural robustness of networks is studied using percolation theory. When a critical fraction of nodes (or links) is removed the network becomes fragmented into small disconnected clusters (https://en.wikipedia.org/wiki/Network_theory).

●	See the example from “Structure and tie strength in mobile communications network” in the DMSN Week 2 Slides (27-35) as well for this section. More details in https://www.pnas.org/content/104/18/7332.
●	See example e.g. in DMSN Week 4 Network Analysis Slide 11:
The paper from Mislove et al. (2007) provides an example of the impact of progressively removing nodes with highest degree (0.01%, 0.1%, 1%, 10%) on the connectivity of the remaining graphs.
Mislove, A., Marcon, M., Gummadi, K. P., Druschel, P., & Bhattacharjee, B. (2007). Measurement and analysis of online social networks. In Proceedings of the 7th ACM SIGCOMM conference on Internet measurement (pp. 29- 42)

+ PageRank

In Gephi, the probability p used to simulate the user randomly restarting the web surfing corresponds to the probability 1-s in DMSN Week 6’s lecture on Web Search (slide 59), where s is a scaling factor.

●	PageRank in Gephi tutorial:
https://www.youtube.com/watch?v=A6fKPzdWLqI 

●	Pagerank Calculation in Gephi:
https://www.youtube.com/watch?v=JRqnWV4ZfnM
●	Identifying Influencers Using Pagerank Analysis
https://www.youtube.com/watch?v=OzyPZwSisZ0 


+ Cascades

●	Python users can use NDlib which has a method for implementing cascades in networks:
https://ndlib.readthedocs.io/en/latest/reference/models/epidemics/Threshold.html
●	For students without coding skills, please refer to the instructions and conduct a cascade analysis manually on a smaller subset of your network.



Some papers to start (more in notes): 
Structure and tie strengths in mobile communication networks. J. P. Onnela, J. Saramaki, J. Hyvonen, G. Szabo, D. Lazer, K. Kaski, J. Kertesz, A. L. Barabasi. Proceedings of the National Academy of Sciences, Vol. 104, No. 18. (13 Oct 2006), pp. 7332-7336.

Maintained relationships on facebook. Cameron Marlow, Lee Byron, Tom Lento, and Itamar Rosenn. 2009. On-line at https://www.facebook.com/notes/facebook-data-science/maintained-relationships-on-facebook/55257228858/ 

Social networks that matter: Twitter under the microscope.Bernardo A. Huberman, Daniel M. Romero, and Fang Wu. First Monday, 14(1), January 2009.

David A. Shamma, Lyndon Kennedy, and Elizabeth F. Churchill. 2009. Tweet the debates: understanding community annotation of uncollected sources. In Proceedings of the first SIGMM workshop on Social media (WSM '09). ACM, New York, NY, USA

P. Grabowicz, J. Ramasco, E. Moro, J. Pujol, V.. Eguiluz. Social features of online networks: the strength of weak ties in online social media. arXiv:1107.4009. July 2011.


