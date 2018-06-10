### DeepMind RL lecture 1, UCL - [Youtube](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PL7-jPKtc4r78-wCZcQn5IqyuWhBZ8fOxT&index=1)

#### Introduction

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
Like these definitions, we can think of the RL as mutual interaction between the Agent and the Environment.

#### information state

An information state(a.k.a Markov state) contains all useful information from the history
"The future is independent of the past given the present"
In other word, you only need to store state.

-   Once the state is known, the history may be thrown away
-   The state is a sufficient indicator of the future

#### Full observability: agent **directly** observes environment state, that is, Ot = St^a, St^e

#### Partial observability:

-   agent **indirectly** observes environment (e.g. robot with camera, and location)
-   A trading agent only observes current prices
-   A poker playing agent, only observes public card
-   Now agent state != environment state
-   Agent must construct its own state representation St^a, e.g.  
    Complete history: St^a = Ht  
    Belief of environment state St^a = (P[St^e = S^1], ..P[St^e = Sn])

### Inside of RL Agent

RL agent may include one or more of these components:

-   Policy: how agent picks actions.
-   Value function: how good is each state.
-   Model: agent's representation of the environment.

#### Policy

-   A **map** from state to action
-   Deterministic policy: a = pi(s)
-   Stochastic policy: pi(a|s) = P[A = a|S = s]

#### Value funciton

-   A **prediction of expected future reward**
-   used to evaluate the goodness/badness of states
-   And therefore to select between actions.

#### Model

A model predicts what the environment will do next

-   Transitions: P predicts the next state
-   Rewards: R predicts hte next (immediate) reward

### Categorizing RL agents

-   Value based

    -   No Policy(implicit)
    -   Value Function
    -   Follow expected value greedily

-   Policy based

    -   Act based on policy
    -   No value function

-   Actor Critic

    -   Policy
    -   Value function

-   Model Free
    -   Policy and/or Value Function
    -   No model
