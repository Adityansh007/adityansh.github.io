#Adityansh
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
<title>DSA Topics Explained</title>
<style>
  /* Reset and base */
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0; padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #f5f7fa;
    color: #333;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  header {
    background-color: #2c3e50;
    color: #ecf0f1;
    padding: 15px 20px;
    font-size: 1.8rem;
    font-weight: 700;
    text-align: center;
    box-shadow: 0 3px 6px rgba(0,0,0,0.1);
  }
  .container {
    display: flex;
    flex: 1;
    overflow: hidden;
  }
  nav {
    background: #34495e;
    color: white;
    width: 220px;
    min-width: 180px;
    overflow-y: auto;
    flex-shrink: 0;
  }
  nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  nav li {
    border-bottom: 1px solid #2c3e50;
  }
  nav button {
    background: none;
    border: none;
    width: 100%;
    padding: 15px 20px;
    font-size: 1rem;
    color: inherit;
    text-align: left;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  nav button:hover,
  nav button.active {
    background-color: #1abc9c;
    color: #fff;
  }
  main {
    flex-grow: 1;
    padding: 25px 30px;
    overflow-y: auto;
    scroll-behavior: smooth;
    background: white;
  }
  h2 {
    border-bottom: 3px solid #1abc9c;
    padding-bottom: 6px;
    margin: 0 0 20px 0;
    font-weight: 700;
    font-size: 1.7rem;
  }
  section {
    margin-bottom: 40px;
  }
  pre {
    background-color: #ecf0f1;
    border-radius: 6px;
    padding: 15px;
    font-size: 0.9rem;
    line-height: 1.4;
    overflow-x: auto;
    font-family: 'Source Code Pro', monospace, monospace;
    user-select: text;
  }
  code {
    font-family: 'Source Code Pro', monospace, monospace;
  }
  .algo-title {
    font-size: 1.1rem;
    font-weight: 600;
    margin-top: 15px;
    margin-bottom: 8px;
    color: #16a085;
  }

  /* Responsive styles */
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
    }
    nav {
      width: 100%;
      max-height: 160px;
      overflow-x: auto;
      overflow-y: hidden;
      white-space: nowrap;
      border-bottom: 1px solid #ddd;
    }
    nav ul {
      display: flex;
      flex-wrap: nowrap;
    }
    nav li {
      flex: 0 0 auto;
      border-bottom: none;
      border-right: 1px solid #2c3e50;
    }
    nav button {
      padding: 12px 16px;
      font-size: 0.9rem;
    }
    main {
      padding: 15px 20px;
      flex-grow: 1;
    }
  }
  @media (max-width: 400px) {
    header {
      font-size: 1.5rem;
      padding: 12px 10px;
    }
    nav button {
      padding: 10px 12px;
      font-size: 0.85rem;
    }
  }
</style>
</head>
<body>
<header>DSA Explained</header>
<div class="container">
  <nav aria-label="DSA topic navigation">
    <ul id="topics-nav">
      <li><button class="active" data-target="arrays">Arrays</button></li>
      <li><button data-target="linkedlists">Linked Lists</button></li>
      <li><button data-target="stacks">Stacks</button></li>
      <li><button data-target="queues">Queues</button></li>
      <li><button data-target="trees">Trees</button></li>
      <li><button data-target="graphs">Graphs</button></li>
      <li><button data-target="sorting">Sorting Algorithms</button></li>
      <li><button data-target="searching">Searching Algorithms</button></li>
      <li><button data-target="hashing">Hashing</button></li>
      <li><button data-target="dp">Dynamic Programming</button></li>
    </ul>
  </nav>
  <main>
    <section id="arrays" tabindex="0">
      <h2>Arrays</h2>
      <p>An array is a collection of items stored at contiguous memory locations. It allows fast access using indices.</p>
      <h3 class="algo-title">Syntax (C++):</h3>
      <pre><code>int arr[5];            // Declaration of array with 5 integers
