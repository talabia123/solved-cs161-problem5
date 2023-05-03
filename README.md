Download Link: https://assignmentchef.com/product/solved-cs161-problem5
<br>



<ol>

 <li>Consider the following directed graph:</li>

</ol>

For the following parts you might want to use this website, which allows you to draw directed graphs in L<sup>A</sup>TEX: <a href="http://madebyevan.com/fsm/">http://madebyevan.com/fsm/</a><a href="http://madebyevan.com/fsm/">.</a> (Note: On a Mac, fn+Delete will delete nodes or edges).

<ul>

 <li>Draw the DFS tree for this graph, starting from node A. Assume that DFS traverses nodes in alphabetic order. (That is, if it could go to either <em>B </em>or <em>C</em>, it will always choose <em>B </em>first).</li>

 <li><strong> </strong>Draw the BFS tree for this graph, starting from node A. Assume that BFS traverses nodes in alphabetic order. (That is, if it could go to either <em>B </em>or <em>C</em>, it will always choose <em>B </em>first).</li>

</ul>

<strong>[We are expecting: Pictures of your trees. No further explanation is required.]</strong>

<ol start="2">

 <li><strong> </strong>This exercise refers to ipynb, graphStuff.py, HW5 mysteryA.pickle, and HW5 mysteryB.pickle, available on the course website.</li>

</ol>

In class, we saw how to use BFS to determine whether or not a graph is bipartite; at least in theory. In this exercise, you will implement this idea (and hopefully also become familiar with the CS161Graph class that we’ll be using for the whole graph unit).

In HW5.ipynb, we have provided the BFS code that we saw in class. This does Breadth-First Search beginning at a single vertex <em>w </em>of a graph, and it explores <em>all of the things reachable from w. </em><strong>(Note that it does not necessarily explore the whole graph). </strong>HW5.ipynb imports graphStuff.py, which includes our implementation of CS161Graph and CS161Vertex.

Use the IPython notebook to load HW5 mysteryA.pickle and HW5 mysteryB.pickle, which load to CS161Graphs named <em>A </em>and <em>B</em>. The CS161Graph class supports directed graphs, but both graphs <em>A </em>and <em>B </em>are undirected in the sense that all edges go both directions: whenever there’s an edge (<em>v,w</em>), there is also an edge (<em>w,v</em>).

One of <em>A,B </em>is bipartite and one of them is not. (Recall that a graph is <em>bipartite </em>if its vertices can be divided into two sets <em>S </em>and <em>T </em>so that there are no edges within <em>S </em>and no edges within <em>T</em>). Adapt the code in the IPython notebook to decide which is which. Your code should run on CS161Graphs in time <em>O</em>(<em>n </em>+ <em>m</em>), where <em>n </em>is the number of vertices in the graph and <em>m </em>is the number of edges.

<strong>Note: </strong>You should not have to change the code in graphStuff.py, although you may if you want to. Notice that graphStuff.py has been modified slightly from class so that a CS161Vertex has a color attribute, which may be helpful.

<strong>[We are expecting: Your answer (which graph is bipartite?) as well as the code that you used, and an English description of the changes that you had to make. You may wish to</strong>

<strong>use the </strong>verbatim <strong>environment to include your code in L<sup>A</sup>T</strong><strong><sub>E</sub>X.]</strong>

<h1>Problems</h1>

You may talk with your fellow CS161-ers about the problems. However:

<ul>

 <li>Try the problems on your own <em>before </em></li>

 <li>Write up your answers yourself, in your own words. You should never share your typed-up solutions with your collaborators.</li>

 <li>If you collaborated, list the names of the students you collaborated with at the beginning of each problem.</li>

</ul>

<ol>

 <li><strong> </strong>Go over the problems on the midterm that you didn’t get. You don’t have to turn anything in, but this problem set is intentionally a little bit shorter to give you time to go over the midterm. Midterms will be handed back and solutions will be posted on Monday.</li>

 <li><strong> </strong>You arrive on an island with <em>n </em> The sheep have developed a pretty sophisticated society, and have a social media platform called Baaaahtter (it’s like Twitter but for sheep<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>). Some sheep follow other sheep on this platform. Being sheep, they believe and repeat anything that they hear. That is, they will re-post anything that any sheep they are following said. We can represent this by a graph, where (<em>a</em>) → (<em>b</em>) means that (<em>b</em>) will re-post anything that (<em>a</em>) posted. For example, if the social dynamics on the island were:</li>

</ol>

Sugar the sheep

the Sherman the Sheep follows Sugar the Sheep, and Sugar follows both Shakira and Shifra, and so on. This means that Sherman will re-post anything that Sugar posts, Sugar will re-post anything by Shifra and Shikira, and so on. (If there is a cycle then each sheep will only re-post a post once).

For the parts below, let <em>G </em>denote this graph on the <em>n </em>sheep. Let <em>m </em>denote the number of edges in <em>G</em>.

<ul>

 <li><strong> </strong>Call a sheep a <strong>source sheep </strong>if anything that they post eventually gets re-posted by every other sheep on the island. In the example above, both Shifra and Shakira are source sheep.</li>

</ul>

Prove that all source sheep are in the same strongly connected component of <em>G</em>, and every sheep in that component is a source sheep.

<strong>[We are expecting: A short but rigorous proof.]</strong>

<ul>

 <li>Suppose that there is at least one source sheep. Give an algorithm that runs in time <em>O</em>(<em>n </em>+ <em>m</em>) and finds a source sheep. You may use any algorithm we have seen in class as a subroutine.</li>

</ul>

<strong>[We are expecting: Pseudocode or an English description of your algorithm; a short justification that it is correct; and short justification of the running time. You may use any statement we have proved in class without re-proving it.]</strong>

