# Classwork feedback 20260904

**Student:** Peter
**Classwork:** Algorithms - Big-O, linear search, binary search, insertion sort
**Date:** 2026-09-04

## Score

**93 / 100**

| Question | Score |
|---|---|
| Q1 | 27/30 |
| Q2 | 40/40 |
| Q3 | 26/30 |

## Feedback on incorrect answers

**Q1 (d) (-3 marks)**
- The function returns -1, not 0. With found initialised to -1 and the loop skipped, the 'if found != -1' test fails and the else branch returns -1. Boundary reasoning was valid.

**Q3 (a) (-1 mark)**
- Outer loop 'for i in range(len(arrayA))' starts at 0 - the first iteration is a no-op. Start at 1: 'range(1, len(arrayA))'.

**Q3 (b) (-2 marks)**
- Two 'count' increments: the one inside the while loop (per shift) is correct, the extra one after the loop (per item) over-counts.

**Q3 (c) (-1 mark)**
- List B does produce more shifts, but List A produces 0 shifts (not 'equal to its length'), and List B is 4+3+2+1 = 10 shifts (not 15).

---
_Detailed notes are also added as comments in your Word file._
