* Which of the following are true? (Check all that apply.)


    1. X is a matrix in which each column is one training example.
    2. X is a matrix in which each row is one training example.
    3. a[2](12) denotes activation vector of the 12th layer on the 2nd training example.
    4. a(4)[2] is the activation output by the 4th neuron of the 2nd layer
    5. a[2] denotes the activation vector of the 2nd layer.
    6. a(4)[2] is the activation output of the 2nd layer for the 4th training example
    7. a[2](12) denotes the activation vector of the 2nd layer for the 12th training example.

    Correct : 1,4,5,7

* The tanh activation usually works better than sigmoid activation function for hidden units because the mean of its output is closer to zero, and so it centers the data better for the next layer. True/False?

    **True**

*  Which of these is a correct vectorized implementation of forward propagation for layer ll, where 1≤l≤L ?
    
    Correct  : Z[l] = W[l]A[l-1] + B[l]

               A[l] = g[l](Z[l])

* You are building a binary classifier for recognizing cucumbers (y=1) vs. watermelons (y=0). Which one of these activation functions would you recommend using for the output layer?

    1. ReLU
    2. Leaky ReLU
    3. sigmoid
    4. tanh

    Correct : 3

* Consider the following code:

    A = np.random.randn(4,3)
    
    B = np.sum(A,axis = 1,keepdims= True)

    What will be B.shape? (If you’re not sure, feel free to run this in python to find out).

    1. (, 3)
    2. (4, )
    3. (4, 1)
    4. (1, 3)

    Correct : 3

* Suppose you have built a neural network. You decide to initialize the weights and biases to be zero. Which of the following statements is true?


    1. Each neuron in the first hidden layer will perform the same computation. So even after multiple iterations of gradient descent each neuron in the layer will be computing the same thing as other neurons.
    2. Each neuron in the first hidden layer will perform the same computation in the first iteration. But after one iteration of gradient descent they will learn to compute different things because we have “broken symmetry”.
    3. Each neuron in the first hidden layer will compute the same thing, but neurons in different layers will compute different things, thus we have accomplished “symmetry breaking” as described in lecture.
    4. The first hidden layer’s neurons will perform different computations from each other even in the first iteration; their parameters will thus keep evolving in their own way.

    Correct : 1

* Logistic regression’s weights w should be initialized randomly rather than to all zeros, because if you initialize to all zeros, then logistic regression will fail to learn a useful decision boundary because it will fail to “break symmetry”, True/False?

    **False**

* You have built a network using the tanh activation for all the hidden units. You initialize the weights to relative large values, using np.random.randn(..,..)*1000. What will happen?


    1. This will cause the inputs of the tanh to also be very large, thus causing gradients to also become 2.large. You therefore have to set \alphaα to be very small to prevent divergence; this will slow down learning.
    2. It doesn’t matter. So long as you initialize the weights randomly gradient descent is not affected by whether the weights are large or small.
    3. This will cause the inputs of the tanh to also be very large, thus causing gradients to be close to zero. The optimization algorithm will thus become slow.
    4. This will cause the inputs of the tanh to also be very large, causing the units to be “highly activated” and thus speed up learning compared to if the weights had to start from small values.

    Correct  : 3

* From the neural network below : 

    ![Neural Network](./img/nn_1.png)

    Correct: W[1] : (4,2)
             b[1] : (4,1)
             W[2] : (1,4)
             b[2] : (1,1)

* In the same network as the previous question, what are the dimensions of Z[1] and A[1] ?

    1. Z[1] and A[1] are (1,4)
    2. Z[1] and A[1] are (4,2)
    3. Z[1] and A[1] are (4,m)
    4. Z[1] and A[1] are (4,1)

    Correct : 3




