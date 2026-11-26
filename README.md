# EXPERIMENT-1.-EXPLORING-NUMPY-AND-PANDAS
AIM
To understand the use of NumPy and Pandas for performing basic data manipulation and analysis in Python.

ALGORITHM
Import the NumPy library for matrix and numerical operations.
Define a two-dimensional square matrix A and a vector b.
Compute the transpose of matrix A to interchange rows and columns.
Calculate the inverse of matrix A using np.linalg.inv(A) (ensure A is non-singular).
Solve the linear equation A × x = b using np.linalg.solve(A, b).
Perform eigen decomposition to find eigenvalues and eigenvectors using np.linalg.eig(A).
Display the results for the matrix, transpose, inverse, solution vector, and eigenvalues.
End the program.
FORMULAS / THEORY
Transpose: Aᵀ --- interchange rows and columns.
Inverse: A⁻¹ = adj(A) / |A|, provided det(A) ≠ 0.
Linear system: A × x = b  ⇒  x = A⁻¹b.
Eigen decomposition: A v = λ v, where λ is an eigenvalue and v is an eigenvector.
CODING
import numpy as np
A = np.array([[4.0, 2.0],
[1.0, 3.0]])
b = np.array([10.0, 8.0])
A_transpose = A.T
if np.linalg.det(A) != 0:
A_inv = np.linalg.inv(A)
else:
raise ValueError("Matrix A is singular and cannot be inverted.")
x = np.linalg.solve(A, b)
eigenvalues, eigenvectors = np.linalg.eig(A)
print("Matrix A:\n", A)
print("\nTranspose of A:\n", A_transpose)
print("\nInverse of A:\n", A_inv)
print("\nSolution vector x:\n", x)
print("\nEigenvalues:\n", eigenvalues)
print("\nEigenvectors:\n", eigenvectors)

OUTPUT
image
RESULT
It flipped the matrix, checked that it could be inverted, found its inverse, solved the equation for x, and calculated its eigenvalues and eigenvectors without any issues.
