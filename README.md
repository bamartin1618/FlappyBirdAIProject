# FlappyBirdAIProject
The code repository for the Flappy Bird AI Project, containing both versions of the game: the control and experimental groups.

In this project, we wanted to compare the training phases of two ANN models that were trained to play Flappy Bird using the NEAT algorithm. The <a href = "https://en.wikipedia.org/wiki/Neuroevolution_of_augmenting_topologies">NEAT</a> algorithm is an approach in deep reinforcement learning founded by Kenneth Stanley. The approach uses evolutionary algorithms to improve an agent over time, inspired by Darwinian concepts such as natural selection.

In NEAT, the performance of a neural network is evaluated by a fitness function. The fitness function is a predetermined mathematical equation that estimates the performance of the network based on factors we are trying to optimize, such as points scored. In this project, we trained a model using a simple, linear fitness function, which was our control group. For this group, we simply evaluated the neural networks by their lifespan in milliseconds. 

<img src="https://latex.codecogs.com/gif.latex?f_{\text{control}}&space;=&space;t_{\text{death}}-t_{\text{control}}" title="f_{\text{control}} = t_{\text{death}}-t_{\text{control}}" />

For the second group, the model's fitness function was a function of points scored and jumps made.

<img src="https://latex.codecogs.com/gif.latex?f_{\text{experimental}}&space;=&space;\text{points}^{2}&space;\times&space;e^{-0.001&space;\cdot&space;\text{jumps}}" title="f_{\text{experimental}} = \text{points}^{2} \times e^{-0.001 \cdot \text{jumps}}" />

In addition, there are differences in the ANN architecture and NEAT configurations of the two models. For the control group, two-hundred birds are in a generation and each neural network has six input neurons, five hidden neurons, and one output neurons. For the experimental group, four-hundred birds are in a generation and each neural network has six input neurons, nine hidden neurons, and one output neuron. However, everything else was the same for the two models. The birds in each model start at the same point, obstacles are generated randomly, and the birds travel at the same speed. By setting these control variables, this allows us to run both models and compare the results of the training phases by recording the performances of the generations. Our guidelines for the best model were which model was more consistent during the training phase and which model plateaued and converged to an optimal set of weights faster. The answer to these questions will help us discern which fitness function and ANN architecture was better suited to the Flappy Bird environment.

The data analysis and results to our experiment can be found <a href = "https://github.com/bamartin1618/FlappyBirdAIProject/blob/main/FlappyAIDataAnalysis.ipynb">here.</a>
