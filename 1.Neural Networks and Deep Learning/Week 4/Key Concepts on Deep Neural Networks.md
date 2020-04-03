## Week 4 Quiz

Question 1. What is the "cache" used for in our implementation of forward propagation and backward propagation?

   - [ ] It is used to cache the intermediate values of the cost function during training.
   - [x] We use it to pass variables computed during forward propagation to the corresponding backward propagation step. It contains useful values for backward propagation to compute derivatives.
   - [ ] It is used to keep track of the hyperparameters that we are searching over, to speed up computation.
   - [ ] We use it to pass variables computed during backward propagation to the corresponding forward propagation step. It contains useful values for forward propagation to compute activations.

   Note: the "cache" records values from the forward propagation units and sends it to the backward propagation units because it is needed to compute the chain rule derivatives.

Question 2. Among the following, which ones are "hyperparameters"? (Check all that apply.) 

   - [x] number of layers L in neural network
   - [] bias vector b^[l]
   - [x] number of iterations
   - [] activation values a^[l]
   - [x] size of the hidden layer n^[l]
   - [x] learning rate α
   - [] weight matrices W^[l]
    
Question 3. Which of the following statements is true?

   - [x] The deeper layers of a neural network are typically computing more complex features of the input than the earlier layers. 
   - [ ] The earlier layers of a neural network are typically computing more complex features of the input than the deeper layers.

Question 4. Vectorization allows you to compute forward propagation in an L-layer neural network without an explicit for-loop (or any other explicit iterative loop) over the layers l=1, 2, …,L. True/False?

   - [ ] True
   - [x] False
   
   Note: We cannot avoid the for-loop iteration over the computations among layers.
    
Question 5. Assume we store the values for n^[l] in an array called layers, as follows: layer_dims = [n_x, 4,3,2,1]. So layer 1 has four hidden units, layer 2 has 3 hidden units and so on. Which of the following for-loops will allow you to initialize the parameters for the model?

   - [x] for(i in range(1, len(layer_dims))):
        parameter[‘W’ + str(i)] = np.random.randn(layers[i], layers[i - 1])) * 0.01
        parameter[‘b’ + str(i)] = np.random.randn(layers[i], 1) * 0.01
        
   - [] for(i in range(1, len(layer_dims)/2)):
           parameter[‘W’ + str(i)] = np.random.randn(layers[i], layers[i-1])) * 0.01
           parameter[‘b’ + str(i)] = np.random.randn(layers[i-1], 1) * 0.01
           
   - [] for(i in range(1, len(layer_dims)/2)):
           parameter[‘W’ + str(i)] = np.random.randn(layers[i], layers[i-1])) * 0.01
           parameter[‘b’ + str(i)] = np.random.randn(layers[i-1], 1) * 0.01
   - [] for(i in range(1, len(layer_dims)/2)):
           parameter[‘W’ + str(i)] = np.random.randn(layers[i], layers[i-1])) * 0.01
           parameter[‘b’ + str(i)] = np.random.randn(layers[i-1], 1) * 0.01

Question 6. Consider the following neural network: (Sadly, the image won't embed so i can't show it)

  - [x] The number of layers L is 4. The number of hidden layers is 3.
  - [ ] The number of layers L is 3. The number of hidden layers is 3.
  - [ ] The number of layers L is 4. The number of hidden layers is 4.
  - [ ] The number of layers L is 5. The number of hidden layers is 4.

Note: Yes. As seen in lecture, the number of layers is counted as the number of hidden layers + 1. The input and output layers are not counted as hidden layers.

Question 7. During forward propagation, in the forward function for a layer l you need to know what is the activation function in a layer (Sigmoid, tanh, ReLU, etc.). During backpropagation, the corresponding backward function also needs to know what is the activation function for layer l, since the gradient depends on it. True/False?

   - [x] True
   - [ ] False
    
   Note: Yes, as you've seen in the week 3 each activation has a different derivative. Thus, during backpropagation you need to know which activation was used in the forward propagation to be able to compute the correct derivative.
    
Question 8. There are certain functions with the following properties:

   (i) To compute the function using a shallow network circuit, you will need a large network (where we measure size by the number of logic gates in the network), but (ii) To compute it using a deep network circuit, you need only an exponentially smaller network. True/False?
    
   - [x] True
   - [ ] False
    
   Note: See lectures, exactly same idea was explained.
    
Question 9. Consider the following 2 hidden layer neural network:

   Which of the following statements are True? (Check all that apply), (Sadly, the image won't embed so i can't show it).

   - W^[1] will have shape (4, 4)
   - b^[1] will have shape (4, 1)
   - W^[2] will have shape (3, 4)
   - b^[2] will have shape (3, 1)
   - b^[3] will have shape (1, 1)
   - W^[3] will have shape (1, 3)
    
   Note: I only listed the correct ones.
    
Question 10. Whereas the previous question used a specific network, in the general case what is the dimension of W^[l], the weight matrix associated with layer l?

  - [x] W^[l] has shape (n^[l],n^[l−1])
    
    Note: I only listed the correct answer

Final Note: This is about the answers I did not list (I'm really sorry). This is because there were too many answers or the answers contained subscripts and superscripts which are really hard to write!
