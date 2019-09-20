# Spatio-temporal Anomaly Detection

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mizvol/anomaly-detection/master)

Example with random graph and random time-series signal. Implementation of the algorithm from [Anomaly detection in the dynamics of web and social networks](https://arxiv.org/abs/1901.09688) paper.

In this example, we use a random graph. The results largely depend on the structure of the graph. The results are much better when the structure of network makes sense (for example, social network or hyperlinks network). This is just a (very inefficient) demonstration for practitioners.

If you need a scalable version and more efficient implementation, use the [following code](https://github.com/epfl-lts2/sparkwiki/blob/master/src/main/scala/ch/epfl/lts2/wikipedia/PeakFinder.scala). To run it, first, you need to deploy two databases with Wikipedia graph (Neo4J) and pagecounts time-series (Apache Cassandra). To do that, please follow [these instructions](https://github.com/epfl-lts2/sparkwiki/tree/master/helpers).

Below, you can see the result of the code example provided here where the graph and time-series signals are random. Even though example initializes with a very dense random network, which does not provide any structural insights, we manage to get a prominent anomalous cluster. In order to get better results with your data, use underlying graph structure instead (social network, hyperlinks network). Unless you have that kind of graph, constructing a nearest neighbours graph is a better option than a random graph.




Initial graph            |  Anomalous cluster (bold edges)
:-------------------------:|:-------------------------:
![init](https://raw.githubusercontent.com/mizvol/anomaly-detection/master/img/initial.png)  |  ![learned](https://raw.githubusercontent.com/mizvol/anomaly-detection/master/img/learned.png)
