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
Reinforcement Learning problems are modelled by Markov Decision Process(MDP). MDP is a formalism to represent the world where our agent will interact with. It is a tuple of five elements: 















## Conclusion

![Untitled_Artwork (1) (1)](https://user-images.githubusercontent.com/59663734/140646265-13d7af87-cba2-429d-902d-eda4efd71838.gif)





## References
