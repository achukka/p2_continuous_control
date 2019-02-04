## Project 2: Continuous Control

This is the second project as part of Deep Reinforcement Learning course in [Udacity](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).
The objective of the project is to keep a double-jointed to arm to in the goal position as long as possible.

---

### Problem Description

For this project we worked with the second version of [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environmnt provided by [Unity](https://github.com/Unity-Technologies)
which contains 20 identical agents, each with their own copy of the environment. In this setting, all the agents must obtain an average score of +30 (over 100 consecutive episodes and over all agents).

In other words, the environment is considered sovled,  when the average (over 100 episodes) of those average scores is at least +30.

---

### Implementation Details
At the heart of this approach lies an actor-critic method. Policy-gradient methods like [REINFORCE](http://www-anw.cs.umass.edu/~barto/courses/cs687/williams92simple.pdf) use Monte-Carlo esitmate.
As a result they exhibit high variance. Value-based approaches using Temporal Difference estimates display low variance. Actor-Critic methods combine these two
approaches and extract the best out of both worlds. They are more stable than TD estimates and at the same time need fewer samples than policy-gradient methods.

An Actor-Critic method contains two neural network one for the actor and one for the critic. The actor's role is to update the policy which is then 
evaluted by the critc, in turn training the actor to acheive a good policy. 


### Results

#### Hyper Parameters

#### Observations

### Further Improvements

- Using Prioritized Replay ([paper](https://arxiv.org/abs/1511.05952)) has generally shown to have been quite useful. It is expected that it'll lead to an improved performance here too.

- Other algorithms like TRPO, PPO, A3C, A2C that have been discussed in the course could potentially lead to better results as well.

- The Q-prop algorithm, which combines both off-policy  and on-policy learning, could be good one to try.

- General optimization techniques like cyclical learning rates and warm restarts could be useful as well.
