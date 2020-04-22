The implementation to solve this project is a fixed target DQN using a pytorch neural network. 

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

As seen below the agent quickly learns to achieve a target >13, and tends to stay around a score of ~16.
![Score over time and average](https://github.com/chrismelba/udacity-dqn/blob/master/Score-over-time.png)

To improve this agent we could implement a number of things:
We could build a prioritized replace experience buffer, so that rare states were more likely to be learned from.
We could create a double DQN, using w- to evaluate the next action
We could create a dueling DQN using different layers for the state evaluation and next action evaluation. 

We could create a "rainbow" agent using multiple of these ideas. 