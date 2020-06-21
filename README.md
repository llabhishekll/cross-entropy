# Cross-Entropy Method

![asset00001](asset/asset00001.png)

The **cross-entropy method** iteratively suggests a small number of neighboring policies, and uses a small percentage of the best performing policies to calculate a new estimate.

The **evolution strategies** technique considers the return corresponding to each candidate policy. The policy estimate at the next iteration is a weighted sum of all of the candidate policies, where policies that got higher return are given higher weight. 

## More about Black-Box Optimization

**Cross-Entropy** and **Evolution Strategies** method can be classified as **black-box optimization** techniques. **Black-box** refers to the fact that in order to find the value of θ that maximizes the function J=J(θ), we need only be able to estimate the value of J at any potential value of θ. 

That is algorithm don't know that we're solving a reinforcement learning problem, and they do not care that the function we're trying to maximize corresponds to the expected return. These algorithms only know that for each value of θ, there's a corresponding **number**. 

We know that this **number** corresponds to the return obtained by using the policy corresponding to θ to collect an episode, but the algorithms are not aware of this. To the algorithms, the way we evaluate θ is considered a black box, and they don't worry about the details. The algorithms only care about finding the value of θ that will maximize the number that comes out of the black box.

## Why Policy-Based Methods?

There are three reasons why we consider policy-based methods:

1. **Simplicity**: Policy-based methods directly get to the problem at hand (estimating the optimal policy), without having to store a bunch of additional data (i.e., the action values) that may not be useful.
2. **Stochastic policies**: Unlike value-based methods, policy-based methods can learn true stochastic policies.
3. **Continuous action spaces**: Policy-based methods are well-suited for continuous action spaces.

## Instructions

This project is a part of [Udacity Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893). Open `CEM.ipynb` to see an implementation of the cross-entropy method with OpenAI Gym's MountainCarContinuous environment.
