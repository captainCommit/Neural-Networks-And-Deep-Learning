* What does a neuron compute?

    1. A neuron computes the mean of all features before applying the output to an activation function
    2. A neuron computes a function g that scales the input x linearly (Wx + b)
    3. A neuron computes an activation function followed by a linear function (z = Wx + b)
    4. A neuron computes a linear function (z = Wx + b) followed by an activation function

    Correct : 4

* Which of these is the "Logistic Loss"?

    Correct : L(y,yhat) = y.log(yhat) + (1-y)log(1-yhat) 

* Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector?


    1. x = img.reshape((32*32,3))
    2. x = img.reshape((1,32*32,*3))
    3. x = img.reshape((32*32*3,1))
    4. x = img.reshape((3,32*32))

    Correct : 3

* Consider the two following random arrays "a" and "b":
    a = np.random.randn(2,3)
    b = np.random.randn(2,1)
    c = a+b

    What will be the shape of "c"?

    1.  c.shape = (2, 3)
    2.  c.shape = (3, 2)
    3.  c.shape = (2, 1)
    4.  The computation cannot happen because the sizes don't match. It's going to be "Error"!

    Correct : 1

* Consider the two following random arrays "a" and "b":
    a = np.random.randn(4,3)
    b = np.random.randn(3,2)
    c = a*b

    What will be the shape of "c"?

    1.  c.shape = (4, 2)
    2.  c.shape = (4, 3)
    3.  c.shape = (3, 3)
    4.  The computation cannot happen because the sizes don't match. It's going to be "Error"!

    Correct : 4

* Suppose you have n_x input features per example. Recall that X = [x^{(1} x^{(2)} ... x^{(m)}]X=[x (1) x^(2)...x^(m)]. What is the dimension of X?

    1. (m,n_{x})
    2. (1,m)
    3. (n_{x},m)
    4. (m,1)

    Correct : 3

* Recall that "np.dot(a,b)" performs a matrix multiplication on a and b, whereas "a*b" performs an element-wise multiplication.Consider the two following random arrays "a" and "b":
    
    a = np.random.randn(12288,150)
    b = np.random.randn(150,45)
    c = np.dot(a,b)

    What is the shape of c?

    1. c.shape = (12288, 45)
    2. c.shape = (150,150)
    3. The computation cannot happen because the sizes don't match. It's going to be "Error"!
    4. c.shape = (12288, 150)

* Consider the following code snippet:

    a.shape = (3,4)
    b.shape = (4,1)
    for i in range(3):
    for j in range(4):
        c[i][j] = a[i][j] + b[j]

    How do you vectorize this?


    1. c = a.T + b
    2. c = a.T + b.T
    3. c = a + b.T
    4. c = a + b

    Correct : c = a +b.T

* Consider the follwong code

    a = np.random.randn(3, 3)
    b = np.random.randn(3, 1)
    c = a*b

    What will be c? (If you’re not sure, feel free to run this in python to find out).


    1. This will invoke broadcasting, so b is copied three times to become (3,3), and *∗ is an element-wise product so c.shape will be (3, 3)
    2. This will invoke broadcasting, so b is copied three times to become (3, 3), and *∗ invokes a matrix multiplication operation of two 3x3 matrices so c.shape will be (3, 3)
    3. This will multiply a 3x3 matrix a with a 3x1 vector, thus resulting in a 3x1 vector. That is, c.shape = (3,1).
    4. It will lead to an error since you cannot use “*” to operate on these two matrices. You need to instead use np.dot(a,b)

    Correct : 1

* Consider the following computation graph.

    ![computation_graph](./img/cg.png)



    1. J = (c - 1)*(b + a)
    2. J = (a - 1) * (b + c)
    3. J = a*b + b*c + a*c
    4. J = (b - 1) * (c + a)

    Correct : 2

