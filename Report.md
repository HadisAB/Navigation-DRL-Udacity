# Navigation-DRL-Udacity Report
Udacity Deep Reinforcement Learning Nanodegree Program
P1-Navigation
used environments: anaconda-spyder4 - python 3.6

### Description
For this project, I will train an agent to navigate (and collect bananas!) in a large, square world.

### Goal
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.
The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### States and actions
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:<br/>

0 - move forward.<br/>
1 - move backward.<br/>
2 - turn left.<br/>
3 - turn right.

### Environment
The used environment for Windows 64 :
[Banan Envoronment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)


### Solution
I have solved the project by Deep Q-Networks and also considering the 'Experience Replay' and 'Fixed Q Targets' to improvement the training.

model.py : This is a neural network consists of two hidden layers with 64 nodes. I have also used Relu function as activation function.
dqn_agent.py : This is a class of agents activites which make agent trained. 
In this part, the agent will take samples in RelayBuffer and also will be trained for each 4 steps. Consider below used functions for more details:
Agent class:
step() : It stores a step taken by the agent in the Replay Buffer. Then the agent will be learnt Every 4 steps.
act(): This returns actions for the given state based on an Epsilon-greedy.
learn(): This update the Neural Network value parameters.
soft_update(): It updates the value from the target Neural Network from the local network weights (That's part of the Fixed Q Targets technique).

ReplayBuffer class:
It implements a fixed-size buffer to store experience tuples (state, action, reward, next_state, done)
add(): It appends the samples to the memory
sample(): It randomly samples a batch of experience steps in the memory.

### used parameters
BUFFER_SIZE = int(1e5)  # replay buffer size
BATCH_SIZE = 64         # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR = 5e-4               # learning rate 
UPDATE_EVERY = 4        # how often to update the network

### Result






