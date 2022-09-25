## Panda学长CS代写
**创始于北美 ｜专注cs全科代写 ｜ 100%原创MOSS查重**

**Panda学长**代写各类程序语言* *: C语言代写, C++代写, 算法作业代写, 数据结构代写, AI/MachineLearning代写, python代写, java代写, matlab代写, 汇编代写, scala代写, SQL/Database代写, racket代写, 安卓/Android代写, IOS/swift代写, racket代写, 网络代写, web代写, OS/操作系统代写, R代写* *

**为什么选择Panda学长CS代写？**

- 我们有经验丰富学历强大的**代写老师**，均毕业于常青藤/清华/北大/北航等顶级CS专业，大部分都是TOP ACMer、LeetCoder, 最快24-48小时即可完成，用技术和耐心帮助客户高效高质量提交作业。
- 我们**价格公道**，绝无高昂的中介费(比中介会便宜很多) 
- 我们的老师都是互相认识的好伙伴，有严格的评价机制，三次差评团队成员就要**强制退出**
- 我们的客服也是由**代写老师轮流担任**，在20分钟内准确高效的评估作业时间和难度，完成后团队有专人负责代码审计。相比于黑中介和个人代写不靠谱，我们团队让您的作业拿到更多分数
- **无限期售后服务**，真正的一站式无忧服务
- 专注留学生编程作业代写,起步于北美，cs业务遍及全球英语国家: [北美CS代写](https://github.com/codedaixie/csdaixie),[美国CS代写](https://github.com/codedaixie/csdaixie),[英国CS代写](https://github.com/codedaixie/csdaixie),[加拿大CS代写](https://github.com/codedaixie/csdaixie),[澳洲CS代写](https://github.com/codedaixie/csdaixie),[新西兰CS代写](https://github.com/codedaixie/csdaixie),[新加坡CS代写](https://github.com/codedaixie/csdaixie),[香港CS代写](https://github.com/codedaixie/csdaixie)

Please feel free to contact us anytime！

**客服24h咨询方式     **微信：cube787**


<img src='https://github.com/codedaixie/csdaixie/blob/main/image/down.png'>
<img src='https://github.com/codedaixie/csdaixie/blob/main/image/logo.png' width='85%'>


### IADS_coursework3 The travelling salesman problem

IADS coursework3 The travelling salesman problem

1 The travelling salesman problem
In this coursework we are going to explore the Travelling Salesman Problem (TSP). In this problem,
we are given an undirected graph on n nodes where the underlying graph structure is assumed to be
complete1
together with a weight function w : E → R+. The nodes of the graph represent a hypothetical
collection of cities that a salesman (or saleswoman!) is required to visit, and the weight w(u, v) represents
the cost of travelling directly from city u to city v (we will assume w(u, v) = w(v, u) always). The
salesman’s task is to visit each city exactly once before returning to the starting point, and although the
tour is restricted to visit every city exactly once, there is freedom to choose the order in which the cities
are visited. Therefore a (potential) tour can be identified with a permutation π : V → {0, . . . , n − 1} of
the nodes/cities, and the cost of such a tour is the sum of all the distances between the adjacent cities
along this tour, including the final edge back to the start:
n−1 X w(π(i), π((i + 1) mod n)). i=0
The Travelling Salesman Problem (TSP) is to find the shortest tour that visits each city once and returns
to the starting city. It one of the classical NP-complete problems2
, having been shown to be NP-complete
in Karp’s famous 1971 paper “Reducibility Among Combinatorial Problems”3.
The definition of TSP allows any combinations of (positive) weights to define distances between cities,
including very unrealistic combinations. If we are to believe that the distances correspond in some
way to a natural setting, we might assume that the distances correspond to the Euclidean (“straight
line”) distances from some embedding of nodes in the plane. This is maybe too idealistic (and indeed
a salesman taking public transport would not be travelling straight-line routes) - however, most natural
TSP problems would have distances which at least satisfy the triangle inequality, where we insist that
w(u, v) ≤ w(u, x) + w(x, v) for all u, v, x ∈ V . This restriction of the general TSP problem is called
the metric TSP problem. The case where the distances are given by a planar embedding is called the
Euclidean TSP problem. It is interesting that both these restricted cases remain NP-complete. 1Note that it is
not difficult to adjust the weights to model missing edges - we just add a very high weight to that edge.
2Of course, the NP-completeness proof will be set-up in terms of the decision version of the problem, where
we query
whether there is a tour of cost less than some given d. 3Karp’s paper, following “hot on the heels” of Cook’s
breakthrough result, demonstrated that 21 extra problems were
NP-complete. One of the 21 was “Hamiltonian Cycle” (HC), and it is an easy inference that when HC is NPcomplete,
TSP must also be.
1
In this coursework we will experiment with some heuristic approaches to TSP - a heuristic method is
a method which does not necessarily give any rigorous performance guarantees for the worst-case, but
which may do fairly-well on many instances of the problem. Your implementation should be in Python,
and since we will mark the coursework in python3.8 on DICE, you should check that your code runs
successfully with this installation.
The relevant files for this project are available as IADS cwk3.tar, and this contains some test files, a
graph.py file for implementation of the required methods, plus an (empty!) test.py file where you should set up your experiments. You will be required to submit graph.py, test.py plus also a short
report report.pdf. Details for the submission will appear on Learn.
2 Part A [25 marks]: Dealing with Graphs
In this Part of the coursework we complete setting-up/evaluation tasks for reading-in files and building
the corresponding graphs, and implement a simple method to score the cost of the current tour. graph.py
has one class Graph, and includes the declaration of the init method:
def init (self,n,filename):
We will allow for two kinds of input files, and your implementation of init will need to identify and
handle these two cases appropriately to build the “table” (list of lists) storing the distances between each
pair of nodes:
• We will allow instances of Euclidean TSP, these being flagged by calling the initialisation with n
set to the flag −1.
These Euclidean file instances will contain just the points/nodes of the graph, each point described
as a pair of integers (the x and y coordinates) on a single line, without any formatting. See
cities50 for an example of the format.
The distance between any pair of points can be calculated using the euclid method in graph.py.
The number of nodes of the graph is exactly the number of points in the file, so we lose nothing
by using n as a flag to indicate this type of input.
• We will also allow more general TSP inputs, possibly metric TSP, but even allowing non-metric
instances to be evaluated. However, for this format, we will assume the distances are integers.
For these inputs, the initialisation must be called with n set to the number of nodes of the input
graph (which will certainly be greater than −1). Each line of the input file describes one edge of the
graph, each line containing three integers, these being the first endpoint i, the second endpoint j
and the given weight/distance for the edge between i and j. See twelvenodes for an example of
this kind of input file.
We ask you to implement init so that we initialise the following variables as described.
• self.n - this should be initialised to the number of nodes/cities in the graph.
This will be the number of points in the input file for the Euclidian case, or the given n in the
general case.
• self.dists - this will be a two-dimensional “table” (in Python, a list of lists), such that the entry
self.dists[i][j] will contain the distance (either given in the general TSP, or calculated by
euclid in the Euclidean TSP) between nodes i and j).
This table should remain unchanged throughout the execution of the various methods of the class.
In filling this table, take care to always initialise the [j][i] cell as well as the [i][j] cell.
• self.perm - this is a list of length self.n which represents the permutation of the cities for the
current tour.
We will always initialise perm with respect to the identity permutation - ie, you should initialise
this to have perm[i] equal to i.
Note that we do expect that self.perm will change as our heuristic methods are applied to the
data.
2
It may be necessary to define some local variables for init (in particular, it may be helpful to have
a list of (pairwise) tuples to temporarily store the input points for the Euclidean case); however, these
are the only class variables which should be set up within init .
Your final task for Part A is to complete the method tourValue which evaluates, and returns, the cost
of the current tour, which is defined by the order of values in self.perm.
def tourValue(self):
Make sure that you remember to include the cost of the “wraparound” edge from the final node of the
permutation round to the first node.
testing: If you run this method for the twelvenodes input file, before applying any optimisation
heuristics, the result should be 34. For example:
>>> g=graph.Graph(12,"twelvenodes")
>>> g.tourValue()
34
3 Part B [35 marks] - Some Basic Heuristics
3.1 Swap Heuristic [10 marks]
In the first heuristic (called “Swap Heuristic”), we explore the effect of repeatedly swapping the order in
which a pair of adjacent cities are visited, as long as this swap improves (reduces) the cost of the overall
tour, or we reach some given bound k on the number of sweeps that will be carried out.
The method which governs the high-level control of this heuristic (the repeated swapping, subject to the
limitations on number of sweeps) is given to you as swapHeuristic. The number of “sweeps” allowed
by swapHeuristic is limited by the value of the k parameter; however, if -1 is supplied as the value
of k, then swapHeuristic will run until there is no improvement from the swaps. In this unbounded
case marked by k being -1, swapHeuristic will run until it achieves a local optimum with respect to the
swap-mechanism - however, this does not imply that we will have a global optimum with respect to our
input graph (as we will see when we run other heuristics).
If the aim is to consider what is possible with polynomial-time methods, then we should avoid running
the unbounded case of swapHeuristic, and should provide a polynomial-bounded value for k (such as n,
or maybe n*n).
Your job is to write the trySwap method which considers the effect of a specific swap (of self.perm[i]
and self.perm[(i+1) % self.n]), determines whether this change will (strictly) improve the cost of
the current tour, and if so, swaps those two values in self.perm.
def trySwap(self,i):
The function should return True if the update improves the cost of the tour (and the swap is made)
and False otherwise. Please avoid any needless inefficiency in coding the method.
testing: If we run swapHeuristic() with a correct implementation of trySwap on the initial data
(with default permutation) from twelvenodes, with k set to 12 (ie, the n of twelvenodes), the updated
tour will have cost 32:
>>> g=graph.Graph(12,"twelvenodes")
>>> g.tourValue()
>>> g.swapHeuristic(12)
>>> g.tourValue()
32
3.2 2-Opt Heuristic [10 marks]
The 2-Opt Heuristic is another heuristic which repeatedly makes “local adjustments” until there is no
improvement from doing these. In this case the alterations are more significant than the swaps - the
method TwoOptHeuristic repeatedly nominates a contiguous sequence of cities on the current tour, and
3
proposes that these be visited in the reverse order, if that would reduce the overall cost of the tour. The
high-level method TwoOptHeuristic has been implemented in graph.py, and has the same k parameter
as swapHeuristic (with the same interpretation of k being -1).
Your job is to implement the tryReverse method that considers the effect of a proposed reversal:
def tryReverse(self,i,j):
Your implementation must consider the cost of the current tour (as defined by self.perm), and then
consider the effect of reversing the “tour segment” from self.perm[i] to self.perm[j] (in other words,
to change self.perm[i] to the old self.perm[j], self.perm[i+1] to the old self.perm[j-1], and
so on.) If this reversal will make the tour length (strictly) shorter, then tryReverse must commit
self.perm to this reversal, and then return True indicating “success”; otherwise self.perm must be
left with its prior order, and False should be returned.
You should avoid any needless inefficiency in coding the method.
testing: If we have correct implementations of trySwap and tryReverse and run swapHeuristic()
immediately followed by TwoOptHeuristic on from twelvenodes, we should get a tour of cost 26:
>>> g=graph.Graph(12,"twelvenodes")
>>> g.swapHeuristic(12)
>>> g.TwoOptHeuristic(12)
>>> g.tourValue()
26
3.3 Greedy [15 marks]
A commonly used approach to optimization problems is the “greedy” approach, where at each step we
do what seems best, and hope that this will lead to a globally optimal solution. For the TSP problem,
this approach involves taking some initial city/node (for us, we will take the one indexed 0) and building
a tour out from that starting point. At the i-th step (for i = 0, . . .), we consider the recently-assigned
endpoint in self.perm[i] against all previously unused nodes, and then we take our next node (to be
saved as self.perm[i+1]) to be the one closest in distance to self.perm[i]. This will eventually create
a permutation within self.perm.
Note that sometimes there may be more one unused candidate node “closest in distance to self.perm[i]”;
if so, the algorithm should break ties by selecting the lowest-indexed of these unused closest vertices.
The final task in this section is to implement this method within graph.py:
def Greedy(self):
Test your new function. How well does the greedy heuristic perform? (it will not always do as well as
the combination of swapHeuristic, then TwoOptHeuristic). On twelvenodes, the result should be 26:
>>> g=graph.Graph(12,"twelvenodes")
>>> g.Greedy()
>>> g.tourValue()
26
4 Part C [20 marks] - Your Own Algorithm
The methods described in Part B are basic methods from the literature, which perform fairly well on
many instances. However, there is scope for improvement!
In this section, you are asked to implement an algorithm of your own, which you should describe in
your report. The algorithm should be polynomial-time and should be motivated by the specific details
of TSP, whether the general case, or the metric/Euclidean version. You might want to implement an
approximation algorithm with guaranteed performance bounds, or to implement an heuristic motivated
by some observation you notice about the problem. The TSP problem has been worked on by many
4
researchers, and if you want to draw on some past work, and implement a known (perhaps more
inter esting) algorithm for TSP than the ones in this specification, that is fine - you must credit the original
authors, describe the algorithm(s) in your own words, and write the implementation yourself.
This section will be assessed in terms of the Algorithm section of your report, about 1.5 pages of A4.
You should include an implementation of your algorithm inside graph.py (name it how you like).
The 20 marks will be distributed according to Algorithm novelty/ideas (8 marks), justification of
polynomial-time (4 marks), and effort/quality of implementation (8 marks). Be careful with how you
justify the polynomial-running time - note that Swap Heuristic and 2-Opt Heuristic are only polynomial time if
the k is polynomial in the size of the input.
5 Part D [20 marks] - Experiments
You have been provided with a small number of graphs to test your algorithms. In this section, you are
asked to carry out a broad collection of comparative experiments on all your implemented algorithms
(the three from Part B, and any Algorithm you have implemented for Part C). You will probably want to
write some code to generate random graphs according to certain parameters for size (number of nodes)
and weights (range for the weights, and probabilities).
Here there is scope to consider different settings for evaluation:
• The Euclidean setting (maybe varying the “window” of the plane to take in larger/wider values
for the x and y co-ordinates).
• The Metric setting (there are different ways of generating a graph which is guaranteed to be a
metric).
• The general non-Metric setting - does this change the quality of the results?
In carrying out experiments on randomly generated instances (or indeed, even the input files for the
Euclidian case), the questions arises of how close we are to the best answer? That is something hard to
know in general, as we have no polynomial-time algorithm to solve the problem! Some ideas that could
be used are the following:
• We may consider implementing a simple method (branch and bound, direct enumeration) to com pute an
exact solution, when we are working with a small number of nodes.
• For larger number of nodes, we can consider generating a graph to ensure it will have a “planted”
(but hidden) high-quality solution, then disguised by re-ordering of vertices and many distracting
competing edge-weights. This can provide more insight (and more interesting coding) than blindly
generating random graphs.
You should submit your code in tests.py; however, the most important detail is to describe your
experiments in the second (“Experiments”) section of your report. Please don’t only show tables, give
some explanation of what was interesting.
