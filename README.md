# Reinforcement-Learning-CartPole
Cart-Pole Balance Using Deep Q-Networks
# Reinforcement Learning Project: Cart-Pole Balance

### Project Overview
This project was part of my coursework in reinforcement learning, where I developed a **Deep Q-Network (DQN)** agent to solve the classic cart-pole balancing problem. The objective was to train an agent capable of maintaining balance by taking optimal actions in response to the environment, emphasizing real-time decision-making and stability through strategic hyperparameter tuning and policy adjustments.

### Objectives
- Build and train a DQN agent to balance a pole on a moving cart in the **OpenAI Gym environment**.
- Optimize learning efficiency and stability by carefully tuning hyperparameters and implementing a **learning rate decay** strategy.
- Use performance metrics, such as mean return per episode, to assess and refine the agent’s balancing capability.

### Key Techniques and Methods
- **Deep Q-Network (DQN)**: A neural network model designed to approximate Q-values for state-action pairs, enabling the agent to select the best actions to balance the pole.
- **Learning Rate Decay**: Implemented a gradual reduction in learning rate with PyTorch’s **StepLR scheduler**, optimizing convergence by starting with a high learning rate for initial exploration, then decaying to promote stable learning as the agent improves.
- **Epsilon-Greedy Policy**: Applied a constant **epsilon of 0.2** to strike a balance between exploration and exploitation, enhancing the stability of the learning curve.
- **Hyperparameter Tuning**:
  - **Batch Size**: Set to 1000 to ensure efficient sampling and stable learning from the memory buffer.
  - **Buffer Capacity**: Optimized at 10,000 to store sufficient experiences for effective learning without excessive computational cost.
  - **Target Network Update Frequency**: Set to every 10 episodes to reduce instability in learning by periodically updating the target network.

### Results and Analysis
- The DQN agent successfully met the assignment’s success threshold, with the **learning curve stabilizing at a high return value**, indicating effective balancing of the cart-pole system.
- **Learning Curve Phases**:
  - *0–50 Episodes*: Initial exploration phase with low returns due to minimal prior experience.
  - *50–100 Episodes*: Steady improvement as the agent began leveraging stored experiences.
  - *100–150 Episodes*: Rapid increase in return values due to effective policy refinement and reduced overshooting from learning rate decay.
  - *150–300 Episodes*: Plateau in return values, demonstrating consistent balancing ability and indicating convergence.

### Key Takeaways
- **Learning Rate Decay** proved essential in stabilizing the agent’s learning, avoiding overshooting, and ensuring convergence to a robust policy.
- **Epsilon-Greedy Strategy**: Using a constant epsilon prevented oscillations in performance, helping the agent reliably exploit learned strategies.
- **Hyperparameter Tuning**: Fine-tuning memory buffer and batch size contributed to stable learning by balancing computational efficiency with memory recall, showing the impact of these factors on DQN training.

### Disclaimer
This project was completed as part of a coursework assignment. Code and data from the original environment are not included in this repository.
