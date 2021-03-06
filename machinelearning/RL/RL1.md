### DeepMind RL lecture 1, UCL - [Youtube](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PL7-jPKtc4r78-wCZcQn5IqyuWhBZ8fOxT&index=1)

#### Introduction

Same problem -> decision making. across many field. optimal way to make decision.  
There are **many different similar fields.**

What makes RL different from other ML paradigms?

-   there is no supervisor, only a reward signal
-   Feedback is delayed, not instantaneous  
    maybe many steps later, you'll actually see that decision was bad or good.
-   Time really matters (sequential, non.i.i.d data)
    Specifically, RL is different from the fact that it changes Environment.

Optimize sequence of decisions!

RL is based on **Reward Hypothesys**. which is a scalar feedback signal.  
Example of rewards:

-   Fly stunt manoeuvres in a helicopter
    -   +reward for following desired trajectory
    -   -reward for crashing

At each step t, the agent:

-   Executes action At
-   Receives observation Ot
-   Receives scalar reward Rt

The environment:

-   Receives action At
-   Emits observation Ot
-   Emits scalar reward Rt

![image](images/brain_and_earth.png 'title')  
**But exactly what moment is t changes?** which one goes first?

#### History and State

The **History** is the sequence of observations, actions, rewards
Ht = A1, O1, R1, A2, O2, R2 ... At, Ot, Rt
What happens next is depends on the history:

-   The agent selects actions
-   The environment selects observations/rewards

Instead of looking back all the history about what was happend every time,  
we see the 'state' of agent.  
State is the information used to determine what happens next

Formally, state is a function of the history:
**St = f(Ht)**

The environment state St^e is the environment's private representation.
The agent state St^a is the agent's internal representation.
Like these definitions, we can think of the RL as mutual interaction between the Agent and the Environment.

#### Information state

An information state(a.k.a Markov state) contains all useful information from the history
"The future is independent of the past given the present"
In other word, you only need to store state.

-   Once the current state is known, the history may be thrown away
-   Current state is a sufficient indicator of the future

#### Rat Example

So we got the concept that current state is enough to represent what happened before.  
However, current state does not necessarily mean it should be static. In other words, we can
define the state as last 3 items in sequence, or complete sequence. If we decided to define
the state to complete sequence, then the state can contain 'past' what we call history.
It is our job to define state that is useful for inteligent agent system.

#### Full observability: agent **directly** observes environment state, that is, Ot = St^a = St^e

#### Partial observability:

-   agent **indirectly** observes environment (e.g. robot with camera, and location)
-   A trading agent only observes current prices
-   A poker playing agent, only observes public card
-   Now agent state != environment state
-   Agent must construct its own state representation St^a, e.g.  
    Complete history: St^a = Ht  
    **Belief**(probability) of environment state St^a = (P[St^e = S^1], ..P[St^e = Sn])

### Inside of RL Agent

RL agent may include one or more of these components:

-   Policy: how agent picks actions from its state.
-   Value function: measures how good is each state or/and how good is each action.
-   Model: agent's representation of the environment.

#### Policy

This is what we really care about. We want to learn this thing from experience.

-   A **map** from state to action
-   Deterministic policy: a = pi(s)
-   Stochastic policy: pi(a|s) = P[A = a|S = s]

#### Value funciton

-   A **prediction of expected future reward**
-   used to evaluate the goodness/badness of states
-   And therefore to select between actions.
-   Important: If you take a look at the fomula, you can notice **pi** is indexed  
    Because policy decides action among various options. so it goes like,
    How much total award is **Expected** to get in the future.

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