int arr[] = {1, 2, 3};  // Initialization of array</code></pre>
      <h3 class="algo-title">Traversal Algorithm:</h3>
      <pre><code>for (int i = 0; i &lt; n; i++) {
    // Access arr[i]
}</code></pre>
    </section>

    <section id="linkedlists" tabindex="0">
      <h2>Linked Lists</h2>
      <p>A linked list consists of nodes where each node contains data and a pointer to the next node.</p>
      <h3 class="algo-title">Node Structure (C++):</h3>
      <pre><code>struct Node {
    int data;
    Node* next;
};</code></pre>
      <h3 class="algo-title">Traversal Algorithm:</h3>
      <pre><code>Node* curr = head;
while (curr != nullptr) {
    // Process curr->data
    curr = curr->next;
}</code></pre>
    </section>

    <section id="stacks" tabindex="0">
      <h2>Stacks</h2>
      <p>Stack is a LIFO data structure where elements are added and removed from the top.</p>
      <h3 class="algo-title">Using STL stack (C++):</h3>
      <pre><code>#include &lt;stack&gt;
std::stack&lt;int&gt; s;
s.push(10);  // Push element
s.pop();     // Pop element</code></pre>
      <h3 class="algo-title">Operations:</h3>
      <pre><code>push(x)    // Insert element x
pop()       // Remove top element
top()       // Access top element
empty()     // Check if empty</code></pre>
    </section>

    <section id="queues" tabindex="0">
      <h2>Queues</h2>
      <p>Queue is a FIFO data structure where elements are added at the rear and removed from the front.</p>
      <h3 class="algo-title">Using STL queue (C++):</h3>
      <pre><code>#include &lt;queue&gt;
std::queue&lt;int&gt; q;
q.push(10);  // Enqueue
q.pop();     // Dequeue</code></pre>
      <h3 class="algo-title">Operations:</h3>
      <pre><code>enqueue(x)   // Add element x
dequeue()     // Remove front element
front()       // Access front element
empty()       // Check if empty</code></pre>
    </section>

    <section id="trees" tabindex="0">
      <h2>Trees</h2>
      <p>Trees are hierarchical data structures with nodes having children, starting from a root node.</p>
      <h3 class="algo-title">Binary Tree Node (C++):</h3>
      <pre><code>struct Node {
    int data;
    Node* left;
    Node* right;
};</code></pre>
      <h3 class="algo-title">Inorder Traversal Algorithm:</h3>
      <pre><code>void inorder(Node* root) {
    if (!root) return;
    inorder(root->left);
    // Process root->data
    inorder(root->right);
}</code></pre>
    </section>

    <section id="graphs" tabindex="0">
      <h2>Graphs</h2>
      <p>Graphs consist of nodes (vertices) connected by edges; they can be directed or undirected.</p>
      <h3 class="algo-title">Adjacency List (C++):</h3>
      <pre><code>std::vector&lt;std::vector&lt;int&gt;&gt; adj(n);
adj[u].push_back(v);  // Edge u -> v</code></pre>
      <h3 class="algo-title">Breadth First Search (BFS) Algorithm:</h3>
      <pre><code>std::queue&lt;int&gt; q;
std::vector&lt;bool&gt; visited(n, false);
q.push(start);
visited[start] = true;

while (!q.empty()) {
    int u = q.front(); q.pop();
    // Process u
    for (auto v : adj[u]) {
        if (!visited[v]) {
            visited[v] = true;
            q.push(v);
        }
    }
}</code></pre>
    </section>

    <section id="sorting" tabindex="0">
      <h2>Sorting Algorithms</h2>
      <p>Sorting arranges elements in order. Common algorithms include Bubble Sort, Merge Sort, Quick Sort.</p>
      <h3 class="algo-title">Bubble Sort (O(n²)):</h3>
      <pre><code>for (int i = 0; i &lt; n-1; i++) {
    for (int j = 0; j &lt; n-1-i; j++) {
        if (arr[j] &gt; arr[j+1]) {
            std::swap(arr[j], arr[j+1]);
        }
    }
}</code></pre>
      <h3 class="algo-title">Merge Sort (O(n log n)):</h3>
      <pre><code>void mergeSort(int arr[], int l, int r);
