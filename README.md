Download Link: https://assignmentchef.com/product/solved-csc349-assignment-8-approximation-algorithms
<br>
<strong>Deliverables:</strong>

<strong>GitHub Classroom: </strong><a href="https://classroom.github.com/a/Gbga1MOi">https://classroom.github.com/a/Gbga1MOi</a>

<strong>Required Files: </strong>compile.sh, run.sh

<strong>Optional Files: </strong>*.py, *.java, *.clj, *.kt, *.js, *.sh

By now you are very familiar with the Vertex Cover problem:

<strong>Input: </strong>A graph <em>G </em>= (<em>V,E</em>).

<strong>Goal: </strong>Find a vertex cover of minimum size.

We will implement a log(<em>n</em>)-approximation algorithm, a 2-approximation algorithm for this problem (this differs from the 2-approximation in class), and an exact (but slow) algorithm. <strong>log</strong>(<strong>n</strong>)<strong>-Approximation Algorithm</strong>

SmartGreedyVertexCover(<em><sub>G</sub></em>)

<strong>Input: </strong>A graph <em>G</em>.

<strong>Output: </strong>A set of vertices that form a (not necessarily optimal) vertex cover.

1: <em>C </em>←∅

2: <strong>while </strong><em>G </em>has at least one edge <strong>do</strong>

3:               <em>v </em>← vertex in <em>G </em>with maximum degree

4:                 <em>G </em>← <em>G </em> <em>v </em>(This also removes all edges adjacent to <em>v</em>)

5:             <em>C </em>← <em>C </em>∪ <em>v</em>

6: <strong>return </strong><em>C</em>

Implement this algorithm.

<strong>2-Approximation Algorithm </strong>BasicGreedyVertexCover(<em><sub>G</sub></em>)

<strong>Input: </strong>A graph <em>G</em>.

<strong>Output: </strong>A set of vertices that form a (not necessarily optimal) vertex cover.

1: <em>C </em>←∅

2: <strong>while </strong><em>G </em>has at least one edge <strong>do</strong>

3:              (<em>u,v</em>) ← any edge in <em>G</em>

4:                   <em>G </em>← <em>G </em>{<em>u,v</em>} (This also removes all edges adjacent to <em>u </em>and <em>v</em>)

5:               <em>C </em>← <em>C </em>∪{<em>u,v</em>}

6: <strong>return </strong><em>C</em>

Implement this algorithm.

<strong>Exact Algorithm</strong>

Implement a brute force (exact) algorithm for vertex cover.

<h1>1  of 2</h1>

CPE 349 – Algorithms                                                                                 <strong>Approximation Algorithms – Programming Assignment 8</strong>

Fall 2019                                                                                                                                                <strong>Due: Thursday, December 5th</strong>

<strong>Format:</strong>

The input graph will be undirected and simple (no self loops or multiple edges). The format will be a simple edge list. There will be <em>n </em>vertices and <em>m </em>edges. Each edge in the graph will be represented by a pair of vertex identifiers. Note that I will not give you graphs with isolated vertices. All edge lists will begin at 0.

For example the following graph is represented by the list:

1 2

1 3 2 3 1 4 0 5 4 3 3 0

<strong>What to turn in via GitHub Classroom by 8pm of the due date:</strong>

<ul>

 <li>Accept the following GitHub Classroom assignment: <a href="https://classroom.github.com/a/Gbga1MOi">https://classroom.github.com/a/Gbga1MOi</a><a href="https://classroom.github.com/a/Gbga1MOi">. </a>This will create a GitHub repository which you will use to submit your source code for this assignment. The repository will also include some basic sample inputs and outputs.</li>

 <li>Your algorithm should take an edge list and output the vertices corresponding to three vertex covers.</li>

 <li>Your program must read input from a file (given as the first command line argument) and write output to stdout.</li>

</ul>

<h1></h1>