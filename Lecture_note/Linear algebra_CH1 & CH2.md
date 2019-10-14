
## Lecture by joo-jae-gul professor from Korea univ.

### CHAPTER 1 
    - Scalar, Vector, Matrix
        - Scalar = a single number
        - Vector = an ordered list of numbers(한방향 1-dimensional)
        - Matrix = a two-dimensional array of numbers
        - Row vector : a horizontal vector
        - Column vector : a vertical vector 

    - Matrix
        - Square matrix
        - Rectangular matrix
        - Transpose of matrix

        <characteristic>
        - Matrix multiplication is NOT commutative
        - Distributive
        - Associative
        - Property of transpose

        - (1x3)(3X1) -> inner product (내적)
        - (3x1)(1x2) -> outer product (외적)
    
    - Row Vector, Column Vector  
        - column <- transpose -> row

### CHAPTER 2 

    - bold small letter = vector, non-bold small letter = scalar, Big letter = Matrix
    - Linear Equation
        - Identity Matrix (= square matrix)(항등 행렬)
            - any vector mutilple identiy matrix = same vector
        - Inverse Matrix (역행렬)
            - Can discuss about Inverse Matrix only in square Matrix
            - if ad - bc = 0, Matrix A is non-invertible.
                - ad - bc = determinant, det A = ad - bc of Matrix A
            - non-invertible matrix
                - no solution or infinitely many solutions

    - Linear system
        - a set of linear quations

####    CHAPTER2 Practice
#####   https://towardsdatascience.com/linear-algebra-cheat-sheet-for-deep-learning-cd67aba4526c
    
'''python
    
    import numpy as np

    # column vector
    c = np.array([1,2,3])
    print(c.shape)

    # obtaining a particular entry
    print (c[0])

    # row vector
    r = np.array([ [1,2,3] ])

    # creating a matrix with all zeros
    a = np.zeros((2,2))

    # creating a matrix with all ones
    b = np.ones((2,2))
                    
    # creating a matrix filled with the same constant
    c = np.full((2,2), 7)
                    
    # creating a matrix with random values
    d = np.random.random((2,2))

    # creating a matrix
    A=np.array([[1,2],[3,4],[5,6]])

    # creating another matrix
    B=np.array([[11,12,13,14],[15,16,17,18]])

    # transpose a matrix
    A.T

    # matrix-matrix multiplication
    np.dot(A,B)

    # identity matrix 
    eye3 = np.eye(3)

    # computing an inverse
    from numpy.linalg import inv
    A_inv = inv(A)

    # coefficient matrix A and a vector b
    A=np.array([[60, 5.5, 1],[65, 5.0, 0],[55, 6.0, 1]])
    b=np.array([66, 70, 78])

    # solution of a linear system
    x=A_inv.dot(b)

    # a better way to solve the same linear system
    from numpy.linalg import solve
    x = solve(A,b)
    
'''

####    CHAPTER2 Linear Combination & Span
    - vector with weights or coefficients
    - the weights in a linear combination can be any real numbers, including zero.
    
