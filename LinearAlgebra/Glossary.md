# Linear Algebra Notes

## Vector
Essentially an array of numbers.  It can be a row vector or a column vector.  It can be used to represent a point in space, a direction, or a line.

Vector addition and subtraction are done element-wise.

### Examples
* 2 dimensional : [2, 3]
* 3 dimensional : [3, 5, 7]

### Row Vector
A vector that is oriented horizontally.  It is a 1xN matrix.

### Column Vector
A vector that is oriented vertically.  It is an Nx1 matrix.

## Dot-product
An operation between two equally-sized vectors that results in a scalar.  It is used to determine the angle between two vectors, or to project one vector onto another.


## Dot-product (aka Inner Product) - Algebraic Definition
The dot product of two vectors is the sum of the products of the corresponding elements of the two vectors.

Alternately, transpose the second vector, then do standard matrix multiplication.

* Associative: No.  You cannot change the order of the vectors.  (A dot B) dot C ≠ A dot (B dot C).
* Distributive: Yes, you can distribute the scalar. a dot (b+c) == a dot b + a dot c
* Commutative: Yes, the dot product is commutative.  A dot B == B dot A

## Dot-Product - Geometric Definition
A * B * cos(θ) where θ is the angle between the two vectors.

* 0 when the vectors are orthogonal
* more-positive when the vectors are similar
* more negative when the vectors are dissimilar

## Hadamard Multiplication
Elementwise Multiplication (eg [a, b] x [c d] = [ a*c b*d ])

Expressed in python as __dot star__ :  V __.*__ W

## Outer Product
The outer product of two vectors is a matrix.  It is the product of the first vector and the transpose of the second vector.

![Outer Product](../images/VectorOuterProduct.png "Outer Product")

Calculated similarly to dot product except the second vector is transposed instead of the first.

## Cross product
A vector that is perpendicular to the plane defined by the two vectors.    

* Defined only for 2 3D vectors.  
* Result is another 3D vector.

![Cross Product](../images/CrossProduct.png "Cross Product")


## Unit Vector
A vector whose magnitude is 1.  It is used to represent a direction.

## Vector Norm
The length of a vector.  It is calculated by taking the square root of the sum of the squares of the elements of the vector.
(ie.. use pythagoras theorem)

## Dimension
The number of elements in a vector.   


## Field
A set (typically numbers) that can be added, subtracted, multiplied, and divided.  Eg...  Real numbers, complex numbers, rational numbers.  But not Integers though because integer division often does not result in an integer.

## Subspace
A set of all vectors that can be created by taking linear combinations of a set of vectors.

Eg 1:   given v = [2,3], v is in the same subspace as 2v = [4,6] and 3v = [6,9].
Eg 2:	given v = [2,3], w = [0 ,4] combined together form a subspace of [12,2] because 6v = [12,18] and 4w = [0,16] and 6v + 4w = [12,2]

## Actual definition
A subset of a vector space that is closed under addition and scalar multiplication.  It must contain the zero vector.

## Ambient space
The vector space that contains the subspace.

ie... the container for a subspace that may have more dimensions than the subspace it contains.

## Subset
A set of points that satisfy a given condition.
* doesn't need to be closed.
* Doesn't need to include the origin.
* can have boundaries.

## Span
The span of a set of vectors is all possible linear combinations of all vectors in that set.

A matrix is "in the span" of another subspace if it can be created by making linear weighted combinations of all vectors in that subspace.

## Linear Independence (a property of a set)
* A set of vectors is linearly independent if no vector in the set can be created by a linear combination of the other vectors in the set.
* A set of M vectors is independent if each vector points in a geometric dimension not reachable using other vectors in the set.


### Examples  
* A = [0, 2, 5], B = [-27, 5, -37], and C = [3, 4, 9] are linearly independent.
* A = [0, 2, 5], B = [-27, 5, -37], and D =[3, 1, 8] are not linearly independent because 7A - 9C = B.

## Basis
A Basis set is a linearly independent set of vectors that span a vector space.


## Matrix 
Essentially a 2D array of numbers.  It can be used to represent a transformation, a set of points, or a set of vectors.

* 3x3 Example 
```  
[1, 3, 5] 
[2, 4, 6] 
[7, 8, 9]
```  

## Transpose
Swap the rows and columns of a matrix or vector.  This is done by flipping the matrix over its diagonal.

