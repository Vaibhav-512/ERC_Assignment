#XOR Gate Implementation 

This is a Code to compute the XOR of two variables X1 and X2 and stores the result in Y.
XOR Function

X +Y ----> X xor Y

0 + 0 ------> 0

0 + 1 ------> 1

1 + 0------> 1

1 + 1 -----> 0

  XOR is a simple function which returns a truth value if the number of input bits true is odd. The following code is a simple Neural Network Classifier, works on the principle of Logistic regression in Machine Learning to perform the task.
It makes the use of torch, the machine learning library in python. The data is stored in the form of a tensor array.
A new model is created inside the class XOR(inbuilt). This comprises 2 inputs in the first layer,2 activation bubbles in the hidden layer, and a single output. An object 'self' is made of the class XOR. This will contain all the data we are working upon.
The algorithm calculates the activation of a layer of the neurons as

                     aL=g(zL)
where aL is the activation of the Lth layer (essentially a vector).zL is computed as follows:
 
                  zL = aL-1* wL-1+bL-1  
aL-1 is the activation vector/input vector of the previous layer and wL is a matrix that contains the weights/parameters we need to vary.bL-1 are the biases for the L-1 th layer. g is the sigmoid function that works on zL-1.
  
                              g(x)= 1/{1+e^{-x}


This function gives an output in the range (0,1) and essentially is used for scaling the features. The weights are first selected randomly for the input layer. The cost (loss) function is evaluated to get the mean squared error i.e, the square of the deviation of the hypothesis from the expected value

                         Loss(zL,yL)=sum(g(zL)-yL)^2

For this action, the MSELoss() function is used. A function 'forward' is used to feed forward the cost and the predicted value in the Lth layer. Another function backward() back propagates to update the value of the weights and biases of the previous layers so that the Cost Function of the final layer converges into a minimum.

It was found that the loss sufficiently converges to zero after 500 iterations of the model. A limiting value is achieved.
Besides this,an optimizer function SGD(){Stochastic Gradient Descent} is used to speed up the gradient descent. This function updates parameters corresponding to each training example of the matrix instead of multiplying the entire gradient matrix by a single value and hence speeds up the convergence of the Cost Function. The learning rate is set to a small value.

https://colab.research.google.com/drive/1J-Jz7d8ecWQyNshBKZ2oTv6JQSbTFRus?usp=sharing

