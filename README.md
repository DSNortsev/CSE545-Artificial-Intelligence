# CSE545-Artificial-Intelligence

In this course we will be solving The Travelling Salesman Problems (TSP) with different algorithms. 

---

## List of projects:

- [Project 1: TSP with Brute Force](#project-1-tsp-with-brute-force)
- [Project 2: TSP search with BFS and DFS](#project-2-tsp-search-with-bfs-and-dfs)
- [Project 3: TSP with Closest Edge Insertion Heuristic](#project-3-tsp-with-closest-edge-insertion-heuristic)
- [Project 4: TSP with Genetic Algorithm](#project-4-tsp-with-genetic-algorithm)


## Project 1: TSP with Brute Force

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DSNortsev/CSE545-Artificial-Intelligence/blob/master/Project1/project1.ipynb)

### Introduction
<p align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;In this project we will review The Travelling Salesman Problem (TSP). The TSP is a problem in Computer Science used to demonstrate intractability and optimization. In short, imagine a salesman who wishes to visit every one of N cities exactly once each. For salesman it does not matter which order he visits the cities as he is equally proficient in applying is selling skills in them all regardless. All that matters is that he takes the shortest route between them all before returning back to the start. This kind of problem is also known as Hamiltonian Cycle to find the minimum weight. 
<br></br>
&nbsp;&nbsp;&nbsp;&nbsp;We would run python code that would demonstarte a TSP simulation and attempt to solve the problem by Brute Force. The Brute Force algorithms is a straightforward method of solving a problem that rely on sheer computer power that will go through all possible solution extensively. A Brute Force solution is 100% possible for only 25 cities which is approximately 15.5 septillion unique permutation, which would make it impossible to find the global optimal solution for large dataset 
<br></br>
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

## Project 3: TSP with Closest Edge Insertion Heuristic

## Project 4: TSP with Genetic Algorithm



## Support

Reach out to me at one of the following places!

- LinkedIn at <a href="https://www.linkedin.com/in/dmitry-nortsev-699975b2/" target="_blank">`@dmitry_nortsev`</a>
- Email to [dmitry.nortsev@gmail.com](mailto:dmitry.nortsev@gmail.com)