## Hermitian Transpose (aka Conjugate Transpose)
It is the transpose of the matrix with the complex conjugate of each element.

Flip the sign of the imaginary part of a complex number.

Eg...  
* a+bi becomes a - bi
* a-bi becomes a + bi

## Matrix Multiplication Example

![Matrix Multiplication](../images/MatrixMulitplication.png "Matrix Multiplication")

## LIVE EVIL rule
(LIVE)^T^ == E^T^V^T^I^T^L^T^

In other words, to apply a transpose to a product of matrices, you can instead reverse the order of the matrices and transpose each one.

This does not work in scenarios where all matrices cannot be transposed.


## Special kinds of matrices

### Square Matrix
A matrix where the number of rows equals the number of columns.

### Symmetric Matrix
A square matrix that is equal to its transpose.

eg...  
```  
[ 1, 2, 3 ]  
[ 2, 4, 5 ]  
[ 3, 5, 6 ]  
```

### Skew-Symmetric Matrix
A square matrix that is equal to the negative of its transpose.
eg...
```  
[ 0, 2, -5 ]  
[ -2, 0, 7 ]  
[ 5, -7, 0 ]  
```

### Pure Rotation Matrix (transformation)
A matrix that rotates a vector but does not scale or skew it.

```
[ cos(θ), -sin(θ) ]
[ sin(θ), cos(θ) ]
```


### Diagonal Matrix
A matrix where all elements are zero except for the diagonal elements.
eg...  
```  
[ 1, 0, 0 ]  
[ 0, 2, 0 ]  
[ 0, 0, 3 ]  
```

### Triangular Matrix
#### upper triangular matrix
A matrix where all elements below the diagonal are zero.
eg...
```  
[ 1, 2, 3 ]  
[ 0, 4, 5 ]  
[ 0, 0, 6 ]  
```

#### lower triangular matrix
A matrix where all elements above the diagonal are zero.
eg...  
```  
[ 1, 0, 0 ]  
[ 2, 4, 0 ]  
[ 3, 5, 6 ]  
```

### Identity Matrix
A square matrix where all elements are zero except for the diagonal elements which are 1.

eg for a 3x3 matrix...  
```  
[ 1, 0, 0 ]  
[ 0, 1, 0 ]  
[ 0, 0, 1 ]  
```

### Block Matrix
A matrix that is made up of smaller matrices.

eg...  
```
[ A, B ]
[ C, D ]
```

where A, B, C, and D are all smaller (2x2) square matrices.

### Multiplicative Identity Matrix
A matrix that when multiplied by another matrix, results in the original matrix.
eg...  for 3x3 matrix...
```  
[ 1, 0, 0 ]  
[ 0, 1, 0 ]  
[ 0, 0, 1 ]  
```

### Additive Identity Matrix (aka Zero Matrix)
A matrix that when added to another matrix, results in the original matrix.  

eg...  for 3x3 matrix...
```  
[ 0, 0, 0 ]  
[ 0, 0, 0 ]  
[ 0, 0, 0 ]  
```

### Additive symmetric matrix
A matrix can be added to its transpose to get a symmetric matrix.

eg...  
```  
[ a, b, c ]    [ a, d, g ]      [a+a, b+d, c+g]
[ d, e, f ] +  [ b, e, h ] =    [b+d, e+e, h+f]
[ g, h, i ]    [ c, f, i ]      [c+g, h+f, i+i]
```
optionally then devide by 2 to scale it back to its previous size.


### Multiplicative symmetric matrix
A matrix that when multiplied by its transpose, results in a symmetric matrix.

eg...  
```  
[ a, b, c ]    [ a, d, g ]      [a*a+b*b+c*c, a*d+b*e+c*f, a*g+b*h+c*i]
[ d, e, f ] *  [ b, e, h ] =    [a*d+b*e+c*f, d*d+e*e+f*f, d*g+e*h+f*i]
[ g, h, i ]    [ c, f, i ]      [a*g+b*h+c*i, d*g+e*h+f*i, g*g+h*h+i*i]
```

## Matrix Algebra Shortcuts with square matrices
* When A is a square matrix, A<sup>-1</sup> is the inverse of A.
* When A is a square matrix, A<sup>-2</sup> is the inverse of AA.
* When A is a square matrix, A<sup>-3</sup> is the inverse of AAA.
* When A is a square matrix, A<sup>-n</sup> is the inverse of A<sup>n</sup>.
* When A is a square matrix, A<sup>T</sup> is the transpose of A.
* When A is a square matrix, A<sup>1/2</sup> is the square root of A.
* When A is a square matrix, A<sup>1/3</sup> is the cube root of A.
* When A is a square matrix, A<sup>1/n</sup> is the nth root of A.

