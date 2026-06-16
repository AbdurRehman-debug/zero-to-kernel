# Daily Log 📓

This folder documents every single day of my journey from SE student to Kernel Engineer.

One markdown file per week. Every day gets an entry inside that week's file.


---



## Folder Structure

```
daily-log/
├── README.md        ← you are reading this
├── week-01.md       ← Days 1-7
├── week-02.md       ← Days 8-14
├── week-03.md       ← Days 15-21
└── ...              ← one file per week, forever
```

Each week file contains 7 daily entries.
Each daily entry follows the exact same format described below.

---

## The Daily Format

Every single entry follows this structure exactly.
Do not invent your own format. Consistency is the point.

```markdown
---

## Day [N] — [Day Name], [Date]

**Phase:** [current phase]
**Topic:** [one line summary of what you studied today]
**Time Spent:** [hours]

---

### 📖 What I Studied
[Be specific. Not "studied linear algebra" but:
"3Blue1Brown Essence of Linear Algebra Video 4 — Matrix multiplication
as composition. MIT 18.06SC Lecture 3 — Multiplication and Inverse Matrices.
Strang book Chapter 2.4 pages 68-74."]

---

### 💡 What I Understood
[Explain the concept in your own words as if teaching it to someone.
No copying from books or videos. Your own words only.
If you cannot explain it simply you have not understood it yet.
This is the most important section.]

---

### 🔨 What I Built or Practiced
[Actual code written, problem solved, program compiled and run.
Even small things count.
"Implemented matrix multiply in NumPy from scratch without looking at reference.
Verified output matches np.matmul() for 3x3 and 4x4 matrices."
Paste short code snippets here if useful.]

---

### 📊 Result or Measurement
[If applicable — performance numbers, accuracy achieved, speedup measured,
problems solved, pages read. Something concrete and measurable.
Skip this section only if truly nothing is measurable today.]

---

### ❓ Still Confused
[Be completely honest. What did not click today.
What you re-read three times and still do not fully get.
This is not failure — this is the log doing its job.]

---

### 📅 Tomorrow
[Specific plan. Not "continue studying" but:
"Watch 3B1B Video 5 on determinants. Read Strang Chapter 3.1.
Implement determinant calculation by hand for 2x2 and 3x3 then verify with numpy."]
```

---

## A Real Example Entry



```markdown
---

## Day 4 — Thursday, June 19 2026

**Phase:** Phase 0 — Math Foundations
**Topic:** Matrix Multiplication — geometric meaning and computation
**Time Spent:** 2.5 hours

---

### 📖 What I Studied
3Blue1Brown Essence of Linear Algebra Video 4 — Matrix multiplication
as composition of transformations (~12 mins).
MIT 18.06SC Lecture 3 — Multiplication and Inverse Matrices (~48 mins).
Strang Introduction to Linear Algebra Chapter 2.4, pages 68-74.

---

### 💡 What I Understood
Matrix multiplication is not just arithmetic — it is composing two
transformations. If matrix A rotates space and matrix B scales it,
then AB is the transformation that first scales then rotates.

The order matters because of this. AB is not the same as BA because
"rotate then scale" gives a different result than "scale then rotate."
This is why matrix multiplication is not commutative.

For the actual computation: the entry C[i][j] is the dot product of
row i of A with column j of B. So every output element is a dot product.
This clicked for me when I realized a neural network layer is doing
this exact operation — each neuron computes the dot product of the
weight row with the input vector.

---

### 🔨 What I Built or Practiced
Implemented matrix multiplication from scratch in NumPy without
looking at any reference:

```python
import numpy as np

def my_matmul(A, B):
    rows_A, cols_A = A.shape
    rows_B, cols_B = B.shape
    C = np.zeros((rows_A, cols_B))
    for i in range(rows_A):
        for j in range(cols_B):
            for k in range(cols_A):
                C[i][j] += A[i][k] * B[k][j]
    return C

A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

my_result = my_matmul(A, B)
numpy_result = np.matmul(A, B)
print(np.allclose(my_result, numpy_result))  # True
```

Worked first try. The triple loop made the dot product structure obvious.

---

### 📊 Result or Measurement
Manual implementation matches np.matmul() for all test cases.
Strang Chapter 2.4 exercises: completed 6 out of 8 problems correctly.
Got problems 5 and 7 wrong — both were about non-square matrices,
will revisit tomorrow.

---

### ❓ Still Confused
Non-square matrix multiplication. When A is 3x2 and B is 2x4 I keep
confusing myself on the dimensions of the output. I know the rule
(inner dimensions must match, output is outer dimensions) but I made
errors on the exercises. Need more practice with non-square cases.

Also not fully clear on why the inverse of AB equals B_inverse times
A_inverse in reversed order. Strang states it but I want to derive it myself.

---

### 📅 Tomorrow
```
Watch 3B1B Video 5 — Three-dimensional linear transformations.
MIT 18.06SC Lecture 4 — Factorization into A=LU.
Read Strang Chapter 2.5 — Inverse Matrices.
Practice 10 more non-square matrix multiply problems to fix today's confusion.
Try to derive (AB)^-1 = B^-1 * A^-1 from scratch on paper.
 ```
 ---


*Started: 14 June 2026*
*Current streak: 3*
