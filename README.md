## 🔹 STL (Standard Template Library) in C++

The **STL** is a powerful library in C++ that provides a set of common classes and functions for handling data structures and algorithms efficiently.

### 📦 Containers – Store Data

| Container           | Description                                |
|---------------------|--------------------------------------------|
| `vector`            | Dynamic array                              |
| `list`              | Doubly linked list                         |
| `deque`             | Double-ended queue                         |
| `stack`             | LIFO structure (usually built over deque)  |
| `queue`             | FIFO structure                             |
| `priority_queue`    | Max-heap or Min-heap                       |
| `set` / `unordered_set` | Store unique elements                |
| `map` / `unordered_map` | Key-value pairs (like dictionaries)   |

Each container serves a specific use case and is optimized for certain types of operations (e.g., fast insertions, random access, ordering, etc.).

---

This project demonstrates the usage of the **Standard Template Library (STL)** in C++. It includes all the major STL components like:

- ✅ Sequence Containers (`vector`, `list`, `deque`)
- ✅ Container Adaptors (`stack`, `queue`, `priority_queue`)
- ✅ Associative Containers (`set`, `map`)
- ✅ Unordered Containers (`unordered_set`, `unordered_map`)
- ✅ Algorithms (`sort`, `find`, `count`, `binary_search`, `accumulate`)
- ✅ Iterators

---

## 🧪 Features Demonstrated

| STL Feature        | Containers/Algorithms Used                  |
|--------------------|----------------------------------------------|
| Sequence           | `vector`, `list`, `deque`                    |
| Adapters           | `stack`, `queue`, `priority_queue`           |
| Associative        | `set`, `map`                                 |
| Unordered          | `unordered_set`, `unordered_map`             |
| Algorithms         | `sort`, `find`, `count`, `accumulate`, `binary_search` |
| Iterators          | `vector::iterator`                           |

---

## Code Example (C++)
---

#include <iostream> <br/>
#include <vector> <br/>
#include <list> <br/>
#include <deque> <br/>
#include <stack> <br/>
#include <queue> <br/>
#include <set> <br/>
#include <map> <br/>
#include <unordered_set> <br/>
#include <unordered_map> <br/>
#include <algorithm> <br/>
#include <numeric> // for accumulate <br/>

using namespace std; <br/>

int main() { <br/>
    cout << "=== VECTOR ===" << endl; <br/>
    vector<int> vec = {5, 1, 4, 2, 3}; <br/>
    sort(vec.begin(), vec.end()); // Sort in ascending order <br/>
    for (int val : vec) cout << val << " "; // 1 2 3 4 5 <br/>
    cout << "\nSum: " << accumulate(vec.begin(), vec.end(), 0) << "\n\n"; // Sum: 15 <br/>

    cout << "=== LIST ===" << endl;
    list<string> fruits = {"Mango", "Apple", "Banana"};
    fruits.push_front("Orange");  // Add at front
    fruits.sort();                // Sort alphabetically
    for (const auto &f : fruits) cout << f << " "; // Apple Banana Mango Orange
    cout << "\n\n";

    cout << "=== DEQUE ===" << endl;
    deque<int> dq;
    dq.push_back(10);
    dq.push_front(20);
    dq.push_back(30);
    for (int x : dq) cout << x << " "; // 20 10 30
    cout << "\n\n";

    cout << "=== STACK ===" << endl;
    stack<int> st;
    st.push(100);
    st.push(200);
    st.push(300);
    while (!st.empty()) {
        cout << st.top() << " "; // 300 200 100 (LIFO)
        st.pop();
    }
    cout << "\n\n";

    cout << "=== QUEUE ===" << endl;
    queue<string> q;
    q.push("C++");
    q.push("Java");
    q.push("Python");
    while (!q.empty()) {
        cout << q.front() << " "; // C++ Java Python (FIFO)
        q.pop();
    }
    cout << "\n\n";

    cout << "=== PRIORITY QUEUE ===" << endl;
    priority_queue<int> pq; // Max heap by default
    pq.push(40);
    pq.push(10);
    pq.push(30);
    while (!pq.empty()) {
        cout << pq.top() << " "; // 40 30 10
        pq.pop();
    }
    cout << "\n\n";

    cout << "=== SET ===" << endl;
    set<int> s = {5, 3, 5, 1, 2}; // Auto-sorted, unique elements only
    for (int x : s) cout << x << " "; // 1 2 3 5
    cout << "\n\n";

    cout << "=== UNORDERED SET ===" << endl;
    unordered_set<int> us = {7, 2, 7, 1, 9}; // Unique, no guaranteed order
    for (int x : us) cout << x << " "; // e.g., 9 2 1 7 (order may vary)
    cout << "\n\n";

    cout << "=== MAP ===" << endl;
    map<string, int> ages;
    ages["Alice"] = 25;
    ages["Bob"] = 30;
    for (auto pair : ages)
        cout << pair.first << ": " << pair.second << endl;
    cout << "\n";

    cout << "=== UNORDERED MAP ===" << endl;
    unordered_map<string, int> scores = {
        {"Math", 90}, {"Physics", 85}, {"Chemistry", 88}};
    for (auto pair : scores)
        cout << pair.first << ": " << pair.second << endl;
    cout << "\n";

    cout << "=== ALGORITHMS (find, count, binary_search) ===" << endl;
    vector<int> data = {10, 20, 30, 40, 50};
    if (find(data.begin(), data.end(), 30) != data.end())
        cout << "30 Found\n"; // Output: 30 Found
    cout << "Count of 20: " << count(data.begin(), data.end(), 20) << "\n"; // Count: 1
    sort(data.begin(), data.end()); // Required before binary_search
    cout << "Binary search for 40: " << binary_search(data.begin(), data.end(), 40) << "\n\n"; // 1 (true)

    cout << "=== ITERATORS ===" << endl;
    vector<int>::iterator it;
    for (it = vec.begin(); it != vec.end(); ++it)
        cout << *it << " "; // 1 2 3 4 5 (using iterator)
    cout << "\n";

    return 0;
}

---
Output Link: https://www.programiz.com/online-compiler/52EMcWy21fHpk