## Matrix algebra shortcuts with non-square matrices
* When A is a full rank rectangular matrix, A<sup>T</sup>A is a square matrix.

## Matrix algebra shortcuts with symmetric matrices
* When A is a square symmetric matrix, A<sup>2</sup> is also a symmetric matrix.
* When A is a symmetric matrix, A<sup>T</sup>A is A<sup>2</sup>.


## Matrix algebra shortcuts with orthogonal matrices
* When Q is a square orthogonal matrix, Q<sup>T</sup> is the same as Q<sup>-1</sup>.
* When Q is a square orthogonal matrix, Q<sup>2</sup> is the identity matrix.
* When Q is a square orthogonal matrix, Q<sup>3</sup> is the same as Q.
* When Q is a square orthogonal matrix, Q<sup>-1</sup> is the same as Q<sup>T</sup>.




## Trace
* The trace of a square matrix is the sum of the diagonal elements.  
* It is used to calculate the determinant of a matrix.
* Trace is only defined for square matrices.

## Broadcasting vs Concatenation


### Matrix Broadcasting
* The process of making two matrices the same size by duplicating rows or columns.
* Used in machine learning to make two matrices the same size so they can be added or multiplied.
* Not common in traditional linear algebra.

eg... to make broadcast a 4x1 matrix to a 4x4 matrix
```
[ 1 ]   becomes   [ 1 1 1 1 ]
[ 2 ]             [ 2 2 2 2 ]
[ 3 ]             [ 3 3 3 3 ]
[ 4 ]             [ 4 4 4 4 ]
```

### Concatenation of matrices
* Concatenation of matrices is the process of joining two matrices together.

eg...
```
[ A, B ] and [ C, D ] can be concatenated to form a 1x4 matrix.
[ A, B, C, D ]
```
 


## Matrix Rank

## Fundamental Eigenvalue equation
A * v = λ * v

Where A is a matrix, v is an eigenvector, and λ is an eigenvalue.

## Eigen Vector
A vector that is not changed by a transformation.  It is a vector that is only scaled by a transformation.

eg...  
```  
[ 2, 1 ]   [ 1 ]   [ 4 ]  
[ 2, 3 ] * [ 2 ] = [ 8 ]  

[1] is the eigen vector of the matrix [2 1]  
[2]                                   [2 3]  
```


## Eigen Value
The scalar that represents how much an eigenvector is scaled by a transformation.

eg in the previous example...  
```
    [ 1 ]   [ 4 ]
4 * [ 2 ] = [ 8 ]

4 is the eigen value of the matrix [2 1]
                                   [2 3]               
                                   
which as the same effect of having multiplied it by [1]
                                                    [2]
```

## Frobenuis dot product
### First way to compute Frobenius dot product

* step 1: multiply the two matrices element-wise
* step 2: sum all the elements in the resulting matrix

### Second Way to compute Frobenius dot product

* Step 1:  Flatten both matrices into vectors.
* Step 2:  Compute the dot product of the two vectors.

### Third way to compute Frobenius dot product
given that a and B are two vectors
Take the trace of (A^T^ B)


## Vectorize a matrix.
To convert a matrix into a vector, you can flatten the matrix.
eg...
```
[ 1, 2, 3 ]   becomes   [ 1 ]
[ 4, 5, 6 ]             [ 4 ]
                        [ 2 ]
                        [ 5 ]
                        [ 3 ]
                        [ 6 ]
```

## Matrix Normalization Techniques

### Frobenuis norm aka Eculedian Norm aka L2 norm aka P2 norm
The square root of the sum of the squares of the elements in a matrix.
eg...with this matrix...
```  
[ 2, 3 ]  
[ 5, 7 ]  
```
the square root of 2^2^ + 3^2^ + 5^2^ + 7^2^ = 9.5

## P norm
The P norm of a matrix is the sum of the absolute values of the elements in the matrix raised to the power of P, then take the Pth root of the result.


### L1 norm, aka P1 norm
Sum of the absolute values of the elements in a matrix.
eg...
```  
[ 2, 3 ]  
[ 5, 7 ]  
```
the sum of the absolute values of the elements = 17

