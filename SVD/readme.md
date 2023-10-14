# Singular Value Decomposition

Singular Value Decomposition(SVD) is a mathematical technique that decomposes a matrix into three other matrices, providing a powerful tool for a variety of applications in linear algebra, statistics, and machine learning.

The SVD of matrix \(X\) is represented as:

\[X = U \Sigma V^T\]

Where:
- \(U\) is an orthogonal matrix representing the left singular vectors.
- \(\Sigma\) is a diagonal matrix containing the singular values.
- \(V\) is an orthogonal matrix representing the right singular vectors.

## Uses of SVD:
1. **Dimensionality Reduction**: By retaining only the top k singular values and setting smaller ones to zero, we can reduce dimensionality.

Here, Singular values are the square of Eigen values i.e., if \(\sigma_1\), \(\sigma_2\), and \(\sigma_3\) are singular values and \(\lambda_1\), \(\lambda_2\), and \(\lambda_3\) are eigenvalues, then:

&emsp;&emsp;&emsp;\(\sigma_1 = \sqrt{\lambda_1}\)
&emsp;&emsp;&emsp;\(\sigma_2 = \sqrt{\lambda_2}\)
&emsp;&emsp;&emsp;\(\sigma_3 = \sqrt{\lambda_3}\)

2. **Face Recognition**: Face recognition is one of the most famous use of SVD in real life. Basically it converts each face image into a matrix of pixel values. Once a matrix has been constructed we can apply SVD for the extraction of essential features. The eigenvectors with high eigenvalues represent the key facial features. These key features are also known as Eigenfaces. So this captures those important or key facial features, making it a powerful tool for face recognition.

3. **Pseudoinverse and Solving Linear Systems**: Pseudoinverse is a very familiar concept for any student studying Linear algebra. It is calculated for solving linear system of equations when the matrix is not square. SVD is used in calculating the pseudoinverse of a matrix.

## How to find SVD of a matrix:
1. **Matrix Setup**: Start with a given matrix \(X\) of dimensions \(m \times n\), where \(m\) is the number of rows and \(n\) is the number of columns.

2. **Calculate the Covariance Matrix**: If needed, calculate the covariance matrix of \(X\). This is not always necessary for finding SVD, but it may be useful in certain applications.

3. **Eigenvalues and Eigenvectors**: If computing the covariance matrix, find the eigenvalues and eigenvectors of \(X^TX\) (or \(XX^T\) if \(m < n\)).

4. **Singular Values and V Matrix**: The singular values, denoted by \(\sigma\), are the square roots of the eigenvalues. They represent the importance of each component. The \(V\) matrix contains the eigenvectors corresponding to the columns of \(X^TX\) (or \(XX^T\) if \(m < n\)). Normalize these vectors.

5. **U Matrix**: The \(U\) matrix contains the eigenvectors of \(XX^T\) (or \(X^TX\) if \(m < n\)). Normalize these vectors.

6. **Construct \(\Sigma\) Matrix**: Create the \(\Sigma\) matrix, which is a diagonal matrix with the square roots of the eigenvalues on the diagonal. The size of \(\Sigma\) is \(m \times n\) if \(m \geq n\) and \(n \times m\) if \(m < n\).

7. **Verify the Decomposition**: Check if \(X \approx U \Sigma V^T\). This serves as a verification of the correctness of the SVD.

8. **Optional: Rank Reduction**:
   - If dimensionality reduction is desired, keep only the top \(k\) singular values and their corresponding vectors in \(U\) and \(V\) to obtain a lower-dimensional approximation.

9. **Reconstruction (Optional)**: If you've performed rank reduction, you can reconstruct an approximation of the original matrix using the truncated \(U\), \(\Sigma\), and \(V\) matrices.

10. **Applications**: Utilize the SVD results for various applications, such as dimensionality reduction, image compression, collaborative filtering, and more.
