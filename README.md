# Reinforcement Learning: Optimizing Warehouse Flows

![image](https://user-images.githubusercontent.com/59663734/140646605-98841672-0769-44f4-924b-b76e5e309307.png)


https://user-images.githubusercontent.com/59663734/140646492-49b8debe-ba8c-4a06-b44f-0401875b081c.mp4



## Abstract

## Case Study

![image](https://user-images.githubusercontent.com/59663734/140644626-98354f2a-3b42-4de0-808a-c2e182e8092a.png)

![actu-rt-knits-fl_opt_20191206113258-scaled](https://user-images.githubusercontent.com/59663734/140644631-b4fa3d0d-f389-451b-aa96-fd2239e90e11.jpg)

![image](https://user-images.githubusercontent.com/59663734/140645995-667ae107-702b-483f-b95f-01e60aa331ec.png)


![Untitled_Artwork](https://user-images.githubusercontent.com/59663734/140641704-6f8bf1d7-a9ec-4460-bd9f-1c9464ac2537.gif)

## Plan of Attack

1. Define the Environment
- Define the States
- Define the Actions
- Define the Rewards


2. The AI Solution
- What is Reinforcement Learning?
- Markov Decision Process(MDP)
- Bellman Equation
- Policy vs Plan
- Living Penalty
- Q-Learning
- Temporal Difference



3. Implementation
- Building the AI solution
- Coding
- Improvement

## 2. The AI Solution

### 2.1 Reinforcement Learning Overview
If we want to train a helicopter to fly and we are given the position, which is the **state**, of the helicopter at a given point in time and we need to take actions to make it fly in a certain trajectory then there is no direct mapping of x to y to how to fly the helicopter. Therefore, it is going to be hard to use supervised learning for this problem. However, with reinforcement learning we don't need to specify the correct answer at every step but only a **reward function** to specify the helicopter when it is flying well and when it is doing poorly. A high reward would signify the helicopter is flying in the correct trajectory and a negative reward when it crashes. 

We can observe this process similar to training a dog whereby the latter is given a treat whenever it does something that is being asked. In our case, our rewards which can be value of ```+1, -1 or 0``` will do the exact same job as the treat. One of the challenges of RL is the **Credit Assignment Problem**. For example in a game of chess, we cannot say it is the last move that made us lose. It could have been the 15th one or the 10th or even the first one. This happens because our rewards are **sparse and infrequent**. In **sparse rewards**, we get the rewards only in the end whereas in dense **rewards** we know what we are doing right or wrong while doing it. Therefore, we need to solve this problem indirectly by proposing small rewards along the way and a bigger reward in the end. 

Early on, reinforcement learning has been used to play games like Atari Breakout. Most recently using OpenAI Gym, we can make a humanoid learn how to walk and do a parkour course. Now we are trying to teach self-dricing cars to drive using RL. Instead of going physically on the road where there are risks on collision and damage, we train the car in a simulator and after a lot of trials, we can then let it drive on real physical roads. 

![image](https://user-images.githubusercontent.com/59663734/141984612-500278fb-287a-43fc-9851-fb880639e3a7.png)


### 2.1 Markov Decision Process(MDP)
Reinforcement Learning problems are modelled by Markov Decision Process(MDP). MDP is a formalism to represent the world where our agent will interact with. It is a tuple of five elements: ![image](https://user-images.githubusercontent.com/59663734/142256520-82a1fbd8-fed2-405e-9567-08c7028cad3c.png)

 - S: Set of States (In chess this equals all possible chess positions and in our warehouse problem this will equal all posible positions our robot can navigate)
 - A: Set of Actions (In the helicopter example this could be all the positions we can move our control sticks and in our case it will be all the possible moves our robot can make)

 - <img src="https://latex.codecogs.com/svg.image?P{sa}" title="P{sa}" />: State Transisiton Probabilities ![image](https://user-images.githubusercontent.com/59663734/142258379-d6ebb940-c611-437d-acf3-180f9b0c88e0.png) (If we take a certain action a in state s then what is the probability of reaching state s')
 - <img src="https://latex.codecogs.com/svg.image?\gamma&space;" title="\gamma " />: Discount Factor <img src="https://latex.codecogs.com/svg.image?\gamma&space;&space;\epsilon&space;&space;[0,1]" title="\gamma \epsilon [0,1]" />
 - R: Reward Function

For simplicity, we wil reduce our warehouse to a simple ```4 x 3``` grid world with one obstacle at coordinates (2,2) as shown below:

![image](https://user-images.githubusercontent.com/59663734/142264675-d6b388cb-5c04-4f47-9344-f64b8558afdb.png)

### Markov Process
In order to understand MDP, it is important to understand what is a Markov Process. By definition a Makrov process is: 

_"A Markov chain or Markov process is a stochastic model describing a sequence of possible events in which the probability of each event depends only on the state attained in the previous event. A countably infinite sequence, in which the chain moves state at discrete time steps, gives a discrete-time Markov chain."_

In simpler terms, it means that it does not matter where our agent has been before in our gridworld. It is a random process in which the future is independent of the past, given the present. What will happen in the future is only determined by the state our agent is in now plus the actions it will take with the overlay of randomness.

For our simplified gridworld, it contains ```11``` states and four possible actions per state: ```Left, Right, Up, Down```. And when we want our robot to come Up for example, it does not always go Up all the time. Due to friction or dynamic noise of our robot, it can slightly veer left or right and we need to model this stochastic behavior which we will experience in the real-world to to our environment. 

![image](https://user-images.githubusercontent.com/59663734/142266339-4af7b212-2568-48d1-88ef-5aab206b470e.png)










## Conclusion

![Untitled_Artwork (1) (1)](https://user-images.githubusercontent.com/59663734/140646265-13d7af87-cba2-429d-902d-eda4efd71838.gif)





## References