### L-infinity norm
The maximum absolute value of the elements in a matrix.
eg...
```  
[ 2, 3 ]  
[ 5, 7 ]  
```
the maximum absolute value of the elements = 7

### L0 norm
The number of non-zero elements in a matrix.
eg...
```  
[ 2, 3 ]  
[ 5, 7 ]  
```
the number of non-zero elements = 4

### Schatten P Norm
The sum of the Pth power of the singular values of a matrix, then take the Pth root of the result.
eg...

## Matrix Asymmetry Index
a~i~ = norm(Ã) / norm(A)

where Ã is the assymetry matrix (A - A^T^) / 2

## Matrix Inverse
* A matrix B that when multiplied by a given matrix A, results in the identity matrix.
* Not all square matrices have an inverse.
* Defined for Square, full rank matrices only.

It's best to avoid inverses if possible due to rounding errors that result from floating-point arithmetic on computers.

For orthogonal matrices, the inverse is the same as their transpose. (ie... A<sup>-1</sup> = A<sup>T</sup>, \
and A<sup>-T</sup> = A)

### How to calculate the inverse of a matrix (MCA Algorithm)
using this matrix as an example...
```
[ 1,  3,  0 ]
[ 0, -2,  8 ]
[ 7,  2, -6 ]
```


First, calculate the determinant of the matrix.  If the determinant is zero, the matrix does not have an inverse.
```
[ 1,  3,  0 ]
[ 0, -2,  8 ]
[ 7,  2, -6 ]
```
determinant = 164

* M - Minors Matrix - The matrix of determinants of the submatrices of a matrix.
```
[  -4, -56,  14 ]
[ -18,  -6, -19 ]
[  24,   8,  -2 ]
```

 
* C - Cofactors Matrix - The minors matrix, with alternating signs.
```
[  -4, 56, 14 ]
[  18, -6, 19 ]
[  24, -8, -2 ]
```

* A - Adjugate Matrix - The transpose of the matrix of cofactors.
```
[  -4, 18, 24 ]
[  56, -6, -8 ]
[  14, 19, -2 ]
```
 
Divide the Adjuate matrix by the determinant of the original matrix to get the Inverse of the original matrix.
```
[  -4, 18, 24 ]
[  56, -6, -8 ] * 1/164
[  14, 19, -2 ]
```

## Singular Matrix
A matrix that does not have an inverse. The determinant will be zero.

## Full Column Rank
A matrix that has only linearly independent columns.

## Left Inverse
Given the original full-column-rank matrix A 
* (A<sup>T</sup>A)<sup>-1</sup> * A<sup>T</sup>A = Identity matrix I
* (A<sup>T</sup>A)<sup>-1</sup> * A<sup>T</sup> => Left Inverse of A

Only available when the Matrix A has full column rank.

Can also be calculated as A = VΣ<sup>-1</sup>U<sup>T</sup> 

## Right Inverse
Given the original full-row-rank matrix A
* (A\*A<sup>T</sup>)(A\*A<sup>T</sup>)<sup>-1</sup> = Identity matrix I
* A<sup>T</sup>(A\*A<sup>T</sup>)<sup>-1</sup> => Right Inverse of A

## Pseudo Inverse (moore-penrose inverse)
* The pseudo-inverse of a matrix is a generalization of the inverse of a matrix that works for non-square matrices.
* The moore-penrose inverse is unique, but there are other kinds of pseudo-inverse algorithms that are not unique.

## Projection in R<sup>2</sup> 
* Mapping over magnitude
Given
* Vector A,   eg... [2, 3]
* Point B, eg... [4, 5]
* Scalar ß = ?  (meant to scale Alpha to be closest to point B)

Come up with a scaled version of A that is closest to B.

The line that is perpendicular to A is B - ßA.  This line is perpendicular to A, so the dot product of A and B - ßA is zero.

A dot (B-Aß) = 0 \
=> \
A dot B - A dot Aß = 0 \
=> \
A dot Aß = A dot B  \
=> \
A dot Aß/(A dot A) = (A dot B) / (A dot A) 

```
ß = (A dot B) / (A dot A)
```

## Orthogonal Matrix
A square matrix whose columns represent individual column vectors that are orthogonal to each other.  Each column should also be of unit length.

## Gram-schmidt procedure
* A method for finding an orthogonal basis for a subspace.
* It's not reliable on large matricies due to rounding errors.  The concept is valid, but surds tend to make the result inaccurate.

