# udacity-unityMLagents-navigation
udacity navigation programming assignment learning to pick up yellow bananas within unity MLagents

# Project Details 
In this project, we trained a DRL agent with the Unity ML-Agents environment to selectively collect bananas in a virtual (digitally simulated) square room. 

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 values and contains the agent's velocity, along with ray-based perception of objects in the agent's forward view. Given this information, the agent has to learn how to select optimal navigation actions. Four discrete actions are available, corresponding to moving forward (value 0), backward (1), and turning left (2) and right (3).

The task is episodic, and the problem is considered 'solved' after achieving a score of 13 or greater over the trailing 100 episodes.  

# Getting Started
The project is comprised of three files:
1. **navigation.ipynb**: imports packages, connects to Unity environment, and then runs the learning function that will interact with that environment, storing the results in a NN defined in model.py
2. **model.py**: contains the pytorch neural network, containing two (fully connected) hidden layers and using RELU activation functions in between
3. **dqn_agent.py**: contains the code to initialize the two Q networks, a replay buffer, and wrappers for selecting actions, submitting them to the environment (through 'step') and then learn from experience stored in the replay buffer

Logically, there are three steps required in order to execute the project: Download the files referred to above, install the necessary Unity MLAgents environment, and execute the code in the environment of your choice, such as a Jupyter Notebook environment (which is recommended for simplicity).  Here are the more detailed instructions for doing so:
1. Download the three files above (from the public github repo)\ 
Execute this command (at a shell prompt, in the appropriate source repo location where you wish to copy the files):\
$ *git clone https://github.com/kamccall/udacity-unityMLagents-navigation* \
This will clone the entire repository - including the three source files as well as associated README and REPORT files - into that source directory. 
1. Install the Unity MLAgents environment (within which the agent will train and subsequently execute).\ 
Follow the directions below in order to install the needed 'navigation' environment for Unity MLAgents:\
https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation#getting-started
1. Execute the code (either within a Jupyter Notebook environment, or within an alternative IDE).\
There are dependencies upon various Python packages in order to successfully execute this project, such as numpy, pyplot, torch, and others. Depending upon your Python environment, it is likely that those packages are already installed, in which case the 'import' commands in the code will successfully execute, thereby allowing the use of the code in those packages.\
If your environment does not already have all of these packages installed, it is possible that you will need to install one or more packages before you can successfully execute the 'import' command to utilize them.  If that is the case:
    1. ADD a new cell at the top of your Jupyter notebook
    1. Follow the appropriate directions in this link to install the required packages (which will be different depending upon whether you are using 'pip' or 'conda' as your package manager): https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/

# Build and Test Instructions
There are three ways to run the code:
1. Install all three files in the same directory, and execute the navigation .ipynb notebook file in a Jupyter notebook server , or
2. Insert the code from 'model.py' and 'dqn_agent.py' into new (inserted) cells in the .ipynb notebook file, and execute everything from the single notebook file within a Jupyter notebook environment, or
3. (More difficult): Copy and paste the Python code from within the .ipynb notebook file into a Python source code file, and then execute the program from the command line (with all appropriate dependencies based on your IDE and OS)

