---

🧭 Dijkstra’s Algorithm

Objective

To find the shortest distance from a given source vertex S to all other vertices in a weighted, connected, and non-negative graph.


---

Algorithm Type

Greedy Algorithm

Uses Priority Queue / Min Heap

Works only with non-negative edge weights



---

Algorithm Steps

Let V = number of vertices and E = number of edges.


---

Step 1: Initialization

1. Create a distance array dist[V] and initialize all distances as infinity (1e9), except the source vertex S, which is set to 0.


2. Use a Min Heap (Priority Queue or Set) to always pick the vertex with the smallest current distance.




---

Step 2: Processing Vertices

While the priority queue is not empty:

1. Extract the vertex u having the smallest distance (dist[u]).


2. Traverse all adjacent vertices v of u.


3. If dist[u] + weight(u, v) < dist[v], then update:

dist[v] = dist[u] + weight(u, v)

and push (dist[v], v) into the min heap.




---

Step 3: Termination

When all vertices are processed (priority queue becomes empty),
the array dist[] contains the shortest distances from the source vertex S to all other vertices.


---

Example

Input:

V = 2, E = 1
0 1 9
S = 0

Output:

0 9

Explanation:

Distance from source vertex 0 to itself = 0

Distance from vertex 0 to vertex 1 = 9



---

Complexity Analysis

Aspect	Complexity

Time Complexity	O((V + E) × log V)
Space Complexity	O(V)



---

🧩 Proof of Time Complexity

Let’s break it down step by step.

1️⃣ Building the Min Heap

Initially, we insert the source vertex into the heap → O(log V).

2️⃣ Each Vertex Extraction

Each vertex (V times) is extracted from the heap once.
Each extraction operation costs O(log V).

So,

Total for all vertex extractions = V × O(log V)

3️⃣ Edge Relaxations

Each edge (E total) may cause at most one decrease-key or insertion operation into the heap,
which also takes O(log V) time per operation.

So,

Total for edge relaxations = E × O(log V)


---

4️⃣ Combining All Operations

Therefore,

Total Time = O(V × log V) + O(E × log V)

Simplifying:

O((V + E) × log V)


---

Alternative Explanation (Expanded Form)

For each vertex v, we:

Pop one vertex from the heap → O(log V)

Push its adjacent edges into the heap → up to (degree of v) pushes, each O(log V)


Hence:

Σ [ O(log V) + (deg(v) × O(log V)) ]  for all v in V

Since the sum of all degrees = 2E (each edge counted twice):

O((V + E) × log V)


---

5️⃣ Space Complexity Proof

dist[] array → O(V)

priority_queue / set → can hold up to V elements → O(V)

Adjacency list representation → O(V + E)


Hence total:

O(V + E) ≈ O(V)

(for sparse graphs, E ≈ V)


---

✅ Final Result

Metric	Complexity

Time Complexity	O((V + E) log V)
Space Complexity	O(V)
Applicable To	Weighted graphs with non-negative edges



---



## 🧩 Problem Description

You are given a **weighted**, **undirected**, and **connected** graph with **V** vertices and **E** edges.
Your task is to find the **shortest distance** from a given **source vertex S** to all other vertices in the graph.

Each edge of the graph has a **positive weight**, and there are **no negative weight cycles**.

---

### Input Format

* The first line contains two integers `V` and `E`,
  representing the number of vertices and edges in the graph.
* The next `E` lines contain three integers `u`, `v`, and `w`,
  representing an undirected edge between vertex `u` and vertex `v` with weight `w`.
* The last line contains the source vertex `S`.

---

### Output Format

Print the shortest distance from the source vertex `S` to all vertices `0` to `V-1`.

---

### Constraints

* 1 ≤ V ≤ 1000
* 1 ≤ E ≤ (V × (V - 1)) / 2
* 0 ≤ u, v < V
* 1 ≤ w ≤ 10⁵

---

### Example

**Input:**

```
2 1
0 1 9
0
```

**Output:**

```
0 9
```

**Explanation:**
There are 2 vertices (0 and 1) and 1 edge between them with weight 9.
The shortest distance from vertex 0 to itself is 0, and to vertex 1 is 9.

