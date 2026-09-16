# Classwork feedback 20260911

**Student:** Peter
**Classwork:** Recursion and abstract data types (stack and queue)
**Date:** 2026-09-11

## Score

**84 / 100**

| Question | Score |
|---|---|
| Q1 Recursion (18) | 16 |
| Q2 Recursion in detail (20) | 13 |
| Q3 Stack (20) | 20 |
| Q4 Queue (26) | 22 |
| Q5 Applications (16) | 13 |

## Feedback on incorrect answers

**Q1 (a) definition of recursion (-1 mark)**
- A good description of the features of recursion. The definition needs the key idea that the problem is broken into a smaller or simpler version of the same problem.

**Q1 (c) why a stack suits recursion (-1 mark)**
- Strong answer. One mark is missing for naming what is actually stored - the return address and the local variables (the activation record).

**Q2 (a) to_binary unfolding (-4 marks)**
- The final answer "1101" and the base case are correct, but the intermediate values are shifted by one level: to_binary(1) returns "1" (not "11"), to_binary(3) returns "11" (not "110"), to_binary(6) returns "110" (not "1101"). Check what each call actually returns.

**Q2 (b) winding / unwinding (-3 marks)**
- Unwinding is well described. Winding needs more: the calls go deeper until the base case is reached, each call pushing a stack frame; unwinding pops the frames and combines the results.

**Q4 (a) FIFO / enqueue / dequeue (-2 marks)**
- FIFO is correct. Two details missing: enqueue adds to the REAR of the queue, and dequeue removes and RETURNS the item at the FRONT (not merely 'discarding' an element).

**Q4 (b) circular array (-2 marks)**
- Wrap-around, reuse of freed space and both pointer purposes are correct. Missing: a circular array avoids shifting the remaining elements, which an ordinary array would require after each dequeue.

**Q5 (b) queue from two stacks (-3 marks)**
- You correctly identify two stacks and that one reverses the order, but the enqueue description is confused. The standard method: enqueue simply pushes onto stack A; dequeue pops from stack B, moving everything from A to B only when B is empty (this reverses the order), then popping.

## Notes (no marks deducted)

**Q1 (d) factorial trace table**
- Full marks. The question did not specify the starting value, and your trace shows the factorial product correctly at each level. Adding the evaluated value (120, 24, 6, 2, 1) would make the table even stronger.

**Q3 (c) another use of a stack**
- Full marks - the question asked only for a situation (it did not require a reason), and saving register contents on an interrupt is an excellent, original example. Adding the LIFO reason (the last value saved is the first restored) would complete the answer.

---
_Detailed notes are also added as comments in your Word file._
