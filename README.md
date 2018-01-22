Austin Smith
Steven Lee

# assignment_knights_travails_js

Do not go gentle into that good knight.

# Warmup Answers

1. DFS uses a stack for the data structure.

2. BFS uses a queue for the data structure.

3. DFS can be done recursively.

4. BFS would be best suited to print the nodes by depth.

5. Both a tree and graph use nodes and relationships between them, hwoever, a graph does not have a set hierarchy like a tree does.

# Pseudocode

---DFS---

1. Start with the root node and push it into the stack.
2. Pop the last item in the stack and assign it to a variable named "currentNode"
3. For every child node of the currentNode, push it into the stack.
4. Repeat this process for each of the children until a dead end is reached.
5. Go back up to the parent node and access the next child until the desired node is found.

---BFS---

1. Start with the root node and push it into a queue.
2. Shift the first item from the queue and asign it to a variable named "currentNode"
3. Use a loop to go through all the children in the currentNode and push them into the queue.
4. Repeat the previous step until the queue is empty.

---DFS with an Edge List---

1. Start at node 0 and pop it. Mark as visited. Check 0 node's children and put them into the stack.
2. Pop the last item in the stack and check its children.
3. Repeat process until the stack is empty.

---

# Knight's Travails Pseudocode

```
class KnightMove {
  constructor(x, y, depth, children = [], parent = null){
    this.x = x
    this.y = y
    this.depth = depth
    this.children = children
    this.parent = parent
  }
}

class MoveTree {
  constructor(x, y, maxDepth = 1){
    this.begin = new KnightMove(x, y, maxDepth)
    this.maxDepth = maxDepth
    this.moves = []
  }

  possibleMoves(){

    this.moves.push(
      new KnightMove(this.begin.x + 2, this.begin.y + 1, 1, [] , this.begin),

      new KnightMove(this.begin.x + 1, this.begin.y + 2, 1, [] , this.begin),

      new KnightMove(this.begin.x - 2, this.begin.y + 1, 1, [] , this.begin),

      new KnightMove(this.begin.x - 1, this.begin.y + 2, 1, [] , this.begin),

      new KnightMove(this.begin.x - 2, this.begin.y - 1, 1, [] , this.begin),

      new KnightMove(this.begin.x - 1, this.begin.y - 2, 1, [] , this.begin),

      new KnightMove(this.begin.x + 1, this.begin.y - 2, 1, [] , this.begin),

      new KnightMove(this.begin.x + 2, this.begin.y - 1, 1, [] , this.begin),
    )

  }
}
```

# Part I: Tree Builder