---

## ✅ C++ Solution (Dijkstra’s Algorithm)

```cpp
#include <bits/stdc++.h>
using namespace std;

class Solution {
public:
    // Function to find the shortest distance of all the vertices from the source vertex S.
    vector<int> dijkstra(int V, vector<vector<int>> adj[], int S) {
        // Min-heap to store {distance, node}
        priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;

        // Initialize all distances as infinity
        vector<int> dist(V, 1e9);

        // Distance from source to itself is 0
        dist[S] = 0;
        pq.push({0, S});

        while (!pq.empty()) {
            int dis = pq.top().first;
            int node = pq.top().second;
            pq.pop();

            // Traverse all adjacent nodes
            for (auto it : adj[node]) {
                int adjNode = it[0];
                int edgeWeight = it[1];

                if (dis + edgeWeight < dist[adjNode]) {
                    dist[adjNode] = dis + edgeWeight;
                    pq.push({dist[adjNode], adjNode});
                }
            }
        }

        return dist;
    }
};

int main() {
    int V, E;
    cin >> V >> E;

    vector<vector<int>> adj[V];

    for (int i = 0; i < E; i++) {
        int u, v, w;
        cin >> u >> v >> w;
        adj[u].push_back({v, w});
        adj[v].push_back({u, w}); // because the graph is undirected
    }

    int S;
    cin >> S;

    Solution obj;
    vector<int> result = obj.dijkstra(V, adj, S);

    for (int d : result) {
        cout << d << " ";
    }
    cout << endl;

    return 0;
}
```

---



---

## 🧩 Problem Description

You are given a **weighted**, **undirected**, and **connected** graph consisting of `V` vertices and `E` edges.
Your task is to **find the shortest distance of all vertices from a given source vertex S**.

> **Note:** The graph does not contain any negative weight cycles.

---

### Input Format

* The first line contains two integers `V` and `E`,
  representing the number of vertices and the number of edges.
* The next `E` lines each contain three integers `u`, `v`, and `w`,
  representing an undirected edge between vertex `u` and vertex `v` with weight `w`.
* The last line contains the source vertex `S`.

---

### Output Format

Print the shortest distance from the source vertex `S` to all other vertices in a single line, separated by spaces.

---

### Constraints

* 1 ≤ V ≤ 1000
* 1 ≤ E ≤ (V × (V - 1)) / 2
* 0 ≤ u, v < V
* 1 ≤ w ≤ 10⁵
* 0 ≤ S < V

---

### Example 1

**Input:**

```
2 1
0 1 9
0
```

**Output:**

```
0 9
```

**Explanation:**
Make the weighted graph:

```
Source:      0
Weight:      9
Destination: 1
```

The source vertex is 0.
Hence, the shortest distance of node 0 is 0, and the shortest distance to node 1 is 9.

---

## ✅ C++ Code (Using Set for Dijkstra’s Algorithm)

```cpp
#include <bits/stdc++.h>
using namespace std;

class Solution {
public:
    // Function to find the shortest distance of all the vertices from the source vertex S.
    vector<int> dijkstra(int V, vector<vector<int>> adj[], int S) {
        // Set stores pairs {distance, node}
        set<pair<int, int>> st;
        vector<int> dist(V, 1e9);

        // Initialize source vertex distance
        dist[S] = 0;
        st.insert({0, S});

        while (!st.empty()) {
            auto it = *(st.begin());
            int dis = it.first;
            int node = it.second;
            st.erase(it);

            // Traverse all adjacent nodes
            for (auto edge : adj[node]) {
                int adjNode = edge[0];
                int edgeWeight = edge[1];

                if (dis + edgeWeight < dist[adjNode]) {
                    // If a shorter path is found, update and erase the older one if present
                    if (dist[adjNode] != 1e9) {
                        st.erase({dist[adjNode], adjNode});
                    }
                    dist[adjNode] = dis + edgeWeight;
                    st.insert({dist[adjNode], adjNode});
                }
            }
        }

        return dist;
    }
};

int main() {
    int V, E;
    cin >> V >> E;

    vector<vector<int>> adj[V];
    for (int i = 0; i < E; i++) {
        int u, v, w;
        cin >> u >> v >> w;
        adj[u].push_back({v, w});
        adj[v].push_back({u, w}); // Undirected graph
    }

    int S;
    cin >> S;

    Solution obj;
    vector<int> result = obj.dijkstra(V, adj, S);

    for (int d : result)
        cout << d << " ";
    cout << endl;

    return 0;
}
```



