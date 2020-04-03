## Week 1 Quiz

Question 1. What does a neuron compute?

- [ ] A neuron computes an activation function followed by a linear function (z = Wx + b)
- [ ] A neuron computes a function g that scales the input x linearly (Wx + b)
- [ ] A neuron computes the mean of all features before applying the output to an activation function
- [x] A neuron computes a linear function (z = Wx + b) followed by an activation function

Note : Correct, we generally say that the output of a neuron is a = g(Wx + b) where g is the activation function (sigmoid, tanh, ReLU, ...).

Question 2. Which of these is the "Logistic Loss"?

- [x] L(i)(y^(i),y(i))=−(y(i)log(y^(i))+(1−y(i))log(1−y^(i)))
- [ ] L(i)(y^(i),y(i))=∣y(i)−y^(i)∣
- [ ] L(i)(y^(i),y(i))=max(0,y(i)−y^(i))
- [ ] L(i)(y^(i),y(i))=∣y(i)−y^(i)∣2

Note : Correct, this is the logistic loss you've seen in lecture!

Question 3. Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector?

- [ ] x = img.reshape((1,32*32,*3))
- [ ] x = img.reshape((3,32*32))
- [x] x = img.reshape((32*32*3,1))
- [ ] x = img.reshape((32*32,3))


Question4. Consider the two following random arrays "a" and "b":
a = np.random.randn(2, 3) # a.shape = (2, 3)
b = np.random.randn(2, 1) # b.shape = (2, 1)
c = a + b
What will be the shape of "c"?

- [ ] c.shape = (2, 1)
- [ ] c.shape = (3, 2)
- [ ] The computation cannot happen because the sizes don't match. It's going to be "Error"!
- [x] c.shape = (2, 3)

Note: Correct
Yes! This is broadcasting. b (column vector) is copied 3 times so that it can be summed to each column of a.


Question 5. Consider the two following random arrays "a" and "b":
What will be the shape of "c"?

- [x] The computation cannot happen because the sizes don't match. It's going to be "Error"!
- [ ] c.shape = (3, 3)
- [ ] c.shape = (4,2)
- [ ] c.shape = (4, 3)

Note :Correct, Indeed! In numpy the "*" operator indicates element-wise multiplication. It is different from "np.dot()". If you would try "c = np.dot(a,b)" you would get c.shape = (4, 2).

Qusetion6. Suppose you have n_x input features per example. Recall that X = [x^{(1)} x^{(2)} ... x^{(m)}]. 
What is the dimension of X?

- [ ] (1,m)
- [ ] (m,1)
- [ ] (m,n_x)
- [x] (n_x, m)

Question7. Recall that "np.dot(a,b)" performs a matrix multiplication on a and b, whereas "a*b" performs an element-wise multiplication.
Consider the two following random arrays "a" and "b":

a = np.random.randn(12288, 150) # a.shape = (12288, 150)
b = np.random.randn(150, 45) # b.shape = (150, 45)
c = np.dot(a,b)
What is the shape of c?

-[x] c.shape = (12288, 45)
-[ ] c.shape = (12288, 150)
-[ ] c.shape = (150,150)
-[ ] The computation cannot happen because the sizes don't match. It's going to be "Error"!

Note: Correct, remember that a np.dot(a, b) has shape (number of rows of a, number of columns of b). The sizes match because :
"number of columns of a = 150 = number of rows of b"