### Gram-Schmidt procedure walkthrough
* Take the first column and orthogonalize it.  
* Then take the second column and orthogonalize it with respect to the first column.  
* Continue this process for all columns.
* Once all this is done, scale each column to have a magnitude of 1. (ie.. make them each unit vectors)

## Sherman-Morrison Formula
An alternate formula that calculates the inverse of a matrix.
Given
* Matrix A
* Identity matrix I
* column vector a
* column vector b 
* a<sup>T</sup>b ≠ 1 \
\
A<sup>-1</sup> = I + ab<sup>T</sup> / (1 - a<sup>T</sup>b)


## Five steps of model-fitting
1. Define the equation(s) underlying the model
2. Map the data into the model equations.
3. Convert the equations into a metrix-vector equation.
4. Compute the parameters.
5. Statistical evaluation of the model

## Statistics terminology for linear algebrists
### GLM - General Linear Model
y = Xβ + ε

* Design Matrix X => Columns = independent variables, predictors, regressors etc...  Typically a tall matrix, so it only has 1 sided inverses.  Only works if it is full column rank.
* Regression coefficients β => The coefficients that multiply the independent variables in the model.

### Dependent variable y
The variable that is being predicted.

### Residuals vector ε
The difference between the predicted values and the actual values.
geometrically it's the line that is projected on to design matrix X.

### y hat (ŷ)
what the data would look like if the model captured all the relationships in the data.
This is the case when ε is zeros -- there's no noise in the data.

## Multicollinearity
When two or more independent variables in a regression model are highly correlated =>  when the columns of the design matrix are linearly dependent =>  same column repeated twice.

## Least Squares
A method for finding the best-fitting line through a set of points.  It is used when the points do not lie on a straight line.
Named because it minimizes the sum of the squares of the residuals.


## Normal Equation
X<sup>T</sup>Xβ = X<sup>T</sup>y

## Least Squares via Row Reduction
row reduction on X<sub>T</sub>Xy => Iβ

## QR decomposition
A matrix factorization technique that decomposes a matrix into an orthogonal matrix and an upper triangular matrix.

## Eigen Decomposition
A matrix factorization technique that decomposes a matrix into a matrix of eigenvectors and a diagonal matrix of eigenvalues.
Symmetric matrices have orthogonal eigenvectors.


## Characteristic Equation
* The equation that is used to find the eigenvalues of a matrix.

$$
determinant(A - λI) = 0
$$

## Eigenlayers
* The eigenvectors of a matrix that are associated with the same eigenvalue.


## Generalized Eigendecomposition
* A matrix factorization technique that decomposes a matrix into a matrix of generalized eigenvectors and a diagonal matrix of generalized eigenvalues.

Given two matrices S and R, the generalized eigenvectors are the vectors v that satisfy the equation Sv = λRv.
$$
Sv = λRv =>  (S-λR)v = 0  
$$


## Difference between eigenvectors and generalized eigenvectors
* Eigenvectors are the vectors that are not changed by a transformation.  Algebraically it is done using the identity matrix:
$$
Av = λIv
$$
* Generalized eigenvectors are the vectors that are scaled by a transformation.  Algebraically it is done using a different matrix (eg... R) than the identity matrix:
$$
Av = λRv
$$



## Singular value Decomposition (SVD)
A matrix factorization technique that decomposes a matrix into three matrices.

A = UΣV<sup>T</sup>

Where
* A is the original matrix (MxN)
* U is a matrix of eigenvectors of A * A<sup>T</sup> (MxM)
* Σ is a diagonal matrix of eigenvalues (MxN)
* V is a matrix of eigenvectors of A<sup>T</sup> * A (NxN)

On a symmetric matrix, U and V are the same.   Accounting for sign flips, U also will be the same (or very similar) to the eigenvectors of that matrix.

with exception for the nullspace of the matrices, the V from SVD is the same matrix as the V from the eigenvalue decomposition of A<sup>T</sup>A.   This usually means the first M columns of V are the same, where M represents the rank of matrix A.

The eigenvalues from Σ are the square roots of the eigenvalues from the eigenvalue decomposition of A<sup>T</sup>A.

Σ is a diagonal matrix where the single values are listed across the diagonal.  The Diagonal values are non-negative and are sorted in descending order.  Any zero-valued single values correspond to the nullspace of the matrix.  THe rank of the matrix corresponds to the non-zero singular values.

