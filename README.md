Classifying MNIST handwritten digits from [Yann LeCun's MNIST Dataset](http://yann.lecun.com/exdb/mnist/).

This databaset has a training set of 60,000 examples, and a test set of 10,000 examples. Images were centered, with sizing of 28x28.

Now, this dataset is particularly interesting, as it is provided in the IDX file format, which is a simple format for vectors and multidimensional matrices 
of various numerical types. And it is so lightweight that it is the case that I provide a copy of such data in the data folder, so you can get up and running with this notebook yourself.

It comes with its trade off of not being very friendly to unpack and to so read. For that I created a separeated module called mnist_load.ipynb to extract
and prepare the data to be fed to our model. Note that this module is indeed a notebook, and to make it available as a python module inside jupyuter notebook,
you have to import this little python script I found online called ipynb_reader. It's in the root folder in case you wanna check it out.

With mnist_load taking care of all the complexity involving data, I created another notebook called mnist_impl.ipynb, containig the model.

In have implemented multiple architectural improvements during this development, and my intention in the notebook is to walk you through each of them,
so you can see and measure by yourself.

   - I start by trying out a two layer neural net with a simple linear function and stochastic gradient descent.
   - Move on to a three layer neural net with a nonlinear activation function(relu) and backpropagation. 
   - Prevent overfitting to a greater extent by adding dropout in the next interation.
   - Get better at parameter updates by adding batch gradient descent
   - Change activation function in hidden layer to tanh, to help us model selective correlation
   - Add softmax as output activation function so as to predict _which digit is more lokely_ instead of a single digit, and then we pick the one with the highest prediciton.
   - A FULL BLOWN CNN, that's right, from scratch. Very cool stuff.

Now, all of these iterations can be rather overwhelming, so I recommend you go checkout the challenge notebook in case you wanna skip through the process.

There I've added useful comments to the code and only implemented the final solution to this classification problem from memory.


