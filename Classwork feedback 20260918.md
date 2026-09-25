# Classwork feedback 20260918

**Student:** Peter
**Classwork:** Abstract data types - binary tree, linked list, circular queue
**Date:** 2026-09-18

## Score

**92 / 100**

| Question | Score |
|---|---|
| Q1 Binary tree concepts (25) | 23 |
| Q2 Linked list (35) | 34 |
| Q3 Circular queue programming (40) | 35 |

## Feedback on incorrect answers

**Q1 (d) binary search tree rule (-1 mark)**
- The left child being smaller than its parent earns the marks for that rule. Two points: the right-hand rule is "greater than **or equal to**" the parent, not simply greater; and both rules compare a child with its own **parent** node, so it is clearer to write "every left child's key < its parent's key and every right child's key >= its parent's key".

**Q1 (f) choice of key (-1 mark)**
- Uniqueness, the duplication problem and the consequence (not knowing which student a record belongs to) are all credited. The missing point is that a key must also be comparable, which is what allows the tree to order the records and search by them.

**Q2 (e) returning a node to the heap (-1 mark)**
- "Returned to the free list" and "can be used again" are credited. The missing point is the two pointer updates, and it is worth naming both variables: the removed node's pointer is set to the old `heapStartPointer`, and `heapStartPointer` is then updated to point at the removed node.

**Q3 (b) enqueue full check (-1 mark)**
- The global declaration, the full check, storing the item at `rear` and the wrap-around are all correct. The mark is lost because the full-queue message is **returned** rather than **output**: `return "Queue full"` hands the string back to the caller and nothing is displayed. Use `print("Queue full")`.

**Q3 (c) dequeue return string (-1 mark)**
- The empty check, reading the item at `front`, the wrap-around and updating `orderCount` are all correct. The mark is lost for the return string: the question specifies `"EMPTY"`, and Python string comparisons are case-sensitive, so `"Empty"` would not match what the program is expected to return.

**Q3 (d) main program (-2 marks)**
- All four steps of the main program are present and in the right order, so the logic earns its marks. Two marks are lost because the last four lines use `Print` with a capital P: Python has no such function, so the program stops with a `NameError` as soon as it reaches that line. Use `print()`.

**Q3 (f) three further dequeue calls (-1 mark)**
- The three "EMPTY" values and the fact that the queue is already empty are correct. The final mark is for naming the check in the code: `dequeue()` tests `orderCount == 0` and returns "EMPTY" **before** it reads the list.

## Notes (no marks deducted)

**Q1 (b) level and height**
- Full marks. Level 3 and height 2 are both correct. To make the answer complete in the exam it also helps to state that the root is counted as level 1, which is what makes 45 level 3, and to define height as the number of edges on the longest path from the root to the deepest leaf.

**Q1 (e) inserting 40**
- Full marks. Your answer - 45, left child - is correct, and the comparisons (larger than 38, smaller than 57, smaller than 45) are right.

**Q2 (a) trace table**
- Full marks. Every itemPointer is correct, and `-1` in the last row is the right value: the node holding 61 is the last node in the list, so its next pointer is the null pointer. It is worth adding in words that the search stops and returns the index once the item is found.

**Q1 (a), Q2 (b), Q2 (c), Q2 (d), Q3 (a), Q3 (e)**
- Full marks. In particular the whole of Q2 (c) and (d) - the insertAtStart and removeItem pseudocode - is exactly right, and your main program in Q3 (d) is correct apart from the `Print` spelling.

**Q3 (e) screenshot**
- Full marks for the output being correct and in the right order. A wider screenshot that also shows the terminal prompt and the command you ran would be more convincing as evidence that the program was run - worth doing next time.

---
_Detailed notes are also added as comments in your Word file._
