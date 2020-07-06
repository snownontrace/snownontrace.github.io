## Proof of the row rank of a matrix equals its column rank

_Summarized from Gilbert Strang's linear algebra lecture 18.065 on YouTube._

For a given matrix A with m rows and n columns, denote its column rank r_col and row rank r_row.

Identify a set of column space basis: C1, C2, ... Cr_col, and compose a matrix C = [C1 C2 ... Cr_col]. Following the rules of matrix multiplication, A can be factored into: A = C * R':
```matrix
                           ┌         ┐
                           │    R1'  │
                           │    R2'  │    
A = [ C1 C2 ... Cr_col ] * │   ...   │
                           │   ...   │
                           │ Rr_col' │
                           └         ┘
```
Note the number of rows in R' is r_col. Therefore, all the row vectors in A are linear combinations of the r_col rows of R', so the row rank of A r_row <= r_col.


Similarly, identify a set of row space basis, R1, R2, ... Rr_row, and compose a matrix R<sup>T</sup> = [R1 R2 R3 ... Rr_row]. A can be factored by A = C' * R:

```matrix
                              ┌        ┐
                              │   R1   │
                              │   R2   │    
A = [ C1' C2' ... Cr_row' ] * │   ...  │
                              │   ...  │
                              │ Rr_row │
                              └        ┘
```
From this factorization, it is clear that all column vectors of A are linear combinations of the r_row columns in C', so the column rank of A r_col <= r_row.

Taken together, we have r_row = r_col.
