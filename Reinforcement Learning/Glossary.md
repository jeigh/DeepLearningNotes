# Reinforcement Learning Glossary

## Agent
The actor that has the choice of action.  It's the actor that you're trying to train.

## Environment
Everything else in the scenario other than the agent. Eg.. the game board, the pieces on the board, the other players, etc...

## Feedback, Reward, Reward Signal
The item given to an agent after the agent has chosen an action.

## Ultimate Reward, Final Reward
The reward given to an agent if the chosen action is the reuslt of the end of the episode.

## Episode
(Colloquial definition) -> it's the game that the agent is being trained to win.

## Initial state
The state of the environment at the beginning of an episode.

## environmental state, state variables, state
The complete information (typically a set of numbers) given to the agent regarding the environment.

## Policy
the attribute of the agent that describes how it selects its move, (eg... could be always best (to maximize explore), could be always worst (to maximize exploit)), or some ratio of explore/exploit.

Examples include
* greedy - a policy that always selects the "best" action.
* epsilon-soft, epsilon-greedy - a policy that uses a random number to determine if the agent should explore or exploit.  a random number is generated, and if it's less than epsilon, the agent will explore.  If it's greater than epsilon, the agent will exploit.
* softmax policy - a policy that uses the softmax function to determine the probability of each action. (ie... there's a distribution of probabilities for each action)
* mellowmax

## Private Information
Information gleaned by the agent from previous actions and episodes.

## Full Observability
The agent can use all information about the environment to inform the decision regarding its actions.

## Limited Observability, Partial Observability
Some information about the environment cannot be used to inform the agent's actions (eg...  information that a human player might not have.)

## Credit Assignment Problem
Finding a way to share the ultimate reward between the last action and the steps leading up to the last action.

## Types of Rewards
* Immediate
* Long Terms

## Total Future Reward (TFR)
The reward attributed to an action + the reward for all the actions that followed it.

## Discounted Future Reward (DFR)
The reward attributed to an action + the DFR of each following action.

## Gamma (Γ or γ)
The percentage that future rewards will be discounted by when calculating DFR. (eg... 0.8 woould suggest that the action should be valued at only 80% of its actual DFR)

See graphic for a better description of the three above concepts.

## Learning Algorithm
The algorithm that the agent uses to learn from the feedback it receives.

* L-Learning
* Q-Learning
* SARSA

## L-Learning
Lousy Learning - basically, replaces the L-Value from the target cell in the L-Table with a new value.

## L-Table
A table that contains the L-Value for each possible action in each possible state.  The number of cells in the table is the number of states times the number of actions. (eg...  4608 rows = 512 * 9 in Flippers because there are 9 possible actions and 512 possible states of the game board)
Updates to the L table are made at the end of the episode, not after each action.

## Update Rule
The rule that determines how the L-Table is updated.   

* With L-Learning, the update rule is to replace the L-Value in the target cell with the new value.  
* Other rules may be a combination of use 80% of the previous value and 20% of the new value.

## Q-Learning
Quality Learning - A type of reinforcement learning that uses the Q-Table to determine the best action to take.  Uses Q-table and Q-values.
Updates to the Q-Table are made after each action.   To compute the new Q-Value, the immediate reward is added to the largest Q-Value of the next state after having mulitplied by a set Discount Factor.  The new Q-Value is then multiplied by the 

## Discount Factor
a value between 0 and 1 that represents how much of the future reward should be discounted.  (eg... 0.8 would suggest that the future reward should be discounted by 20%)

## Learning Rate
Often represented by the Greek letter Alpha (α), the learning rate is a value between 0 and 1 that represents how much of the new value should be used to update the old value.  (eg... 0.2 would suggest that 20% of the new value should be used to update the old value).   Used as part of the update rule mentioned above. 0.9 and 0.99 are commonly used values.

## SARSA
A type of reinforcement learning that uses the S-Table to determine the best action to take.

## S-Table
A table that contains the S-Value for each possible action in each possible state.... similar to the L-Table, but with the S-Value instead of the L-Value.

