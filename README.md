# udacity-dqn
Submission of DQN assingment for udacity Reinforcement Learning Course

This assignment trains an agent for use in the unity environment trying to eat yellow bananas while avoiding blue bananas. 

The agent used in this project utilizes a pytorch neural network with 4 layers:

-Input layer: size of the state space (37 units)
-Fully connected layer: 64 units
-Second fully connected layer: 64 units
-Output layer: the size of the action space (4 units)

The agent uses a fixed target DQN, the hyper-parameters were chosen to mimic successful agents in previous exercises:
Buffer Size: 10,000
Batch Size: 64 
Gamma (discount factor): 0.99
Tau (soft update of NN): 0.001 
Learning Rate: 0.0005 - small learning rates are critical in DQN
Update_every 4 steps
Training Steps: initially 2000, but could be reduced to 700 as no learning seems to take place beyond that.


![Score over time and average](https://octodex.github.com/images/yaktocat.png)
