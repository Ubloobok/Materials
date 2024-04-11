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

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

### Stack

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

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
|--------------|------|------------|---------------------|
|||||

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

