---
date: 1717420992.719196
tags:
- autogenerated
- source__oai
- conversation_id__cde9c00e-cdff-4efa-abc5-d00424dfb6d3
- msg_1e8fd660-7be5-4bc1-abaa-8f56e445788c
- msg_861ede02-7673-4f68-8a26-cae226485bb9
- colorclass/vector-space
title: demonstrate a minimal hnsw implementation in python
---

**USER**

Demonstrate a minimal hnsw implementation in python


**ASSISTANT**

Here's a minimal implementation of the Hierarchical Navigable Small World (HNSW) algorithm in Python. This example will focus on the core concepts and basic functionality rather than performance optimization.

```python
import random
import math
import heapq
from collections import defaultdict
import numpy as np

class HNSW:
    def __init__(self, max_elements, M=16, ef_construction=200):
        self.max_elements = max_elements
        self.M = M
        self.ef_construction = ef_construction
        self.levels = {}
        self.entry_point = None
        self.distances = {}
        
    def _distance(self, x, y):
        return np.linalg.norm(x - y)
        
    def _get_random_level(self):
        return int(-math.log(random.random()) * self.M)
        
    def _search_layer(self, q, ep, level, ef):
        visited = set()
        candidates = [(self._distance(q, ep), ep)]
        heapq.heapify(candidates)
        results = []
        while candidates:
            dist, curr_node = heapq.heappop(candidates)
            if curr_node in visited:
                continue
            visited.add(curr_node)
            if len(results) < ef:
                heapq.heappush(results, (-dist, curr_node))
            else:
                if dist < -results[0][0]:
                    heapq.heappop(results)
                    heapq.heappush(results, (-dist, curr_node))
                else:
                    break
            for neighbor in self.levels[level][curr_node]:
                if neighbor not in visited:
                    heapq.heappush(candidates, (self._distance(q, neighbor), neighbor))
        return [node for _, node in results]

    def add_point(self, data_point, id):
        level = self._get_random_level()
        self.distances[id] = data_point
        if not self.entry_point:
            self.entry_point = id
            self.levels[0] = {id: []}
            for l in range(1, level + 1):
                self.levels[l] = {id: []}
            return
        
        curr_ep = self.entry_point
        for l in range(max(self.levels.keys()), level, -1):
            curr_ep = self._search_layer(data_point, curr_ep, l, 1)[0]
        
        for l in range(min(level, max(self.levels.keys())) + 1):
            neighbors = self._search_layer(data_point, curr_ep, l, self.ef_construction)
            self.levels[l][id] = neighbors
            for neighbor in neighbors:
                self.levels[l][neighbor].append(id)
                if len(self.levels[l][neighbor]) > self.M:
                    self.levels[l][neighbor] = sorted(self.levels[l][neighbor], 
                                                      key=lambda x: self._distance(self.distances[neighbor], self.distances[x]))[:self.M]
        for l in range(level + 1, max(self.levels.keys()) + 1):
            self.levels[l][id] = []

    def search(self, q, k=1):
        curr_ep = self.entry_point
        for l in range(max(self.levels.keys()), 0, -1):
            curr_ep = self._search_layer(q, curr_ep, l, 1)[0]
        return self._search_layer(q, curr_ep, 0, k)

# Example usage
hnsw = HNSW(max_elements=1000)

# Add some points
points = [np.random.rand(2) for _ in range(100)]
for i, point in enumerate(points):
    hnsw.add_point(point, i)

# Search for nearest neighbors of a random point
query_point = np.random.rand(2)
neighbors = hnsw.search(query_point, k=3)
print("Nearest neighbors:", neighbors)
```

### Explanation

1. **Initialization (`__init__`)**: Initializes the HNSW with parameters for the maximum number of elements, the maximum number of connections per layer (`M`), and the size of the dynamic list for nearest neighbor candidates during construction (`ef_construction`).

2. **Distance Calculation (`_distance`)**: Uses Euclidean distance for measuring similarity between points.

3. **Random Level Generation (`_get_random_level`)**: Determines the level of each point using a geometric distribution.

4. **Search Layer (`_search_layer`)**: Searches for nearest neighbors within a specific layer. This function


---

preceding: [[hnsw]]  


following: [[relationship between edge contraction on a graph and tensor contraction operations]]

See also: [[tensor contraction]]