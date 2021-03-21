Background
The Sparse matrix-vector multiplication (SpMV) operation (y = A ∗ x) is widely used in scientific and engineering calculations. But CSR-based SpMV has poor performance on processors with vector units.
CSR format stores nonzero elements discretely; thus, each multiplication needs memory access to fetch the nonzero elements in the matrix as well as the corresponding elements in the dense vector. Hence, a new pattern is needed to ameliorate this drawback.

Goals
In order to take full advantage of SIMD acceleration technology, the goals are:
1.	Design a new sparse matrix storage format to adapt the SIMD units.
2.	Design a new sparse matrix storage format‑based SpMV algorithm using SIMD vectorization.
