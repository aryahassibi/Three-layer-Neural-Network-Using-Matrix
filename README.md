# Three-layer Neural Network ( Using Matrix )
This Neural network is written in Python (3.7.6) <br>
All of the matrix calculations of this neural network are done by matrix.py.

# **Neural Network**

This Neural network is a a basic three-layer netwrok that you can solve simple problems (e.g., XOR, some non-linear problems, etc.) with.
> *note:* The Activation function of this neural netwrok is the ***sigmoid*** function 
### *HOW TO USE IT:*
1. import Class
      
        from neuralNetwork import *
        
        
2. Create an Object

        nn = Neuralnetwork(number_of_input_nodes, number_of_hidden_nodes, number_of_output_nodes)

    > *note:* number_of_input_nodes, number_of_hidden_nodes and number_of_output_nodes could be what ever you want.
    
    
3. Generate the inputs and the targets that you wnat to train your netwrok with

    <br>For training the neural netwrok you should use **train()** method: 
          
        nn.train(input_array, target_array)

    > *note:* length of **input_array** should be equal to **number_of_input_nodes** <br>
    >    and lenght of **target_array** should be equal to **number_of_output_nodes**

    for example this time we are gonna train the neural netwrok to solve XOR problem:
    
          inputs = [[0, 0], [1, 0], [1, 1], [0, 1]]
          targets = [[0], [1], [0], [1]]

          # Training the neural network 10000 times
          for j in range(10000):
              i = randint(0, 3)
              nn.train(inputs[i], targets[i])

4. Getting neural network prediction
    <br>For Getting predictions you should use **predict()** method:

        nn.predict(input_array)

    > *note:* length of **input_array** should be equal to **number_of_input_nodes**

    Again we continue with XOR problem.<br>
    For getting the result after trianing the neural network you can do this:
    
        inputs = [[0, 0], [1, 0], [1, 1], [0, 1]]

        for i in range(4):
          o = nn.predict(inputs[i])
          print("XOR", inputs[i], " ≈ ", o[0])

    *output:*
    
        XOR [0, 0]  ≈  0.09681844789560402
        XOR [1, 0]  ≈  0.8642830639305592
        XOR [1, 1]  ≈  0.16421678094863154
        XOR [0, 1]  ≈  0.8545802569550945

  

