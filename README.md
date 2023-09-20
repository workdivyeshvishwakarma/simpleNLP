# **Simple NLP Model Training and Testing**

This repository contains a basic implementation of an NLP model trained
on a minimal dataset consisting of just one sentence: \"I am Divyesh\".
The primary goal of this exercise was to understand the mechanics of
neural networks and their training processes.

## **Table of Contents**

-   [[Overview]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#overview)

-   [[Implementation]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#implementation)

    -   [[Initialization]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#initialization)

    -   [[Forward
        > Pass]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#forward-pass)

    -   [[Backpropagation]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#backpropagation)

    -   [[Training
        > Loop]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#training-loop)

    -   [[Testing]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#testing)

-   [[Results]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#results)

-   [[License]{.underline}](https://chat.openai.com/c/f90a5b50-6cf5-4be3-ab1c-e3aae0fd119f#license)

## **Overview**

The model is a simple feedforward neural network with one hidden layer.
We use word embeddings and train the model to predict the next word in
the sequence.

## **Implementation**

### **Initialization**

First, we initialize the model parameters, including the weights (W1 and
W2) and biases (b1 and b2).

python

\# Pseudo code for initialization

input_size = len(tokens)

hidden_size = 3

output_size = len(tokens)

\# Weights and biases initialization

W1, b1, W2, b2 = initialize_parameters(input_size, hidden_size,
output_size)

### **Forward Pass**

We use the forward propagation to get the predicted output for a given
input. It involves processing the input data through each layer of the
network to get the output.

python

\# Pseudo code for forward pass

y_pred = forward(x)

### **Backpropagation**

Backpropagation helps adjust model parameters using the error between
predicted outputs and actual data. We compute the gradients of the loss
function with respect to model parameters.

python

\# Pseudo code for backpropagation

dL_dW1, dL_db1, dL_dW2, dL_db2 = backward(y_pred, target_index, a1)

### **Training Loop**

We train the model using a basic loop. Inside the loop, we predict the
next word using the forward pass, compute the loss, and then update the
model\'s weights and biases based on the error using backpropagation.

python

\# Pseudo code for the training loop

for epoch in range(num_epochs):

\# Forward pass, compute loss, backpropagation

\# Update weights and biases

### **Testing**

After training, we can use the model to predict the next word in the
sequence. The model uses the word embeddings to make its predictions.

python

\# Pseudo code for testing

predicted_word = predict_next_word(input_word)

## **Results**

Considering the size of the dataset and the simplicity of the sequence,
the model should predict \"am\" after \"I\" and \"Divyesh\" after
\"am\".

## **License**

This project is open-source and available to everyone. Please provide
attribution if you use the content elsewhere.
