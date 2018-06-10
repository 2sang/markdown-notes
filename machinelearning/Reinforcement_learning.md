#### DeepMind RL lecture 1, UCL - [Youtube](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PL7-jPKtc4r78-wCZcQn5IqyuWhBZ8fOxT&index=1)

RL is based on **reward hypothesys**
Reward: is a scalar feedback signal.
At each step t, the agent:

-   Executes action At
-   Receives observation Ot
-   Receives scalar reward Rt

The environment:

-   Receives action At
-   Emits observation Ot
-   Emits scalar reward Rt

Ht = A1, O1, R1, A2, O2, R2 ... At, Ot, Rt
What happens next is depends on the history:

-   The agent selects actions
-   The environment selects observations/rewards

State is the information used to determine what happens next

Formally, state is a function of the history:
**St = f(Ht)**

The environment state St^e is the environment's private representation.
The agent state St^a is the agent's internal representation.
