Mastercard’s coding interviews and Online Assessments (OAs) focus heavily on **core data structures, optimal pattern recognition, and readable implementation** rather than esoteric "gotcha" algorithms.

Historically, Mastercard’s algorithmic question mix sits around **45% Easy, 50% Medium, and under 5% Hard**. The focus is on clean edge-case handling, optimal Big-O performance, and explaining your thought process clearly.

---

## 1. Primary Algorithm Patterns Tested

```
         ┌────────────────────────────────────────────────────────┐
         │              Mastercard Question Frequency             │
         ├────────────────────────────────────────────────────────┤
         │  Array & Hash Maps  ██████████████████████████ 67%     │
         │  String Operations  ███████████████ 33%                │
         │  Dynamic Programming███████████ 25%                    │
         │  Greedy & Two Pointer██████████ 25%                    │
         │  Stacks & Queues    ███████ 17%                        │
         └────────────────────────────────────────────────────────┘

```

---

## 2. High-Frequency Mastercard Coding Questions

### A. Arrays & Hash Tables

1. **Two Sum / Target Pair Matching**
* *Problem:* Find two numbers in an array that add up to a target sum.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time, $\mathcal{O}(N)$ Space using a Hash Map.
* *Mastercard Nuance:* Often framed around matching financial transactions or balancing ledger amounts.


2. **Remove Duplicates from Sorted Array**
* *Problem:* Modify an array in-place to remove duplicates and return the new length.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time, $\mathcal{O}(1)$ Space using Two Pointers.


3. **Subarray / Sliding Window (Maximum Subarray - Kadane’s Algorithm)**
* *Problem:* Find the contiguous subarray with the largest sum.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time, $\mathcal{O}(1)$ Space.


4. **Rotate Image / Matrix Transformation**
* *Problem:* Rotate an $N \times N$ 2D matrix by 90 degrees clockwise in-place.
* *Optimal Complexity:* $\mathcal{O}(N^2)$ Time via matrix transpose and row reversal.



---

### B. String Manipulation & Sliding Window

1. **Valid Parentheses / Expression Matching**
* *Problem:* Check if opening and closing brackets `()`, `{}`, `[]` are balanced and in valid sequence.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time, $\mathcal{O}(N)$ Space using a Stack.


2. **Longest Substring Without Repeating Characters**
* *Problem:* Find the length of the longest substring containing unique characters.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time using a Sliding Window with a Hash Set.


3. **Valid Anagram & Palindrome Checks**
* *Problem:* Verify if one string is an anagram of another, or if a string reads the same backward after stripping non-alphanumeric characters.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time, $\mathcal{O}(1)$ auxiliary space with character frequency tables.



---

### C. Search & Two-Pointer Algorithms

1. **Search in Rotated Sorted Array**
* *Problem:* Given an array rotated at some pivot, search for a target value in $\mathcal{O}(\log N)$ time.
* *Key Concept:* Modified Binary Search identifying which half of the array is strictly sorted.


2. **Container With Most Water**
* *Problem:* Given array heights, find two lines that together with the x-axis form a container holding the most water.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time using inward Two Pointers.



---

### D. Dynamic Programming & Greedy Algorithms

1. **Best Time to Buy and Sell Stock**
* *Problem:* Maximize profit from buying on one day and selling on a future day.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time, $\mathcal{O}(1)$ Space tracking running minimum price.


2. **Coin Change Problem**
* *Problem:* Find the minimum number of coins needed to make a specific amount.
* *Optimal Complexity:* $\mathcal{O}(S \cdot N)$ where $S$ is the amount and $N$ is the number of coin denominations (using 1D DP tabulation).


3. **Gas Station / Circuit Traversal**
* *Problem:* Determine starting gas station index to complete a full circular route.
* *Optimal Complexity:* $\mathcal{O}(N)$ Time using Greedy tracking of net total vs. current tank balance.



---

## 3. Practical Platform Logic Questions (Java / Backend Roles)

In technical live-coding rounds, Mastercard often shifts from abstract DSA to practical code manipulation tasks:

* **Functional Collections Operations:** Using Java 8 Streams to group, aggregate, or filter custom objects (e.g., *Group transactions by currency and calculate total sum* or *Find top 3 frequent numbers/strings*).
* **LRU Cache Implementation:** Implementing a Least Recently Used cache combining a `HashMap` and `DoublyLinkedList` in $\mathcal{O}(1)$ time.
* **Custom Thread-Safe Counter / Singleton:** Writing thread-safe implementations using `ReentrantLock` or `AtomicInteger`.

---

## Key Tips for Clearing the Mastercard Technical Round

1. **State Trade-offs Out Loud:** Always mention your initial brute-force approach first, then explain how moving from $\mathcal{O}(N^2)$ to $\mathcal{O}(N)$ or $\mathcal{O}(N \log N)$ optimizes space/time.
2. **Proactively Test Edge Cases:** Before running your code, test empty inputs, single-element arrays, duplicate values, and negative integers.
3. **Prioritize Code Cleanliness:** Use descriptive variable names, avoid monolithic functions, and structure modular helper methods.
