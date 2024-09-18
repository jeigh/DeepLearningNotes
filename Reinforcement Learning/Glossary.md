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
The percentage that future rewards will be discounted by when calculating DFR. (eg... .8 woould suggest that the action should be valued at only 80% of its actual DFR)

See graphic for a better description of the three above concepts.