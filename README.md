# Three-layer Neural Network ( Using Matrix )
This [Neural Network](#neural-network) is written in Python (3.7.6) <br>
All of the matrix calculations of this neural network are done by [matrix.py](#matrix).

## **Neural Network**

Three-layer Neural network is a basic neural network that you can solve simple problems with(e.g., XOR, some non-linear problems, etc.).
> *note:* The Activation function of this neural network is the ***sigmoid*** function 
### *HOW TO WORK WITH neuralNetwork.py:*
1. Import Class
      
        from neuralNetwork import *
        
        
2. Create an Object

        nn = Neuralnetwork(number_of_input_nodes, number_of_hidden_nodes, number_of_output_nodes)

    > *note:* number_of_input_nodes, number_of_hidden_nodes and number_of_output_nodes could be whatever you want.
    
    
3. Generate the inputs and the targets that you want to train your network with

    <br>For training the neural netwrok you should use **train()** method: 
          
        nn.train(input_array, target_array)

    > *note:* length of **input_array** should be equal to **number_of_input_nodes** <br>
    >    and lenght of **target_array** should be equal to **number_of_output_nodes**

    for example this time we are going to train the neural netwrok to solve XOR problem:
    
        inputs = [[0, 0], [1, 0], [1, 1], [0, 1]]
        targets = [[0], [1], [0], [1]]

        # Training the neural network 10000 times
        for _ in range(10000):
            index = randint(0, 3)
            nn.train(inputs[index], targets[index])

4. Getting neural network prediction
    <br>For Getting predictions you should use **predict()** method:

        nn.predict(input_array)

    > *note:* length of **input_array** should be equal to **number_of_input_nodes**

    Again we continue with XOR problem.<br>
    For getting the result after trianing the neural network you can do this:
    
        inputs = [[0, 0], [1, 0], [1, 1], [0, 1]]

        for i in range(4):
            output = nn.predict(inputs[i])[0]
            print("XOR", inputs[i], " ≈ ", output)

    *output:*
    
        XOR [0, 0]  ≈  0.09681844789560402
        XOR [1, 0]  ≈  0.8642830639305592
        XOR [1, 1]  ≈  0.16421678094863154
        XOR [0, 1]  ≈  0.8545802569550945
      
      
## Matrix
Matrix is a class that is capable of doing some simple 2d-matrix calculations.

### *HOW TO WORK WITH matrix.py:*
1. Import class
      
            from matrix import *
            
2. Create an Object

            matrix = Matrix(number_of_rows, number_of_columns)
      > *note:* When you create a new object, the new matrix is filled with **0**<br>
      > you can use randomize method to assign a random number( between -1 and 1 ) to each element of the matrix
 
<br>
      
+ Each matrix has 4 different properties:
    1. number of rows

                  matrix.rows
    2. number of columns

                  matrix.cols
    3. shape of the matrix (number_of_rows, number_of_columns)

                  matrix.shape
    4. the data stored in the matrix<br>
          All of the data is  stored in a python list<br>
          and you can access the data by using:

                  matrix.data
                  
> *note:* See all of the methods and read about their functionality in matrix.py 
            
           