void merge(int arr[], int l, int m, int r);</code></pre>
      <p>Recursively split and merge sorted subarrays.</p>
      <h3 class="algo-title">Quick Sort (O(n log n) avg):</h3>
      <pre><code>int partition(int arr[], int low, int high);
void quickSort(int arr[], int low, int high);</code></pre>
      <p>Partition array around pivot and recursively sort subarrays.</p>
    </section>

    <section id="searching" tabindex="0">
      <h2>Searching Algorithms</h2>
      <p>Algorithms to find data. Includes Linear and Binary Search.</p>
      <h3 class="algo-title">Linear Search (O(n)):</h3>
      <pre><code>for (int i = 0; i &lt; n; i++) {
    if (arr[i] == target) return i;
}
return -1;</code></pre>
      <h3 class="algo-title">Binary Search (O(log n)) (Sorted Array):</h3>
      <pre><code>int low = 0, high = n - 1;
while (low &lt;= high) {
    int mid = low + (high - low) / 2;
    if (arr[mid] == target) return mid;
    else if (arr[mid] &lt; target) low = mid + 1;
    else high = mid - 1;
}
return -1;</code></pre>
    </section>

    <section id="hashing" tabindex="0">
      <h2>Hashing</h2>
      <p>Hashes map keys to indices in a table for efficient lookup.</p>
      <h3 class="algo-title">Syntax (C++ STL unordered_map):</h3>
      <pre><code>#include &lt;unordered_map&gt;
std::unordered_map&lt;int, std::string&gt; hashmap;
hashmap[1] = "one";
auto it = hashmap.find(1);
if (it != hashmap.end()) {
    // Found
}</code></pre>
      <h3 class="algo-title">Concept:</h3>
      <pre><code>key --hash_function--> index in hash table
Store/retrieve data at that index</code></pre>
    </section>

    <section id="dp" tabindex="0">
      <h2>Dynamic Programming (DP)</h2>
      <p>DP solves problems by combining solutions to overlapping subproblems, storing results to avoid recomputation.</p>
      <h3 class="algo-title">Example: Fibonacci (Memoization):</h3>
      <pre><code>int fib(int n, std::vector&lt;int&gt;&amp; memo) {
    if (n &lt;= 1) return n;
    if (memo[n] != -1) return memo[n];
    memo[n] = fib(n-1, memo) + fib(n-2, memo);
    return memo[n];
}</code></pre>
      <h3 class="algo-title">Example: Fibonacci (Tabulation):</h3>
      <pre><code>int fib(int n) {
    std::vector&lt;int&gt; dp(n+1);
    dp[0] = 0; dp[1] = 1;
    for (int i = 2; i &lt;= n; i++) {
        dp[i] = dp[i-1] + dp[i-2];
    }
    return dp[n];
}</code></pre>
    </section>
  </main>
</div>
<script>
  // Navigation buttons
  const navButtons = document.querySelectorAll('nav button');
  const sections = document.querySelectorAll('main section');

  function clearActive() {
    navButtons.forEach(btn => btn.classList.remove('active'));
  }

  navButtons.forEach(btn => {
    btn.addEventListener('click', () => {
      clearActive();
      btn.classList.add('active');
      const target = btn.getAttribute('data-target');
      const section = document.getElementById(target);
      if (section) {
        section.scrollIntoView({behavior: 'smooth', block: 'start'});
        section.focus({preventScroll: true});
      }
    });
  });

  window.addEventListener('scroll', () => {
    const scrollPos = window.scrollY + 100;
    let current = '';
    sections.forEach(section => {
      if (scrollPos >= section.offsetTop) {
        current = section.id;
      }
    });
    if (current) {
      clearActive();
      const activeBtn = document.querySelector(`nav button[data-target="${current}"]`);
      if (activeBtn) activeBtn.classList.add('active');
    }
  });
</script>
</body>
</html>