---

🧩 Problem Description

Shortest Path in Weighted Undirected Graph

Difficulty: Medium
Accuracy: 50.0%
Points: 4


---

Problem Statement

You are given a weighted undirected graph having n vertices and m edges, where each edge connects two vertices a and b with a given weight w.

Your task is to find the shortest path from vertex 1 to vertex n.
If there is no path from vertex 1 to vertex n, return a list consisting of only -1.


---

Input Format

n: number of vertices

m: number of edges

edges: a vector of m edges, where each edge is represented as [a, b, w]



---

Output Format

Return a vector representing the sequence of vertices forming the shortest path from 1 to n.
If no such path exists, return [-1].


---

Constraints

1 ≤ n ≤ 10⁵

1 ≤ m ≤ 2 × 10⁵

1 ≤ a, b ≤ n

1 ≤ w ≤ 10⁵



---

Example

Input:

n = 5, m = 6
edges = [[1,2,2], [2,5,5], [2,3,4], [1,4,1], [4,3,3], [3,5,1]]

Output:

1 4 3 5

Explanation:
The shortest path from vertex 1 to vertex 5 is:
1 → 4 → 3 → 5
with total weight = 1 + 3 + 1 = 5.


---

Your Task

You don’t need to read input or print anything.
Your task is to complete the function shortestPath(), which takes:

an integer n (number of vertices),

an integer m (number of edges),

and a vector of vectors edges,


and returns a vector containing the shortest path from vertex 1 to vertex n.
If the path does not exist, return {-1}.


---

Expected Time Complexity:

O(m * log n)

Expected Space Complexity:

O(n)


---

✅ C++ Solution

#include <bits/stdc++.h>
using namespace std;

class Solution {
public:
    vector<int> shortestPath(int n, int m, vector<vector<int>>& edges) {
        // Step 1: Create adjacency list
        vector<pair<int, int>> adj[n + 1];
        for (auto it : edges) {
            int u = it[0];
            int v = it[1];
            int w = it[2];
            adj[u].push_back({v, w});
            adj[v].push_back({u, w});
        }

        // Step 2: Min-heap for Dijkstra (distance, node)
        priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;

        // Step 3: Distance and parent initialization
        vector<int> dist(n + 1, 1e9);
        vector<int> parent(n + 1);
        for (int i = 1; i <= n; i++) parent[i] = i;

        dist[1] = 0;
        pq.push({0, 1});

        // Step 4: Dijkstra's algorithm
        while (!pq.empty()) {
            auto it = pq.top();
            pq.pop();

            int dis = it.first;
            int node = it.second;

            for (auto edge : adj[node]) {
                int adjNode = edge.first;
                int edgeWeight = edge.second;

                if (dis + edgeWeight < dist[adjNode]) {
                    dist[adjNode] = dis + edgeWeight;
                    parent[adjNode] = node;
                    pq.push({dist[adjNode], adjNode});
                }
            }
        }

        // Step 5: If no path exists
        if (dist[n] == 1e9) return {-1};

        // Step 6: Build path from 1 → n
        vector<int> path;
        int node = n;
        while (parent[node] != node) {
            path.push_back(node);
            node = parent[node];
        }
        path.push_back(1);
        reverse(path.begin(), path.end());

        return path;
    }
};

int main() {
    int n = 5, m = 6;
    vector<vector<int>> edges = {
        {1, 2, 2},
        {2, 5, 5},
        {2, 3, 4},
        {1, 4, 1},
        {4, 3, 3},
        {3, 5, 1}
    };

    Solution obj;
    vector<int> ans = obj.shortestPath(n, m, edges);

    for (int x : ans) cout << x << " ";
    cout << endl;

    return 0;
}


---

✅ Output

1 4 3 5


---


