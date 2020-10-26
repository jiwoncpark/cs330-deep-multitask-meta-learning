# HW3

## Concepts
* Adapt an existing model (a Deep Q-Network) to be goal-conditioned.
* Run goal-conditioned DQN on two environments
* Implement Hindsight Experience Replay (HER) [1] on top of a goal-conditioned DQN for each environment
* Compare the performance with and without HER

## Main takeaways:
* Implementing goal-conditioning for DQN was just a matter of concatenating the state (observation) with goal before forwarding the model.
* "With HER, the model is trained on the actual (state, goal, reward) tuples along with (state,goal, reward) tuples where the goal has been relabeled to be what state was actually reached and the rewards correspondingly relabeled. In other words, we pretend that the  state we reached was always our goal so that the agent has more examples of actions that have positive rewards. The reward function for relabeled goals is the same as the environment reward function; for the bit flipping environment, the reward is -1 if the state and goal vector do not match and 0 if they do match." from the assignment prompt

## Not checked in
* Image files (see HW3 submission PDF)
* MUJUCO key (so as not to violate the license agreement)

## References
[1] Andrychowicz, Marcin, et al. "Hindsight experience replay." Advances in neural information processing systems. 2017.
