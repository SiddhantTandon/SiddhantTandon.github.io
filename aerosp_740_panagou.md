# Multi-Agent Control


**Project Description:** AEROSP 740 course by Dr. Dimitra Panagou, Winter 2020, University of Michigan.

## Project 1: Graph Networks and Formation

The first project I had to understand various graph networks (through which single agents can recieve signals or send signals or do both) and implement them on agents to see how they behave and form formations. By using graph theory we treat multi-agents as vertices of a graph and the signals between them as the edges.

The different types of graphs I tested and developed controllers for are shown below in the videos (developed using MATLAB).

The first three videos are multi-agent systems attaining a formation in which they are 100 m apart from each other horizontally and vertically.
The last three videos are on multi-agent circular formation.

Directed-path network is shown below in which, each agent is connected with two adjacent agents in the network and the signal between two agents is in one direction. More on directed-paths can be found [here](https://algs4.cs.princeton.edu/42digraph/).

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/q1yDDiPBfw4" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

Undirected Complete Graph is shown below, where each agent is connected with every other agent and can send and receive signals. More on undirected graphs can be found [here](https://algs4.cs.princeton.edu/41graph/).
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/DNGHmVaqm38" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

Undirected Path Graph is shown below, which is similar to directed path graph above, with the only difference that between two connected agents the signal can travel both directions.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/CqpdoK-UUN0" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

The video below is multi-agent circular formation using directed path graph.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/p_RM6nr5gW0" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

This video is on multi-agent circular formation using undirected complete graph.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/7rFQxpxci54" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

Lastly, video below is on multi-agent circular formation using undirected path graph.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/QPn-qyciQ0s" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->



## Project 2: Collision Avoidance and Safe Path Planning

The second project emphasized the use of control lyapunov functions and control barrier functions to build multi-agent controllers that are safe for operation. We can optimize for safe path planning formation, by implementing a [Quadratic Program](https://ncss-wpengine.netdna-ssl.com/wp-content/themes/ncss/pdf/Procedures/NCSS/Quadratic_Programming.pdf) with the aforementioned control functions as constraints.

Below we can see an example of multi-agent system that starts from given position and is moving towards its destination without colliding with other agents in the process.

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/uMbWNOECFKI" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

Another important control problem is that of resolving deadlocks, which happen when agents are moving towards each other on a straight line. An example is given below.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/yYBK6Aq2qME" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

There are ways to implement a controller to avoid such deadlocks by using perturbations. The video below shows that in action.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/jhrn8rpd-YU" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

## Project 3: Formation Flying, Obstacle Avoidance and Cyber-resilience

In the last project we learn to handle multiple agents in a real environment with obstacles. The aim was to create control lyapunov functions and control barrier functions which will lead to successful operation of the agents in the problem statement.

The first video is about how to control agents to form a formation when their origniating position is random in an obstacle environment.
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/Wl6cg81tRzo" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

The second aspect of the project was to move to this formation through the obstacle course to their new position. To implement this task, I created a leader-follower path network graph, which controls the agents to travel safely through the obstacles to their destinations.

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/-O_Jsy-oGNs" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

Multi-Agent networks are susceptible to attacks from hostile agents and thus cyber-resiliency of such systems is of utmost importance. One way to achieve resiliency is by using filters like the [Sliding Window Mean-Subsequence-Reduced](https://ieeexplore.ieee.org/document/7962962). Below are examples of SW-MSR in use when we have more than one malicious agents in the multi-agent network.



<p><a href="images/prob3_wmsr2.png">
  <figure>
    <img src="images/prob3_wmsr2.png"/>
    <figcaption><center>K-circulant graph with 2 malicious agents affecting consensus on altitude</center></figcaption>
  </figure>
</a></p>

<figure>
  <img src="images/prob3_wmsr.png"/>
  <figcaption><center>K-circulant graph now using SW-MSR filtering</center></figcaption>
</figure>

## Final  Project
For the final project, I went back to one of the first literature on formation flying by [C. Reynolds](http://www.red3d.com/cwr/boids/). He developed what he called 'boids' or agents which can be controlled to move in formations like birds or fishes. The intent was to recreate real life-like movement of graphics in computer. However, the literature became widely popular in the multi-agent community.

I personally like this Youtube Video on boids below:
<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/bqtqltqcQhw" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

I implemented my own version of it as shown below in a short video, capturing the major elements as described by C. Reynolds as 'separation' (or collision avoidance), 'alignment' (leader-follower) and 'cohesion' (formation control).

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/PjmeAlUoXE0" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->
