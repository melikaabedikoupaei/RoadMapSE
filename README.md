# RoadMapSE
##https://github.com/HadiEsna/coding-interview-university#dont-feel-you-arent-smart-enough

this my roadmap to become software engineer
1-Data Structures and Algorithms in Python
2-Cracking the Coding Interview: 189 Programming Questions and Solutions
Let's Get Started
Alright, enough talk, let's learn!

But don't forget to do coding problems from above while you learn!

Algorithmic complexity / Big-O / Asymptotic analysis
Nothing to implement here, you're just watching videos and taking notes! Yay!
There are a lot of videos here. Just watch enough until you understand it. You can always come back and review.
Don't worry if you don't understand all the math behind it.
You just need to understand how to express the complexity of an algorithm in terms of Big-O.
 Harvard CS50 - Asymptotic Notation (video)
 Big O Notations (general quick tutorial) (video)
 Big O Notation (and Omega and Theta) - best mathematical explanation (video)
 Skiena (video)
 UC Berkeley Big O (video)
 Amortized Analysis (video)
 TopCoder (includes recurrence relations and master theorem):
Computational Complexity: Section 1
Computational Complexity: Section 2
 Cheat sheet
 [Review] Big-O notation in 5 minutes (video)
Well, that's about enough of that.

When you go through "Cracking the Coding Interview", there is a chapter on this, and at the end there is a quiz to see if you can identify the runtime complexity of different algorithms. It's a super review and test.

Data Structures
Arrays
 About Arrays:
Arrays CS50 Harvard University
Arrays (video)
UC Berkeley CS61B - Linear and Multi-Dim Arrays (video) (Start watching from 15m 32s)
Dynamic Arrays (video)
Jagged Arrays (video)
 Implement a vector (mutable array with automatic resizing):
 Practice coding using arrays and pointers, and pointer math to jump to an index instead of using indexing.
 New raw data array with allocated memory
can allocate int array under the hood, just not use its features
start with 16, or if starting number is greater, use power of 2 - 16, 32, 64, 128
 size() - number of items
 capacity() - number of items it can hold
 is_empty()
 at(index) - returns item at given index, blows up if index out of bounds
 push(item)
 insert(index, item) - inserts item at index, shifts that index's value and trailing elements to the right
 prepend(item) - can use insert above at index 0
 pop() - remove from end, return value
 delete(index) - delete item at index, shifting all trailing elements left
 remove(item) - looks for value and removes index holding it (even if in multiple places)
 find(item) - looks for value and returns first index with that value, -1 if not found
 resize(new_capacity) // private function
when you reach capacity, resize to double the size
when popping an item, if size is 1/4 of capacity, resize to half
 Time
O(1) to add/remove at end (amortized for allocations for more space), index, or update
O(n) to insert/remove elsewhere
 Space
contiguous in memory, so proximity helps performance
space needed = (array capacity, which is >= n) * size of item, but even if 2n, still O(n)
Linked Lists
 Description:
 Linked Lists CS50 Harvard University - this builds the intuition.
 Singly Linked Lists (video)
 CS 61B - Linked Lists 1 (video)
 CS 61B - Linked Lists 2 (video)
 [Review] Linked lists in 4 minutes (video)
 C Code (video) - not the whole video, just portions about Node struct and memory allocation
 Linked List vs Arrays:
Core Linked Lists Vs Arrays (video)
In The Real World Linked Lists Vs Arrays (video)
 Why you should avoid linked lists (video)
 Gotcha: you need pointer to pointer knowledge: (for when you pass a pointer to a function that may change the address where that pointer points) This page is just to get a grasp on ptr to ptr. I don't recommend this list traversal style. Readability and maintainability suffer due to cleverness.
