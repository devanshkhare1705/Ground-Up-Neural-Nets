# ground-up-neural-nets
Building neural networks without PyTorch

## Motivation

This exercise is based on Andrej Karpathy's YouTube series on understanding the first principles of neural networks [1].

I've built deep neural network architectures with PyTorch before. My objective in implementing this ground-up small-scale neural network is not to optimize for performance and efficiency. Instead, I wanted to implement it for three reasons:

1) To understand the low-level knobs and levers that impact complex deep learning architectures. How can I take the robustness of my neural networks to the next level?

2) To identify shortcomings in the state-of-the-art today. What ideas do we treat as immutable truths, when they were just one of the many options before their widespread adoption?

3) To develop intuition for borrowing ideas from different fields for ML. How did researchers attack problems that nobody had answers for, to eventually create something that could change society?


## Technical Implementation

Four custom classes have been created in this exercise: Value, Neuron, Layers, and MLP. 

Value is used to capture the network’s parameters. Compared to scalar parameters, Value parameters enable three additional functionalities: topological search for backward pass, computation & storage of gradients, and visualisation of the network.

Neuron is used to instantiate single neurons in each layer. It initialises the input weights and biases from the previous layer for each neuron.

Layer sets up the desired number of neurons in each layer.

And MLP sets up the desired layers in each network.

Custom functions are also written to run the training loop, forward pass, backward pass, and weight updates.

The neural network is then trained on a tiny dataset of 4 vectors to observe its behaviour with time, and its final version is visualized using a combination of custom and graphviz methods.

## Citations
[1] https://www.youtube.com/watch?v=VMj-3S1tku0
