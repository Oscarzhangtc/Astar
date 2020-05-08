
# Astar GUI

This a GUI that implements the Astar graph traversal and path search algorithm with pygame. It tells the story of PAUL, who strives to find his path to the cake.


**About the Map**

![map](/readme/swamps.png)

Lava nodes: nodes that are impossible to step on and cross directly.
Swamps nodes: nodes that can be step on by Paul but it will cost more points(3).
The cake: Pauls ultimate destination.


**About Paul**

Paul can go Diagonal

![diagonal](/readme/diagonal.png)

Paul can move diagonally when he finds it impossible to move cardinality. Even though it
costs more points(3) to move diagonally it is worth it for Paul in many cases that it would take 2
cardinal steps to cover a diagonal step. That actually 1 step is indeed worth it when paul can not
move to the destination cardinally.


Paul Jumps

![jumps](/readme/jump.png)

Paul jumps! It is Paul's most impressive ability that he can now pass through lava nodes
that are previously unpassable. Even though a jump would cost Paul 6 steps, Paul will do
whatever it takes to get to the cake. Because of that and Paul’s new abilities, now the cost will
NEVER return none.

**A star**
Paul will do whatever it takes to get the cake with the help of [A*](http://web.mit.edu/eranki/www/tutorials/search/) search algorithm. Paul the finds the fastest and least costly path to the cake.


# Costs and Point Systems
By uncommenting different type of cost under the draw function will yield different effects.

**With nothing uncommented**

![nothinguncommented](/readme/nothinguncommented.jpg)

Pauls finds the best path to the cake, avoiding the lava nodes.


**g-score**

![g_cost](/readme/g_cost)

With Self.g_cost uncommented.
G_score is the total number of points it takes for Paul to reach the cake. The g-score equals the
number of steps since each node is 1 point.


**h-score**

![g_cost](/readme/h_cost)

H_cost or h-score calculates the reverse of g-score where it is the total number of points it
takes from the final destination to paul similar displays none is paul can't be reached from cake.


**h-score**

![h_cost](/readme/h_cost.png)

H_cost or h-score calculates the reverse of g-score where it is the total number of points it
takes from the final destination to paul similar displays none is paul can't be reached from cake.


**f-score**

![f_cost](/readme/f_cost.png)

F-score is displayed only when the cost(points required) is bigger than 18(the minimum number
of moves Paul requires to reach the cake). Each node is coded with its costs, while the lava
nodes the path is no longer the only factor that impacts Paul's choice of path.


# Installation and Guide

Also install pygame to run the GUI.
```bash
$ pip install pygame
```

Then simply start the GUI with:
```bash
$ python astar.py
```

A GUI window will spin up.

**Instructions**
To use this astar GUI/toy, hit the 'l' key to switch to the 'add lava tiles' mode. Then you can click on any cell to add or remove a lava tile from that cell. Hit the spacebar at any time to have Paul plan (or replan) his path, and highlight that path. The cost of the your choice will then be logged.