Pointers to Pointers
 Implement (I did with tail pointer & without):
 size() - returns number of data elements in list
 empty() - bool returns true if empty
 value_at(index) - returns the value of the nth item (starting at 0 for first)
 push_front(value) - adds an item to the front of the list
 pop_front() - remove front item and return its value
 push_back(value) - adds an item at the end
 pop_back() - removes end item and returns its value
 front() - get value of front item
 back() - get value of end item
 insert(index, value) - insert value at index, so current item at that index is pointed to by new item at index
 erase(index) - removes node at given index
 value_n_from_end(n) - returns the value of the node at nth position from the end of the list
 reverse() - reverses the list
 remove_value(value) - removes the first item in the list with this value
 Doubly-linked List
Description (video)
No need to implement
Stack
 Stacks (video)
 [Review] Stacks in 3 minutes (video)
 Will not implement. Implementing with array is trivial
Queue
 Queue (video)
 Circular buffer/FIFO
 [Review] Queues in 3 minutes (video)
 Implement using linked-list, with tail pointer:
enqueue(value) - adds value at position at tail
dequeue() - returns value and removes least recently added element (front)
empty()
 Implement using fixed-sized array:
enqueue(value) - adds item at end of available storage
dequeue() - returns value and removes least recently added element
empty()
full()
 Cost:
a bad implementation using linked list where you enqueue at head and dequeue at tail would be O(n) because you'd need the next to last element, causing a full traversal each dequeue
enqueue: O(1) (amortized, linked list and array [probing])
dequeue: O(1) (linked list and array)
empty: O(1) (linked list and array)
Hash table
 Videos:

 Hashing with Chaining (video)
 Table Doubling, Karp-Rabin (video)
 Open Addressing, Cryptographic Hashing (video)
 PyCon 2010: The Mighty Dictionary (video)
 PyCon 2017: The Dictionary Even Mightier (video)
 (Advanced) Randomization: Universal & Perfect Hashing (video)
 (Advanced) Perfect hashing (video)
 [Review] Hash tables in 4 minutes (video)
 Online Courses:

 Core Hash Tables (video)
 Data Structures (video)
 Phone Book Problem (video)
 distributed hash tables:
Instant Uploads And Storage Optimization In Dropbox (video)
Distributed Hash Tables (video)
 Implement with array using linear probing

hash(k, m) - m is size of hash table
add(key, value) - if key already exists, update value
exists(key)
get(key)
remove(key)
More Knowledge
Binary search
 Binary Search (video)
 Binary Search (video)
 detail
 blueprint
 [Review] Binary search in 4 minutes (video)
 Implement:
binary search (on sorted array of integers)
binary search using recursion
Bitwise operations
 Bits cheat sheet - you should know many of the powers of 2 from (2^1 to 2^16 and 2^32)
 Get a really good understanding of manipulating bits with: &, |, ^, ~, >>, <<
 words
 Good intro: Bit Manipulation (video)
 C Programming Tutorial 2-10: Bitwise Operators (video)
 Bit Manipulation
 Bitwise Operation
 Bithacks
 The Bit Twiddler
 The Bit Twiddler Interactive
 Bit Hacks (video)
 Practice Operations
 2s and 1s complement
