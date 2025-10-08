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


