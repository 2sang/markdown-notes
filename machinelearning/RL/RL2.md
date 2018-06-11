### Markov Reward Process

A Markov reward process is a Markov chain with values.

-   Markov Reward Process is a tuple \<S, P, R, gamma\>
-   S is a finite set of states
-   P is a state transition probability matrix,  
    Pss' = P[St+1 = s' | St = s]
-   R is a reward function, Rs = E[Rt+1 | St = s]  
    How much reward I get from that moment, from that state.
    This is what we care about, maximizing reward function.
-   gamma is a discount factor

Bellman Equation:

-   Consists of expected return(Gt), conditioned on state s
-   Return is, sum of reward we get in the future.
-   Basically, it decomposes the value function into **immediate reward Rt+1** and **value of next state**
