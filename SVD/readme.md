# Singular Value Decomposition

Singular Value Decomposition(SVD) is a mathematical technique that decomposes a matrix into three other matrices, providing a powerful tool for a variety of applications in linear algebra, statistics, and machine learning.

The SVD of matrix \(X\) is represented as:

\[X = U \Sigma V^T\]

Where:
- \(U\) is an orthogonal matrix representing the left singular vectors.
- \(\Sigma\) is a diagonal matrix containing the singular values.
- \(V\) is an orthogonal matrix representing the right singular vectors.

## Uses of SVD:
1. **Dimensionality Reduction:** By retaining only the top k singular values and setting smaller ones to zero, we can reduce dimensionality.

Here, Singular values are the square of Eigen values i.e., if \(\sigma_1\), \(\sigma_2\), and \(\sigma_3\) are singular values and \(\lambda_1\), \(\lambda_2\), and \(\lambda_3\) are eigenvalues, then:

&emsp;&emsp;&emsp;\(\sigma_1 = \sqrt{\lambda_1}\)
&emsp;&emsp;&emsp;\(\sigma_2 = \sqrt{\lambda_2}\)
&emsp;&emsp;&emsp;\(\sigma_3 = \sqrt{\lambda_3}\)

2. **Face Recognition:** Face recognition is one of the most famous use of SVD in real life. Basically it converts each face image into a matrix of pixel values. Once a matrix has been constructed we can apply SVD for the extraction of essential features. The eigenvectors with high eigenvalues represent the key facial features. These key features are also known as Eigenfaces. So this captures those important or key facial features, making it a powerful tool for face recognition.

3. **Pseudoinverse and Solving Linear Systems:** Pseudoinverse is a very familiar concept for any student studying Linear algebra. It is calculated for solving linear system of equations when the matrix is not square. SVD is used in calculating the pseudoinverse of a matrix.