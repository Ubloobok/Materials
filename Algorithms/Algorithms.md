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
|--------------|----------|------------|---------------------|
| [35. Search Insert Position](https://leetcode.com/problems/search-insert-position/) | Binary search to find the target or return left as position in a sorted array, `while left <= right`. | O(log n) Time, O(1) Space | Used in database queries to determine the insertion point for new records to maintain sorted order. |
| [704. Binary Search](https://leetcode.com/problems/binary-search/) | Binary search to find the target or determine it's not present. | O(log n) Time, O(1) Space | Quickly locating records in a large, sorted database or in any sorted data collection. |
| [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/) | Treat the 2D matrix as a flattened sorted array and use binary search. | O(log(m*n)) Time, O(1) Space | Searching in databases where records are stored in a matrix format, like seat reservations. |
| [875. Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/) | Use binary search to find the smallest possible maximum eating rate that allows Koko to eat all bananas within H hours. | O(n log m) Time, O(1) Space | Optimizing rates of processing or consumption in logistical operations and resource management. |
| [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) | Modified binary search, compare `mid` to `last` to handle the rotation. | O(log n) Time, O(1) Space | Applications involving retrieval of minimum data values from cyclically sorted datasets. |
| [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/) | Modified binary search, compare values to determine if left or right half is sorted. | O(log n) Time, O(1) Space | Searching in rotated logs or timeseries data where a sequence has been cyclically shifted. |
| [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/) | Dictionary where each key maps to a sorted list of timestamped values; then binary search. | O(log n) for searches, O(1) for insertions | Version control systems or caching systems where data must be retrieved as it existed at a particular time. |
| [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) | Parallel binary search in both arrays, ensuring the median conditions are satisfied, `int maxX = (partitionX == 0) ? int.MinValue : nums1[partitionX - 1];` etc. | O(log(min(m, n))) Time, O(1) Space | Statistical analysis in real-time data processing where median values are required from continuously updated data streams. |

### Sliding Window

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|----------|------------|---------------------|
| [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) | Iterate through the list of prices, keeping track of the minimum price encountered so far and calculating the maximum profit from potential sales on subsequent days. | O(n) Time, O(1) Space | Used in financial algorithms to maximize profit from trading stocks based on historical data. |
| [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/) | Use a sliding window approach with a hash map to track the last indices of characters and expand the window until a repeat character is found. | O(n) Time, O(min(m, n)) Space | Identifying the longest unique visitor sequence in web analytics without repeating users. |
| [424. Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/) | Use a sliding window approach to find the longest substring where you can replace k characters to make the substring all one character. | O(n) Time, O(1) Space | Modifying strings in text processing to achieve uniformity for aesthetic or formatting purposes. |
| [567. Permutation in String](https://leetcode.com/problems/permutation-in-string/) | Use a sliding window with two arrays to check character counts in the current window against the target permutation's character counts. | O(n) Time, O(1) Space | Searching for anagrams or certain patterns within biological sequences in computational biology. |
| [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/) | Implement a sliding window to find the smallest substring encompassing all the characters of another string, adjusting the window dynamically. | O(n) Time, O(m) Space | Filtering data to find the minimum context window containing required tokens in natural language processing. |
| [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) | Use a deque to maintain indices of elements, ensuring the front of the deque always gives the maximum element for the current window. | O(n) Time, O(k) Space | Real-time queue management where maximum or priority needs to be determined quickly within a moving time frame. |

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

A greedy algorithm constructs a solution by always making a choice that looks the best at the moment. 
It directly constructs the final solution. For this reason, greedy algorithms are usually very efficient.
The difficulty is that locally optimal choices (function) should also be globally optimal.

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|----------|------------|---------------------|
| [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/) | Kadane's algorithm, iterate through the array and store the maximum sum subarray ending at each position, set current sum as zero once it's negative (accumulated value). | O(n) Time, O(1) Space | Financial analysis to find the most profitable period in stock trading history. |
| [55. Jump Game](https://leetcode.com/problems/jump-game/) | Iterate through array, track max jump balance, i.e. the furthest reachable index as you move forward. | O(n) Time, O(1) Space | Evaluating if a sequence of steps or tasks can be completed in games or real-life project planning. |
| [45. Jump Game II](https://leetcode.com/problems/jump-game-ii/) | Iterate through array, track current end of the range you can reach and the farthest point that can be reached with another jump. Update the jump count each time you reach the end of the current range. | O(n) Time, O(1) Space | Planning and optimizing routes in logistics to minimize stops or changes, such as in delivery routes or during network routing to reduce latency. |
|||||
| [179. Largest Number](https://leetcode.com/problems/largest-number/) | Sort the numbers based on a custom comparator that compares two strings formed by concatenating the numbers in different orders. | O(n log n) Time, O(n) Space (or more because of temp memory?) | Creating the largest possible numerical value from a sequence of numbers, useful in generating visually impactful marketing numbers or sorting technical identifiers in a maximally distinguishable way. |

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
|--------------|----------|------------|---------------------|
| [136. Single Number](https://leetcode.com/problems/single-number/) | Use XOR to find the single non-repeated number in an array of pairs. | O(n) Time, O(1) Space | Detecting unique elements in datasets, such as unique user IDs in logs where all other IDs appear in pairs. |
| [191. Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/) | Iterate through each bit of the number using a mask. | O(1) Time, O(1) Space | Analysis of network packets to check parity or error bits, or simple hardware fault detection. |
| [338. Counting Bits](https://leetcode.com/problems/counting-bits/) | Dynamic programming, array where each element is the count of 1's in the binary representation of the index, turn off the rightmost 1-bit: `n & (n - 1)`. | O(n) Time, O(n) Space | Generating histograms of bit counts for cryptographic analysis or optimizing data compression algorithms. |
| [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/) | Iterate through each bit, set left (high) bit equal to lowest 0th bit, `result |= (uint)((n & 1) << bit)`. | O(1) Time, O(1) Space | Bit-level operations in low-level hardware communication protocols or graphics rendering optimizations. |
| [268. Missing Number](https://leetcode.com/problems/missing-number/) | Use XOR to detect the missing number in a sequence from 0 to n. | O(n) Time, O(1) Space | Detecting missing elements in data transmission or synchronization errors in data streams. |
| [371. Sum of Two Integers](https://leetcode.com/problems/sum-of-two-integers/) | XOR for sum, AND for carry. | O(1) Time, O(1) Space | Low-level programming where arithmetic operations are restricted or to avoid integer overflow issues. |
| [7. Reverse Integer](https://leetcode.com/problems/reverse-integer/) | Iteratively pop and push digits, check overflow before commit and bit shift. | O(log(n)) Time, O(1) Space | Applications requiring manipulation of numeric input, like calculators, or games involving number puzzles. |
| [9. Palindrome Number](https://leetcode.com/problems/palindrome-number/) | Like two pointers, extract value by / and %. | O(log n) Time, O(1) Space | Validating serial numbers, reading palindromic sequences in computational biology, or data validation checks. |

### Math & Geometry

| Problem Name | Approach | Complexity | Real-World Examples | 
|--------------|------|------------|---------------------|
|||||

