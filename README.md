# udacity-unityMLagents-navigation
udacity navigation programming assignment learning to pick up yellow bananas within unity MLagents

# Project Details 
In this project, we trained a DRL agent with the Unity ML-Agents environment to selectively collect bananas in a virtual (digitally simulated) square room. 

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 values and contains the agent's velocity, along with ray-based perception of objects in the agent's forward view. Given this information, the agent has to learn how to select optimal navigation actions. Four discrete actions are available, corresponding to moving forward (value 0), backward (1), and turning left (2) and right (3).

The task is episodic, and the problem is considered 'solved' after achieving a score of 13 or greater over the trailing 100 episodes.  

# Getting Started
The project is comprised of three files:
1. navigation.ipynb: imports packages, connects to Unity environment, and then runs the learning function that will interact with that environment, storing the results in a NN defined in model.py
2. model.py: contains the pytorch neural network, containing two (fully connected) hidden layers and using RELU activation functions in between
3. dqn_agent.py: contains the code to initialize the two Q networks, a replay buffer, and wrappers for selecting actions, submitting them to the environment (through 'step') and then learn from experience stored in the replay buffer

There are dependencies upon various Python packages such as numpy, pyplot, and (very importantly) Pytorch and Unity, but those packages are automatically imported as a result of running the cells. 

# Build and Test Instructions
There are two ways to run the code:
1. Install all three files in the same directory, and execute the navigation notebook in a notebook server, or
2. Insert the code from 'model.py' and 'dqn_agent.py' into additional (inserted) cells in the notebook file, and execute everything from the single notebook file
