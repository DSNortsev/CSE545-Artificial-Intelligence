# CSE545-Artificial-Intelligence

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence)


In this course we will be solving The Travelling Salesman Problems (TSP) with different algorithms. 

#### Languages and Tools:
[<img align="left" alt="Python" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png" />][python]
[<img align="left" alt="Jupyter Notebook" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/jupyter-notebook/jupyter-notebook.png" />][jupyter_notebook]
[<img align="left" alt="Git" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/git/git.png" />][git]
 
</br>

## List of projects:

- [Project 1: TSP with Brute Force](#project-1-tsp-with-brute-force)
- [Project 2: TSP search with BFS and DFS](#project-2-tsp-search-with-bfs-and-dfs)
- [Project 3: TSP with Closest Edge Insertion Heuristic](#project-3-tsp-with-closest-edge-insertion-heuristic)
- [Project 4: TSP with Genetic Algorithm](#project-4-tsp-with-genetic-algorithm)
- [Project 5: TSP GA with Wisdom of Artificial Crowds](#project-5-tsp-ga-with-wisdom-of-artificial-crowds)



## Project 1: TSP with Brute Force

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project1/project1.ipynb)

### Introduction
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;In this project we will review The Travelling Salesman Problem (TSP). The TSP is a problem in Computer Science used to demonstrate intractability and optimization. In short, imagine a salesman who wishes to visit every one of N cities exactly once each. For salesman it does not matter which order he visits the cities as he is equally proficient in applying is selling skills in them all regardless. All that matters is that he takes the shortest route between them all before returning back to the start. This kind of problem is also known as Hamiltonian Cycle to find the minimum weight. 
<br></br>
&nbsp;&nbsp;&nbsp;&nbsp;We would run python code that would demonstarte a TSP simulation and attempt to solve the problem by Brute Force. The Brute Force algorithms is a straightforward method of solving a problem that rely on sheer computer power that will go through all possible solution extensively. A Brute Force solution is 100% possible for only 25 cities which is approximately 15.5 septillion unique permutation, which would make it impossible to find the global optimal solution for large dataset 
</p>

### Result
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;For this experiment, we have analyzed the performance of Brute Force algorithm with different TSP files that contains different number of cities with the range from 4 to 12. Each city record has “x” and “y” coordinates, then we used the Euclidian distance formula to find the  distance between two cities. We also found all possible premutation, other word all possible variations of tours. Then we calculated the total cost of each tour and the tour with minimum cost has been chosen. The computation power of my laptop was  not enough to find the best tour with the dataset of 12 cities due to kernel crash. 
</p>


| Total cities  | Running Time  |
| :------------:| -------------:|
|       4       |    24.6 ms    |  
|       5       |    28.2 ms    |
|       6       |    30.2 ms    |
|       7       |    48.5 ms    |
|       8       |     221 ms    |
|       9       |     1.97 s    |
|      10       |     21.1 s    |
|      11       |  4 min 32 s   |



<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;By looking at the table above, we can conclude that the Brute Force search to TSP has the runtime complexity of  O(n!), which means each time N ( number of cities) is incremented, the runtime is multiplied by N. For example the number of tours for N=4 is 4*3*2*1 = 24, 11! = 39916800. This algorithm would only work for small datasets, in order to be able to find best route for large dataset,  this algorithm needs to be optimized. 
</p>

## Project 2: TSP search with BFS and DFS

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project2/Project2.ipynb)

### Introduction
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp; In the second project we will review Breadth First Search (BFS) and Depth First Search (DFS) algorithms for Traveling Sale Person (TSP).  We will have two input data the start city and the goal city, where we need to find the shortest path with minimum cost.  BFS is one of the most commonly used approach where you start traversing from the selected node ( source or starting node) and traverse the graph layer wise by exploring neighbor nodes ( nodes that are directly connected to the source node) and keep moving toward the next level  neighbor nodes until the goal node is reached. DFS is an algorithm for searching a graph or tree data structure by starting at the root node and goes as far as it can down a given path, then backtracks until it finds an unexplored path, and then explores it. The algorithm does this until the entire graph is explored and then returns the shortest path. 
</p>

### Result
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;For this experiment, we have analyzed the performance of BFS and DFS algorithm. The total execution time of DFS is 667 μs where BFS algorithm has been completed in 349 µs. We can see that  that the running time of the BFS algorithms almost twice lower for particular scenario because the shortest path exists in 4th layers of the tree. We can conclude that BFS is more suitable for searching goal node that are closer to the source node where DFS would perform better when the shortest path is far away from the goal node. 
</p>

## Project 3: TSP with Closest Edge Insertion Heuristic

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project3/project3.ipynb)

### Introduction
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;For the third project, we will demonstarte a TSP simulation to solve TSP problem by Closest Edge Insertion Algorithm . The Closest Edge Insertion is a straightforward method  with computational complexity O(n^2). The main idea of this algorithm is to start from tour of the two closest cities, repeatedly choose the non-tour city with the minimum distance to its nearest neighbor among the tour city , and insert it in between the two consecutive tour cities for which such an insertion causes the minimum increase in total tour length.
</p>

### Result
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;For this experiment, we have analyzed the performance of Closest Edge Insertion algorithm with two TSP files that contains 30 and 40 cities. Each city record has “x” and “y” coordinates, then we used the Euclidian distance formula to find the  distance between two cities. Then we have built a list of completed tours (that has a cycle) by adding one city to the graph and calculate the total cost of the final tour.  Since the first city has been chosen randomly the total cost of the final tour is different every time the program runs. 
<br></br>
The best tour for TSP with 30 cities where the first city has been chosen randomly:
<br></br>
</p>

```shell
[23, 17, 2, 14, 22, 27, 9, 5, 26, 12, 18, 4, 13, 25, 6, 20, 29, 11, 16, 10, 8, 15, 30, 1, 24,
 7, 21, 3, 19, 28, 23]
```

![30 Nodes](https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project3/30nodes.gif)

<p>
The best tour for TSP with 40 nodes:
<br></br>
</p>

```shell
[7, 24, 1, 30, 15, 39, 40, 10, 8, 16, 11, 18, 38, 29, 20, 6, 25, 13, 31, 33, 4, 35, 26, 5, 9, 27,
 22, 14, 2, 12, 37, 36, 34, 28, 32, 19, 3, 21, 23, 17, 7]
```

![40 Nodes](https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project3/40nodes.gif)


| Total cities  | Running Time  | Total cost |
| :------------:| -------------:| ----------:|
|       30      |    9.02 ms    |    497.1   |
|       40      |   20.08 ms    |   632.15   |


<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;From the table above, we can see that the running time is doubled by adding 10 nodes to the graph which is still much faster than the Brute Force search algorithms  from the project 1 where it takes 4 minutes and 32 seconds to find the optimal path. 
</p>


## Project 4: TSP with Genetic Algorithm

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project4/project4.ipynb)

### Introduction
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;Genetic Algorithms(GAs) are adaptive heuristic search algorithms that belong to the larger part of evolutionary algorithms. Genetic algorithms are based on the ideas of natural selection and genetics. Generally, GA is composed of two processes. The first process is selection of individuals for the production of the next generation and the second process is manipulation of the selected individuals to form the next generation by crossover and mutation techniques. The selection mechanism determines which individuals are chosen for mating (reproduction) and how many offspring each selected individual produces. The main principle of selection strategy is “the better is an individual; the higher is its chance of being parent.” Generally, crossover and mutation explore the search space, whereas selection reduces the search area within the population by discarding poor solutions. However, worst individuals should not be discarded and they have some chances to be selected because it may lead to useful genetic material. A good search technique must find a good trade-off between exploration and exploitation in order to find a global optimum [1]. Hence, it is important to find a balance between exploration (i.e. poor solutions must have chance to go to the next generation) and exploitation (i.e. good solutions go to the next generation more frequently than poor solutions) within the mechanism of the selection.
</p>

### Approach
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;For this project, we have analyzed the performance of Genetic Algorithm with a TSP file that contains different 100. Each city record has “x” and “y” coordinates, then we used the Euclidian distance formula to find the  distance between two cities. First step in Genetic Algorithm is to generate a random population meaning create different combination of tours and use fitness function to find the total cost of each tour. Then, Selection method can be applied, we have decided to select 30% of population  with the highest rank (tours with the minimum cost), and select 70% of tours randomly with the highest probabilities of best routes. After selection step is completed,  then Crossover method can be applied. In this project, we have decided to use three different methods such as order crossover, maximal preservation crossover and partial mapped crossover. 
<br>
&nbsp;&nbsp;&nbsp;&nbsp;The order crossover (OX)  builds offspring by choosing a subtour of a parent and preserving the relative order of bits of the other parent. The partially mapped crossover (PMX) is choosing two random cut points on parents to build offspring, the portion between cut points, one parent’s string is mapped onto the other parent’s string and the remaining information is exchanged. The  maximal preservation crossover (MPX) operator is closely related to the PMX crossover operator. MPX operates by initially selecting a random substring from the first parent. This subtour is usually defined as being a tour with string length less than or equal to the TSP problem size n divided by 2. The second stage of MPX is to remove the elements currently in the offspring from the second parent. Then the remaining elements are inserted into the offspring, the first parent’s substring having been placed at the start of the offspring and the remaining free elements of the offspring being filled by the clean parent 2 strings. [2]
<br>
&nbsp;&nbsp;&nbsp;&nbsp;The third step in Genetic Algorithm is a mutation. Mutation serves an important function in GA, as it helps to avoid local convergence by introducing novel routes that will allow to explore other parts of the solution space. Similar to crossover, the TSP has a special consideration when it comes to mutation, in our project we will be using the following methods such as  swap, insertion and displacement. Insertion Mutation selects a city at random and inserts it at random position. Displacement Mutation selects a sub tour at random and inserts it at a random position outside the sub tour. Insertion can be viewed as a special case of displacement in which the substring contains only one city. Swap mutation selects two positions at random and swaps the cities on these positions. [3]
<br>
&nbsp;&nbsp;&nbsp;&nbsp;All above steps such as Ranking, Selection, Crossover and Mutation need to be repeated until algorithm reaches the result that meets the stopping criteria. In our project, the stopping criteria  is when an algorithm cannot find a better route in 50 consecutive generations. 
</p>

### Results
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;For our experiment, we have run genetic algorithm 4 times with different  combination of crossover and mutation methods with 100 population size and 50 generation without improvement before terminating. Also, we have decide to use 0.9 crossover rate and 0.1 mutation rate which is one of the most common practice.
<br>
</p>

```shell
The best route: [64, 35, 29, 25, 6, 60, 81, 79, 68, 30, 73, 89, 74, 83, 10, 90, 16, 99, 
70, 93, 86, 46, 34, 61, 55, 96, 100, 52, 28, 32, 63, 91, 19, 53, 23, 39, 41, 3, 21, 66,
38, 37, 36, 7, 75, 17, 94, 85, 24, 71, 1, 92, 72, 43, 95, 15, 20, 98, 40, 13, 56, 33, 97,
51, 54, 8, 69, 11, 12, 87, 2, 67, 27, 9, 82, 44, 80, 58, 42, 5, 57, 78, 88, 22, 45, 65,
48, 76, 14, 50, 62, 26, 77, 49, 47, 18, 4, 59, 31, 84, 64]

Total cost: 1060.45
Total number generations: 1097
```

![100 Nodes gif](https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project4/genetic_algorithm.gif)

Final solution: 

![100 Nodes](https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project4/graphs/project_4_135.png)
![Performance](https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project4/project_4_performance.png)

<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;After plotting the performance of Genetic Algorithm, we can see that after 300 - 400 generations there is no much improvements, the best result we have received  in 1097 generation which takes 3 times longer. It might not be reasonable to run for so many generation and get a better result, because it would require much more computational power. We can also notice that not every generation give a better solution, sometimes the new generation performs worse than previous generation, but the overall tendency is performance increases throughout many generations.
<br>
&nbsp;&nbsp;&nbsp;&nbsp;In conclusion, the genetic algorithm is useful for NP-hard problems,  but it does depend on selection criteria, crossover and mutation operation. This algorithm  can be improved by not selecting the first population randomly instead  Dijkstra's Algorithm (with time complexity O (ElgV) ) cab be applied and then Genetic Algorithm can be used to find the shortest path. In that case, the total number of generations would decrease  because at the starting point there is some routes with better total cost, which random solution does not guarantee it. 
<br>
</p>

### References
<p align="justify">
[1]  Noraini Mohd Razali, John Geraghty, “Genetic Algorithm Performance with Different Selection Strategies in Solving TSP”, the World Congress on Engineering 2011, Accessed July 8, 2011
<br>
[2] A.J. Umbarkar1,P.D. Sheth, “Crossover operations in Genetic Algorithm: A Review”, ICTACT journal on soft computing, Accessed October, 2015
<br>
[3] Kusum Deep, Hadush Mebrathu, “Combined Mutation Operators of Genetic Algorithm for the Travelling Salesman Problem”, International Journal of Combinatorial Optimization Problems and Informatics, Accessed December, 2011
</p>

## Project 5: TSP GA with Wisdom of Artificial Crowds

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project5/project5.ipynb)

### Connect with me:

[<img align="left" alt="linkedIn" width="22px" src="https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/assets/icons/linkedin.png" />][linkedin]
[<img align="left" alt="Instagram" width="22px" src="https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/assets/icons/instagram.png" />][instagram]
[<img align="left" alt="gmail" width="22px" src="https://github.com/DSNortsev/CSE545-Artificial-Intelligence/blob/master/assets/icons/gmail.png" />][gmail]

<br />

[instagram]: https://www.instagram.com/dmitry_nortsev/
[linkedin]: https://www.linkedin.com/in/dmitry-nortsev-699975b2/
[gmail]: mailto:dmitry.nortsev@gmail.com
[python]: https://www.python.org/
[jupyter_notebook]: https://jupyter.org/
[git]: https://git-scm.com/book/en/v2
