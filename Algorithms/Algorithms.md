# Algorithms

These notes don't pretend to be like [Awesome Algorithms](https://github.com/tayllan/awesome-algorithms) or [Algo Deck](https://github.com/teivah/algodeck/tree/master), and even more like [Tech Interview Cheat Sheet](https://github.com/TSiege/Tech-Interview-Cheat-Sheet) or [Algorithms and Data Structures Cheatsheet](https://algs4.cs.princeton.edu/cheatsheet/).

## Problems

Well known problems (e.g. [Neetcode roadmap](https://neetcode.io/roadmap)), and comments for them, to remember something common between approaches.

### Arrays & Hashing

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
| [217. Contains Duplicate](https://leetcode.com/problems/contains-duplicate/) | HashSet to track seen elements. | O(n) Time, O(n) Space | Detecting fraud or duplicate transactions in banking systems. |
| [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/) | Count character occurrences in both strings and compare. | O(n) Time, O(1) Space | Plagiarism detection in textual content by comparing word frequencies. |
| [1. Two Sum](https://leetcode.com/problems/two-sum/) | Dictionary for numbers with indices, check for target - current. | O(n) Time, O(n) Space | Finding pair of products whose prices sum up to a specific gift card value in e-commerce platforms. |
| [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/) | Sort each string and use the sorted version as a key in a hashmap. | O(nk log k) Time, O(nk) Space | Categorizing words or phrases for efficient search in a dictionary or language processing app. |
| [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/) | Use a hashmap for frequency count and a heap or sort to find top K elements. | O(n log k) Time, O(n) Space | Identifying top searched queries or hashtags on social media platforms to trend topics. |
| [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/) | Calculate prefix and postfix products for each element, then multiply them. | O(n) Time, O(1) Space | Calculating the product of all other elements in a dataset, useful in financial analysis for portfolio diversification. |
| [36. Valid Sudoku](https://leetcode.com/problems/valid-sudoku/) | Check rows, columns, and 3x3 sub-boxes for duplicates using sets or arrays. | O(n^2) Time, O(n) Space | Validating user input in digital Sudoku games to ensure the rules are followed. |
| [271. Encode and Decode Strings](https://leetcode.com/problems/encode-and-decode-strings/) | Use a delimiter not present in strings or encode lengths to separate strings. | O(n) Time, O(n) Space | Encoding and decoding communication protocols in networking, or data storage formats. |
| [128. Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/) | Use a set for the array elements, then find the longest consecutive streak. | O(n) Time, O(n) Space | Determining the longest streak of attendance or consecutive logins by a user on a platform. |

### Two Pointers

| Problem Name | Hint | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
| [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) | Two pointers, by comparing from start and end. | O(n) Time, O(1) Space. | Data validation or processing palindrome phrases. |
| [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/) | Two pointers, moving inward based on their sum compared to the target. | O(n) Time, O(1) Space | Find options to fit within a budget limit in e-commerce optimization. |
| [15. 3Sum](https://leetcode.com/problems/3sum/) | Sort the array and use a fixed pointer with two moving pointers from both ends to find triples that sum to zero, skip the iterations where `nums[i]==nums[i-1]`. | O(n * log(n) + n^2) Time, O(1) Space | Find three investment options to balance a portfolio to zero net change in financial software. |
| [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/) | Two pointers, moving the pointer pointing to the shorter line inward, `if (height[i] < height[j])`. | O(n) Time, O(1) Space | Calculating maximum water containment or storage in physical simulations and real-world engineering problems. |
| [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/) | Two pointers and two heights from both sides to calculate trapped water at each index based on the min of max heights observed from both directions. | O(n) Time, O(1) Space | Modeling water collection in urban planning software or simulating fluid dynamics in environmental studies. |

### Stack

| Problem Name | Hint | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
| [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) | Track opening parentheses and match them with closing ones as they appear. | O(n) Time, O(n) Space | Syntax checking in code editors. |
| [155. Min Stack](https://leetcode.com/problems/min-stack/) | Simple stack with stored min, `(int item, int min)[] items`. | O(1) Time for all operations, O(n) Space | Implementing data structures in systems that require constant-time minimum retrieval, like resource management. |
| [150. Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/) | If int, then Push, else Pop+Pop, to evaluate the last operator. | O(n) Time, O(n) Space | Calculator software that needs to evaluate expressions entered in postfix form for easier computation. |
| [22. Generate Parentheses](https://leetcode.com/problems/generate-parentheses/) | Use backtracking, pass `countOpen` and `countClosed`, `if (countClosed == n) list.Add(str)`, adding open or close as long as it doesn't invalidate the sequence. | O(4^n / sqrt(n)) Time ([Catalan number](https://en.wikipedia.org/wiki/Catalan_number)), O(n) Space | Generating valid configurations for systems modeled with constraints similar to balanced parentheses. |
| [739. Daily Temperatures](https://leetcode.com/problems/daily-temperatures/) | Stack to track indices of temperatures, Pop when a higher temperature to calculate days until a warmer temperature. | O(2n) Time, O(n) Space | Climatology software predicting future temperature trends or changes based on past data. |
| [853. Car Fleet](https://leetcode.com/problems/car-fleet/) | Sort by position, `for` loop from the end, calculate the time needed for each car to reach the target, determine fleets based on time to reach the target. | O(n log n + n) Time (due to sorting, O(n) Space | Logistics and transport management systems tracking groups of vehicles reaching destinations. |
| [84. Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/) | Use a stack to maintain bars of histograms, and calculate area by extending the width for bars stored in the stack until a smaller one is encountered, `new Stack<(int index, int height)>()`, Push back last index with max common height. | O(n) Time, O(n) Space | Computational geometry applications analyzing spatial data to find the largest possible area under constraints. |


### Binary Search

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Sliding Window

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Linked List

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Trees

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Tries

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Backtracking

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Heap / Priority Queue

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|----------|------------|---------------------|
| [703. Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/) | Min-heap of size k, the top is the kth largest. | O(log k) for add operation, O(k) for initialization | Real-time leaderboard updates in gaming or financial applications, where only the top performers need to be tracked. |
| [1046. Last Stone Weight](https://leetcode.com/problems/last-stone-weight/) | Max-heap to dequeue the two largest stones until one or none remains. | O(n log n) Time, O(n) Space | Simulation of processes where the largest items are progressively reduced or combined, similar to tournament structures. |
| [973. K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/) | Max-heap of size k, priority based on Euclidean distance. | O(n log k) Time, O(k) Space | Determining nearest facility locations in logistics or emergency services relative to a central point. |
| [215. Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/) | Min-heap of size k,  the top is the kth largest, for guaranteed O(n log k). | O(n) average, O(n log k) worst-case | Stock market analysis to find the kth top-performing stocks in a dynamic array of stock changes. |
| [621. Task Scheduler](https://leetcode.com/problems/task-scheduler/) | Max-heap to schedule the most frequent tasks first, and cooldown queue with a period enforced by a counter. | O(n) Time, O(1) Space | CPU task scheduling where tasks must be spaced by a cooling period to prevent overheating or resource contention. |
| [355. Design Twitter](https://leetcode.com/problems/design-twitter/) | Implement using a combination of lists (for tweets) and hashmaps (for user follow information), using heaps to sort tweets by timestamp. | O(log n) for fetching tweets, O(1) for tweet posting and follow actions | Social media platforms where users need real-time access to a dynamically updating stream of data from followed accounts. |


### Intervals

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Greedy

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Graphs

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
| [207. Course Schedule](https://leetcode.com/problems/course-schedule) | DFS to find any cycle. | O(2n + 2e)) Time, O(3n + e) Space | Maze Solving, Dependency Resolution, Network Analysis. |
| [210. Course Schedule II](https://leetcode.com/problems/course-schedule-ii) | Topological Sort using BFS (Kahn's Algorithm). | O(2n + 2e) Time, O(3n + e) Space | Shortest Path, Social Networking, Web Crawling. |

### Advanced Graphs

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### 1-D DP

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### 2-D DP

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Bit Manipulation

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Math & Geometry

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