<ul>

 <li>Suppose that you don’t know whether or not there is a single source sheep. Give an algorithm that runs in time <em>O</em>(<em>n </em>+ <em>m</em>) and either returns a source sheep or returns no source sheep. You may use any algorithm we have seen from class as a subroutine.</li>

</ul>

<strong>[We are expecting: Pseudocode or an English description of your algorithm, and an informal justification of why it is correct and runs in time </strong><em>O</em>(<em>n </em>+ <em>m</em>)<strong>.]</strong>

<ol start="3">

 <li>Let <em>G </em>= (<em>V,E</em>) be a directed graph. A <em>path </em>from <em>s </em>to <em>t </em>in <em>G </em>is formally defined as a sequence of edges</li>

</ol>

(<em>u</em><sub>0</sub><em>,u</em><sub>1</sub>)<em>,</em>(<em>u</em><sub>1</sub><em>,u</em><sub>2</sub>)<em>,</em>(<em>u</em><sub>2</sub><em>,u</em><sub>3</sub>)<em>,…,</em>(<em>u<sub>M</sub></em>−<sub>1</sub><em>,u<sub>M</sub></em>)

so that <em>u</em><sub>0 </sub>= <em>s</em>, <em>u<sub>M </sub></em>= <em>t</em>, and (<em>u<sub>i</sub>,u<sub>i</sub></em><sub>+1</sub>) ∈ <em>E </em>for all <em>i </em>= 0<em>,…,M </em>− 1. A <em>shortest path </em>is a path

((<em>u</em><sub>0</sub><em>,u</em><sub>1</sub>)<em>,…,</em>(<em>u<sub>M</sub></em><sub>−1</sub><em>,u<sub>M</sub></em>)) so that

<em>M</em>−1                                                            <em>M</em><sup>0</sup>−1

<h2>                                                                     X                                                    X 0                       0</h2>

weight(<em>u<sub>i</sub>,u<sub>i</sub></em><sub>+1</sub>) ≤                weight(<em>u</em><em>i,u</em><em>i</em>+1)

<em>i</em>=0                                                               <em>i</em>=0

for all paths ((

As we saw in class, Dijkstra’s algorithm can be used to find shortest paths in weighted graphs, when there are non-negative edge weights. In this exercise, we’ll see what happens when there <em>are </em>negative edge weights.

Consider the following version of Dijkstra’s algorithm, which has been modified to return a shortest path. (Note, this is pseudocode, not working Python code, although it is adapted from the IPython notebook for Lecture 11).

# Finds a shortest path from s to t in G def dijkstraShortestPath(G,s,t):

Initialize a data structure d which uses vertices as keys and stores real numbers. d[v] = Infinity for all v in G.vertices d[s] = 0

unsureVertices = G.vertices while len(unsureVertices) &gt; 0:

u = a vertex in unsureVertices so that d[u] is minimized if d[u] == Infinity:

# then there is nothing more that I can reach break

# update u’s neighbors for v in u.getOutNeighbors():

if d[u] + weight(u,v) &lt; d[v]: d[v] = d[u] + weight(u,v) v.parent = u

unsureVertices.remove(u)

# now I have all the information I need to find the shortest path from s to t.

if d[t] == Infinity:

return “Can’t reach t from s!”

path = [] current = t while current!= s:

path.append(current) current = current.parent path.append(current) path.reverse() return path

For all the questions below, suppose that <em>G </em>is a directed, weighted graph, which may have negative edge weights, containing vertices <em>s </em>and <em>t</em>. Suppose that there <em>is </em>some path from <em>s </em>to <em>t </em>in <em>G</em>.

<ul>

 <li><strong> </strong>Give an example of a graph where there is a path from <em>s </em>to <em>t</em>, but no shortest path from <em>s </em>to <em>t</em>.</li>

</ul>

<strong>[We are expecting: A small example (fewer than </strong>5 <strong>vertices) and an explanation of why there is not shortest path from </strong><em>s </em><strong>to </strong><em>t</em><strong>.]</strong>

<ul>

 <li><strong> </strong>Give an example of a graph where there <em>is </em>a shortest path from <em>s </em>to <em>t</em>, but dijkstraShortestPath(<em>G,s,t</em>) does not return one.</li>

</ul>

<strong>[We are expecting: A small example (fewer than </strong>5 <strong>vertices) and an explanation of what </strong>dijkstraShortestPath <strong>does on this graph and why it does not return a shortest path.]</strong>

<ul>

 <li><strong> </strong>Your friend offers the following way to patch up Dijkstra’s algorithm to deal with negative edge weights. Let <em>G </em>be a weighted graph, and let <em>w</em><sup>∗ </sup>be the smallest weight that appears in <em>G</em>. (Notice that <em>w</em><sup>∗ </sup>may be negative). Consider a graph <em>G</em><sup>0 </sup>= (<em>V,E</em><sup>0</sup>) with the same vertices, and so that <em>E</em><sup>0 </sup>is as follows: for every edge <em>e </em>∈ <em>E </em>with weight <em>w</em>, there is an edge <em>e</em><sup>0 </sup>∈ <em>E</em><sup>0 </sup>with weight <em>w </em>− <em>w</em><sup>∗</sup>. Now all of the weights in <em>G</em><sup>0 </sup>are non-negative, so we can apply Dijkstra’s algorithm to that:</li>

</ul>

modifiedDijkstra(G,s,t): Construct G’ from G as above. return dijkstraShortestPath(G’,s,t)

Does your friend’s approach work? (That is, does it always return a shortest path from <em>s </em>to <em>t </em>if it exists?) Either prove that it is correct or give a counter-example.

<strong>[We are expecting:      Your answer, along with either a short proof or a counterexample.]</strong>

<a href="#_ftnref1" name="_ftn1">[1]</a> Also my new start-up idea