## Left inverse using the SVD
A<sup>-1</sup> = VΣ<sup>-1</sup>U<sup>T</sup>




## Four Subspaces
* Column space - The space spanned by the columns of a matrix. - Aka the range of a matrix.
* Null space - Aka the kernel of a matrix.  
* Row space - The space spanned by the rows of a matrix. AKA the range of the transpose of a matrix.
* Left null space - The null space of the transpose of a matrix. AKA the kernel of the transpose of a matrix.

The SVD provides orthogonal for the four subspaces.

## Spectral theory of matrices
You can represent a matrix as the sum of many simpler matrices, each invdividual matrix being a rank of 1.

## Condition Number
A measure of how sensitive a matrix is to changes in its elements.  It is the ratio of the largest singular value (ie... form the diagonal values of matrix Σ) to the smallest singular value.

Larger # => ill conditioned \
Smaller # => well conditioned \

Sometimes represented using the greek letter Kappa (κ)
the ratio of the leftmost value to the rightmost value in a scree plot of the singular values.




## Quadratic Form of a matrix
A quadratic form is a function that takes a vector as input and returns a scalar.  It is defined as w<sup>T</sup>Sx, where w is a vector and S is a square matrix: \
\
$
w^TSw
$
\
\
$ 
S = \begin{pmatrix} a & b \\ c & d \end{pmatrix} , 
w = \begin{pmatrix} x \\ y \end{pmatrix} 
$
\
\
therefore \
\
$
w^TSw = ax^2+(b+c)xy + dy^2
$

If matrix S is symmetric, then the transpose of w<sup>T</sup>Sx is w<sup>T</sup>Sx.  

Example: \
$
S = \begin{pmatrix} a & b \\ c & d \end{pmatrix} 
$

and therefore the quadratic expression simplifes to: \
$
w^TSw = ax^2+2bxy + dy^2
$

## Normalized Quadratic Form
A quadratic form that is normalized to have a unit length.  It is defined as 

$$
\frac{w^TSw}{w^Tw} 
$$
In R<sup>2</sup> this simplifies to
$$ 
\frac{ax^2+(b+c)xy + dy^2}{x^2 + y^2} 
$$

## Principal Component Analysis (PCA)
A technique that is used to reduce the dimensionality of a dataset by finding the directions of maximum variance in the data.

$ W\Lambda = SW $
    
* W is the matrix of eigenvectors of the covariance matrix of the data.
* Λ is the diagonal matrix of eigenvalues of the covariance matrix of the data.
* S is the covariance matrix of the data.

then ->
$ y=A^Tw_j $

* y is the component or score
* A is the data matrix
* $ w_j $ is the jth eigenvector of the covariance matrix of the data.  (aka factor, filter, or weight)

## Quadratic form of generalized Eigendecomposition
Given two matrices S and R, the generalized eigenvectors are the vectors v that satisfy the equation Sv = λRv.

Given a matrix W of generalized eigenvectors, R is the mass matrix (or metric matrix) of the generalized eigenvalue equation
* $ W^TW \neq I $
* $ W^TAW $ will be a diagonal matrix
* $ W^TRW $ will be the identity matrix


## Definiteness of a square matrix
The definiteness of a matrix is determined by the sign of the eigenvalues of the matrix. Ignore the zero point (origin).  


Category|Geometry|Eigenvalues|Invertibility
---|---|---|---
Positive definite|Convex|All positive|Always invertible
Positive semi-definite|Convex|All non-negative|No
Indefinite|Saddle|Some positive, some negative|Possibly
Negative semi-definite|Concave|All non-positive|No
Negative definite|Concave|All negative|Always invertible

## Properties of $ A^TA $
* it is a Square matrix
* It is a Symmetric matrix
* It is invertable if A is full column or full row rank
* It has orthogonal eigenvectors
* it has real eigenvalues
* If $ A^TA $ is full column rank, it is positive definite 
* If $ A^TA $ is not full column rank, it is positive semi-definite

## Properties of $ AA^T $
* If $ AA^T $ is full column rank, it is positive definite 
* If $ AA^T $ is not full column rank, it is positive semi-definite
 





















## Linear descriminant analysis / Fisher's Linear Discriminant
A technique that is used to find the linear combination of features that best separates two or more classes of data.


## LU decomposition
A matrix factorization technique that decomposes a matrix into a lower triangular matrix and an upper triangular matrix.