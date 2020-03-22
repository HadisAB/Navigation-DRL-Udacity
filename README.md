# Navigation-DRL-Udacity
P1-Navigation- Udacity Deep Reinforcement Learning Nanodegree Program

## Project details

### Description
For this project, I will train an agent to navigate (and collect yellow bananas!) in a large, square world.

### Goal
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of agent is to collect as many yellow bananas as possible while avoiding blue bananas.
The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

### States and actions
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:<br/>

0 - move forward.<br/>
1 - move backward.<br/>
2 - turn left.<br/>
3 - turn right.

## Getting Started
### Environment
The used environment for Windows 64 :
[Banan Envoronment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

### Framework: 
anaconda-spyder4 - python 3.6 - pytorch

## Instructions
I have solved the project by Deep Q-Networks and also considering the 'Experience Replay' and 'Fixed Q Targets' to improvement the training. You can find the solution by refering to [training code](https://github.com/HadisAB/Navigation-DRL-Udacity/tree/master/Training%20code) and using below clarification. <br/>
To find the details of how you should use the code, refer to the [report](https://github.com/HadisAB/Navigation-DRL-Udacity/blob/master/Report.md). 