Binary: Plusses & Minuses (Why We Use Two's Complement) (video)
1s Complement
2s Complement
 Count set bits
4 ways to count bits in a byte (video)
Count Bits
How To Count The Number Of Set Bits In a 32 Bit Integer
 Swap values:
Swap
 Absolute value:
Absolute Integer
Trees
Trees - Intro
 Intro to Trees (video)
 Tree Traversal (video)
 BFS(breadth-first search) and DFS(depth-first search) (video)
BFS notes:
level order (BFS, using queue)
time complexity: O(n)
space complexity: best: O(1), worst: O(n/2)=O(n)
DFS notes:
time complexity: O(n)
space complexity: best: O(log n) - avg. height of tree worst: O(n)
inorder (DFS: left, self, right)
postorder (DFS: left, right, self)
preorder (DFS: self, left, right)
 [Review] Breadth-first search in 4 minutes (video)
 [Review] Depth-first search in 4 minutes (video)
 [Review] Tree Traversal (playlist) in 11 minutes (video)
Binary search trees: BSTs
 Binary Search Tree Review (video)
 Introduction (video)
 MIT (video)
C/C++:
 Binary search tree - Implementation in C/C++ (video)
 BST implementation - memory allocation in stack and heap (video)
 Find min and max element in a binary search tree (video)
 Find height of a binary tree (video)
 Binary tree traversal - breadth-first and depth-first strategies (video)
 Binary tree: Level Order Traversal (video)
 Binary tree traversal: Preorder, Inorder, Postorder (video)
 Check if a binary tree is binary search tree or not (video)
 Delete a node from Binary Search Tree (video)
 Inorder Successor in a binary search tree (video)
 Implement:
 insert // insert value into tree
 get_node_count // get count of values stored
 print_values // prints the values in the tree, from min to max
 delete_tree
 is_in_tree // returns true if given value exists in the tree
 get_height // returns the height in nodes (single node's height is 1)
 get_min // returns the minimum value stored in the tree
 get_max // returns the maximum value stored in the tree
 is_binary_search_tree
 delete_value
 get_successor // returns next-highest value in tree after given value, -1 if none
Heap / Priority Queue / Binary Heap
visualized as a tree, but is usually linear in storage (array, linked list)
 Heap
 Introduction (video)
 Binary Trees (video)
 Tree Height Remark (video)
 Basic Operations (video)
 Complete Binary Trees (video)
 Pseudocode (video)
 Heap Sort - jumps to start (video)
 Heap Sort (video)
 Building a heap (video)
 MIT: Heaps and Heap Sort (video)
 CS 61B Lecture 24: Priority Queues (video)
 Linear Time BuildHeap (max-heap)
 [Review] Heap (playlist) in 13 minutes (video)
 Implement a max-heap:
 insert
 sift_up - needed for insert
 get_max - returns the max item, without removing it
 get_size() - return number of elements stored
 is_empty() - returns true if heap contains no elements
 extract_max - returns the max item, removing it
 sift_down - needed for extract_max
 remove(x) - removes item at index x
 heapify - create a heap from an array of elements, needed for heap_sort
 heap_sort() - take an unsorted array and turn it into a sorted array in-place using a max heap or min heap
Sorting
 Notes:

Implement sorts & know best case/worst case, average complexity of each:
no bubble sort - it's terrible - O(n^2), except when n <= 16
 Stability in sorting algorithms ("Is Quicksort stable?")
Sorting Algorithm Stability
Stability In Sorting Algorithms
Stability In Sorting Algorithms
Sorting Algorithms - Stability
 Which algorithms can be used on linked lists? Which on arrays? Which on both?
I wouldn't recommend sorting a linked list, but merge sort is doable.
Merge Sort For Linked List
For heapsort, see Heap data structure above. Heap sort is great, but not stable

 Sedgewick - Mergesort (5 videos)

 1. Mergesort
 2. Bottom up Mergesort
 3. Sorting Complexity
 4. Comparators
 5. Stability
 Sedgewick - Quicksort (4 videos)

 1. Quicksort
 2. Selection
 3. Duplicate Keys
 4. System Sorts
 UC Berkeley:

 CS 61B Lecture 29: Sorting I (video)
 CS 61B Lecture 30: Sorting II (video)
 CS 61B Lecture 32: Sorting III (video)
 CS 61B Lecture 33: Sorting V (video)
 CS 61B 2014-04-21: Radix Sort(video)
 Bubble Sort (video)

 Analyzing Bubble Sort (video)

 Insertion Sort, Merge Sort (video)

 Insertion Sort (video)

 Merge Sort (video)

 Quicksort (video)

 Selection Sort (video)

 Merge sort code:

 Using output array (C)
 Using output array (Python)
 In-place (C++)
 Quick sort code:

 Implementation (C)
 Implementation (C)
 Implementation (Python)
 [Review] Sorting (playlist) in 18 minutes

 Quick sort in 4 minutes (video)
 Heap sort in 4 minutes (video)
 Merge sort in 3 minutes (video)
 Bubble sort in 2 minutes (video)
 Selection sort in 3 minutes (video)
 Insertion sort in 2 minutes (video)
 Implement:

 Mergesort: O(n log n) average and worst case
 Quicksort O(n log n) average case
Selection sort and insertion sort are both O(n^2) average and worst case
For heapsort, see Heap data structure above
 Not required, but I recommended them:

 Sedgewick - Radix Sorts (6 videos)
 1. Strings in Java
 2. Key Indexed Counting
 3. Least Significant Digit First String Radix Sort
 4. Most Significant Digit First String Radix Sort
 5. 3 Way Radix Quicksort
 6. Suffix Arrays
 Radix Sort
 Radix Sort (video)
 Radix Sort, Counting Sort (linear time given constraints) (video)
 Randomization: Matrix Multiply, Quicksort, Freivalds' algorithm (video)
 Sorting in Linear Time (video)
As a summary, here is a visual representation of 15 sorting algorithms. If you need more detail on this subject, see "Sorting" section in Additional Detail on Some Subjects

Graphs
Graphs can be used to represent many problems in computer science, so this section is long, like trees and sorting were.

Notes:

There are 4 basic ways to represent a graph in memory:
objects and pointers
adjacency matrix
adjacency list
adjacency map
Familiarize yourself with each representation and its pros & cons
BFS and DFS - know their computational complexity, their trade offs, and how to implement them in real code
When asked a question, look for a graph-based solution first, then move on if none
 MIT(videos):

 Breadth-First Search
 Depth-First Search
 Skiena Lectures - great intro:

 CSE373 2020 - Lecture 10 - Graph Data Structures (video)
 CSE373 2020 - Lecture 11 - Graph Traversal (video)
 CSE373 2020 - Lecture 12 - Depth First Search (video)
 CSE373 2020 - Lecture 13 - Minimum Spanning Trees (video)
 CSE373 2020 - Lecture 14 - Minimum Spanning Trees (con't) (video)
 CSE373 2020 - Lecture 15 - Graph Algorithms (con't 2) (video)
 Graphs (review and more):

 6.006 Single-Source Shortest Paths Problem (video)
 6.006 Dijkstra (video)
 6.006 Bellman-Ford (video)
 6.006 Speeding Up Dijkstra (video)
 Aduni: Graph Algorithms I - Topological Sorting, Minimum Spanning Trees, Prim's Algorithm - Lecture 6 (video)
 Aduni: Graph Algorithms II - DFS, BFS, Kruskal's Algorithm, Union Find Data Structure - Lecture 7 (video)
 Aduni: Graph Algorithms III: Shortest Path - Lecture 8 (video)
 Aduni: Graph Alg. IV: Intro to geometric algorithms - Lecture 9 (video)
 CS 61B 2014: Weighted graphs (video)
 Greedy Algorithms: Minimum Spanning Tree (video)
 Strongly Connected Components Kosaraju's Algorithm Graph Algorithm (video)
 [Review] Shortest Path Algorithms (playlist) in 16 minutes (video)
 [Review] Minimum Spanning Trees (playlist) in 4 minutes (video)
Full Coursera Course:

 Algorithms on Graphs (video)
I'll implement:

 DFS with adjacency list (recursive)
 DFS with adjacency list (iterative with stack)
 DFS with adjacency matrix (recursive)
 DFS with adjacency matrix (iterative with stack)
 BFS with adjacency list
 BFS with adjacency matrix
 single-source shortest path (Dijkstra)
 minimum spanning tree
DFS-based algorithms (see Aduni videos above):
 check for cycle (needed for topological sort, since we'll check for cycle before starting)
 topological sort
 count connected components in a graph
 list strongly connected components
 check for bipartite graph
Even More Knowledge
Recursion
 Stanford lectures on recursion & backtracking:
 Lecture 8 | Programming Abstractions (video)
 Lecture 9 | Programming Abstractions (video)
 Lecture 10 | Programming Abstractions (video)
 Lecture 11 | Programming Abstractions (video)
When it is appropriate to use it?
How is tail recursion better than not?
 What Is Tail Recursion Why Is It So Bad?
 Tail Recursion (video)
 5 Simple Steps for Solving Any Recursive Problem(video)
Backtracking Blueprint: Java Python

Dynamic Programming
You probably won't see any dynamic programming problems in your interview, but it's worth being able to recognize a problem as being a candidate for dynamic programming.
This subject can be pretty difficult, as each DP soluble problem must be defined as a recursion relation, and coming up with it can be tricky.
I suggest looking at many examples of DP problems until you have a solid understanding of the pattern involved.
 Videos:
 Skiena: CSE373 2020 - Lecture 19 - Introduction to Dynamic Programming (video)
 Skiena: CSE373 2020 - Lecture 20 - Edit Distance (video)
 Skiena: CSE373 2020 - Lecture 20 - Edit Distance (continued) (video)
 Skiena: CSE373 2020 - Lecture 21 - Dynamic Programming (video)
 Skiena: CSE373 2020 - Lecture 22 - Dynamic Programming and Review (video)
 Simonson: Dynamic Programming 0 (starts at 59:18) (video)
 Simonson: Dynamic Programming I - Lecture 11 (video)
 Simonson: Dynamic programming II - Lecture 12 (video)
 List of individual DP problems (each is short): Dynamic Programming (video)
 Yale Lecture notes:
 Dynamic Programming
 Coursera:
 The RNA secondary structure problem (video)
 A dynamic programming algorithm (video)
 Illustrating the DP algorithm (video)
 Running time of the DP algorithm (video)
 DP vs. recursive implementation (video)
 Global pairwise sequence alignment (video)
 Local pairwise sequence alignment (video)
Design patterns
 Quick UML review (video)
 Learn these patterns:
 strategy
 singleton
 adapter
 prototype
 decorator
 visitor
 factory, abstract factory
 facade
 observer
 proxy
 delegate
 command
 state
 memento
 iterator
 composite
 flyweight
 Series of videos (27 videos)
 Book: Head First Design Patterns
I know the canonical book is "Design Patterns: Elements of Reusable Object-Oriented Software", but Head First is great for beginners to OO.
Handy reference: 101 Design Patterns & Tips for Developers
Combinatorics (n choose k) & Probability
 Math Skills: How to find Factorial, Permutation and Combination (Choose) (video)
 Make School: Probability (video)
 Make School: More Probability and Markov Chains (video)
 Khan Academy:
Course layout:
 Basic Theoretical Probability
Just the videos - 41 (each are simple and each are short):
 Probability Explained (video)
NP, NP-Complete and Approximation Algorithms
Know about the most famous classes of NP-complete problems, such as traveling salesman and the knapsack problem, and be able to recognize them when an interviewer asks you them in disguise.
Know what NP-complete means.
 Computational Complexity (video)
 Simonson:
 Greedy Algs. II & Intro to NP Completeness (video)
 NP Completeness II & Reductions (video)
 NP Completeness III (Video)
 NP Completeness IV (video)
 Skiena:
 CSE373 2020 - Lecture 23 - NP-Completeness (video)
 CSE373 2020 - Lecture 24 - Satisfiability (video)
 CSE373 2020 - Lecture 25 - More NP-Completeness (video)
 CSE373 2020 - Lecture 26 - NP-Completeness Challenge (video)
 Complexity: P, NP, NP-completeness, Reductions (video)
 Complexity: Approximation Algorithms (video)
 Complexity: Fixed-Parameter Algorithms (video)
Peter Norvig discusses near-optimal solutions to traveling salesman problem:
Jupyter Notebook
Pages 1048 - 1140 in CLRS if you have it.
How computers process a program
 How CPU executes a program (video)
 How computers calculate - ALU (video)
 Registers and RAM (video)
 The Central Processing Unit (CPU) (video)
 Instructions and Programs (video)
Caches
 LRU cache:
 The Magic of LRU Cache (100 Days of Google Dev) (video)
 Implementing LRU (video)
 LeetCode - 146 LRU Cache (C++) (video)
 CPU cache:
 MIT 6.004 L15: The Memory Hierarchy (video)
 MIT 6.004 L16: Cache Issues (video)
Processes and Threads
 Computer Science 162 - Operating Systems (25 videos):
for processes and threads see videos 1-11
Operating Systems and System Programming (video)
What Is The Difference Between A Process And A Thread?
Covers:
Processes, Threads, Concurrency issues
Difference between processes and threads
Processes
Threads
Locks
Mutexes
Semaphores
Monitors
How they work?
Deadlock
Livelock
CPU activity, interrupts, context switching
Modern concurrency constructs with multicore processors
Paging, segmentation and virtual memory (video)
Interrupts (video)
Process resource needs (memory: code, static storage, stack, heap, and also file descriptors, i/o)
Thread resource needs (shares above (minus stack) with other threads in the same process but each has its own pc, stack counter, registers, and stack)
Forking is really copy on write (read-only) until the new process writes to memory, then it does a full copy.
Context switching
How context switching is initiated by the operating system and underlying hardware?
 threads in C++ (series - 10 videos)
 CS 377 Spring '14: Operating Systems from University of Massachusetts
 concurrency in Python (videos):
 Short series on threads
 Python Threads
 Understanding the Python GIL (2010)
reference
 David Beazley - Python Concurrency From the Ground Up: LIVE! - PyCon 2015
 Keynote David Beazley - Topics of Interest (Python Asyncio)
 Mutex in Python
Testing
To cover:
how unit testing works
what are mock objects
what is integration testing
what is dependency injection
 Agile Software Testing with James Bach (video)
 Open Lecture by James Bach on Software Testing (video)
 Steve Freeman - Test-Driven Development (that’s not what we meant) (video)
slides
 Dependency injection:
 video
 Tao Of Testing
 How to write tests
String searching & manipulations
 Sedgewick - Suffix Arrays (video)
 Sedgewick - Substring Search (videos)
 1. Introduction to Substring Search
 2. Brute-Force Substring Search
 3. Knuth-Morris Pratt
 4. Boyer-Moore
 5. Rabin-Karp
 Search pattern in text (video)
If you need more detail on this subject, see "String Matching" section in Additional Detail on Some Subjects.

Tries
Note there are different kinds of tries. Some have prefixes, some don't, and some use string instead of bits to track the path
I read through code, but will not implement
 Sedgewick - Tries (3 videos)
 1. R Way Tries
 2. Ternary Search Tries
 3. Character Based Operations
 Notes on Data Structures and Programming Techniques
 Short course videos:
 Introduction To Tries (video)
 Performance Of Tries (video)
 Implementing A Trie (video)
 The Trie: A Neglected Data Structure
 TopCoder - Using Tries
 Stanford Lecture (real world use case) (video)
 MIT, Advanced Data Structures, Strings (can get pretty obscure about halfway through) (video)
Floating Point Numbers
 simple 8-bit: Representation of Floating Point Numbers - 1 (video - there is an error in calculations - see video description)
Unicode
 The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets
 What Every Programmer Absolutely, Positively Needs To Know About Encodings And Character Sets To Work With Text
Endianness
 Big And Little Endian
 Big Endian Vs Little Endian (video)
 Big And Little Endian Inside/Out (video)
Very technical talk for kernel devs. Don't worry if most is over your head.
The first half is enough.
Networking
If you have networking experience or want to be a reliability engineer or operations engineer, expect questions
Otherwise, this is just good to know
 Khan Academy
 UDP and TCP: Comparison of Transport Protocols (video)
 TCP/IP and the OSI Model Explained! (video)
 Packet Transmission across the Internet. Networking & TCP/IP tutorial. (video)
 HTTP (video)
 SSL and HTTPS (video)
 SSL/TLS (video)
 HTTP 2.0 (video)
 Video Series (21 videos) (video)
 Subnetting Demystified - Part 5 CIDR Notation (video)
 Sockets:
 Java - Sockets - Introduction (video)
 Socket Programming (video)
