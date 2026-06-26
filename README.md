# 🪟✌️ Sliding Window & Two Pointer Interview Patterns

Welcome to my personal archive of optimal solutions for classic **Sliding Window** and **Two Pointer** problems. 

This repository serves as a practical study guide containing clean, efficient implementations of some of the most frequently asked array and string manipulation questions in technical interviews (LeetCode / Striver's A2Z DSA Sheet).

---

## 📋 Solved Problems Index

The repository currently contains solutions to the following problems:

| Problem Name | Primary Pattern | Complexity (Time / Space) |
| :--- | :--- | :--- |
| **Binary Subarrays With Sum** | Variable Window / Prefix Sum | `O(N)` / `O(1)` or `O(N)` |
| **Count Number of Nice Subarrays** | Variable Window | `O(N)` / `O(1)` |
| **Fruit Into Basket** | Variable Window | `O(N)` / `O(1)` |
| **Longest Repeating Character Replacement** | Variable Window | `O(N)` / `O(1)` |
| **Longest Substring Without Repeating Characters**| Variable Window | `O(N)` / `O(min(N, M))` |
| **Max Consecutive Ones III** | Variable Window | `O(N)` / `O(1)` |
| **Maximum Points You Can Obtain from Cards** | Fixed Window | `O(K)` / `O(1)` |
| **Minimal Window Substring** | Variable Window (Hard) | `O(N + M)` / `O(1)` |
| **Number of Substrings Containing All Three Characters** | Variable Window | `O(N)` / `O(1)` |
| **Subarrays with K Different Integers** | Variable Window (Hard) | `O(N)` / `O(N)` |

*(Note: `M` generally denotes the size of the character alphabet, e.g., 26 or 128).*

---

## 🧠 Core Strategy Nuggets

If you are reviewing these files for interview prep, keep these three mental shortcuts in mind:

1. **The "At Most" Math Trick** 
   For problems like *Binary Subarrays With Sum*, *Count Number of Nice Subarrays*, and *Subarrays with K Different Integers*, calculating an exact count `== K` directly is extremely difficult. Instead, solve for:
   $$\text{Count}(= K) = \text{Count}(\le K) - \text{Count}(\le K - 1)$$

2. **The "Non-Shrinking" Window Optimization**
   In problems like *Max Consecutive Ones III* or *Longest Repeating Character Replacement*, once your window reaches a valid maximum length $L$, **you never need to shrink it back down**. Instead of a `while` loop that contracts the left pointer, use an `if` statement to shift the entire window to the right. This keeps your logic strictly `O(N)`.

3. **Circular / Opposite Ends (Cards Problem)**
   For *Maximum Points You Can Obtain from Cards*, rather than trying to simulate taking from the left and right dynamically, calculate the total sum of a fixed window of size `K` from the left, then iteratively slide the window backward into the right side of the array.

---

## 🚀 Repository Navigation

Each file in this repository corresponds directly to the problem title and contains:
* The core solution class/function.
* Clean, readable syntax.
* Minimal overhead so you can copy-paste directly into testing environments like LeetCode.

---

## 🛠️ Language

* **Primary Language:** C++ *(Update this if your repo uses Python/Java)*
