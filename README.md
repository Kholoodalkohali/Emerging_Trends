# Treasure Hunt Game Deep Q-Learning
## Overview
This project implements a reinforcement learning agent (pirate) that navigates a maze to find the treasure using Deep Q-Learning (DQN). The goal is to design an intelligent agent that maximizes its reward by finding the optimal path through the maze, using exploration and exploitation strategies.

## Project Files
- TreasureHuntGame.ipynb: Jupyter notebook with the implementation of the treasure hunt game and deep Q-learning training loop.
- TreasureMaze.py: Python class that defines the maze environment, including the grid, valid actions, and the game state.
- GameExperience.py: Python class for experience replay, which stores past game experiences for training the Q-learning agent.
- Maze Environment: The game environment is represented as an 8x8 grid maze where the pirate has to navigate through valid cells to reach the treasure.
## Dependencies
- TensorFlow: For implementing the neural network model and training the agent using deep Q-learning.
- NumPy: For handling array operations and matrix manipulations.
- Matplotlib: For visualizing the maze and the agent’s progress.
- Keras: For building and training the neural network model.
### You can install the dependencies via:
pip install tensorflow numpy matplotlib keras

## Project Structure
### Initialization and Setup:

The maze is defined as an 8x8 grid, where 1 represents a valid path and 0 represents a wall.
The agent (pirate) starts from a defined initial position in the maze.
## Deep Q-Learning Model:

The neural network model is designed to take the current state of the environment (maze) as input and output Q-values for each possible action.
The model consists of three fully connected layers: one input layer, two hidden layers with ReLU activations, and an output layer representing possible actions.
## Experience Replay:

The agent learns by exploring the environment and storing its experiences in memory. This memory is used to train the neural network using past experiences.
## Exploration vs. Exploitation:

The agent uses the epsilon-greedy strategy where it explores the maze randomly with probability epsilon (exploration) or chooses the action with the highest Q-value (exploitation).
## Training Loop:

The agent plays multiple episodes, each consisting of selecting actions, observing rewards, and updating its Q-values based on the experience.
## Performance Evaluation:

After training for a number of epochs, the agent is evaluated on its performance, and a win rate is calculated. The training stops when the agent achieves a win rate above a specified threshold (e.g., 90%).
## How to Run
- Clone the repository or download the project files.
- Open the TreasureHuntGame.ipynb notebook in Jupyter Notebook.
- Run the cells in order to initialize the maze, train the agent, and visualize the agent’s performance.
- The agent will attempt to find the optimal path to the treasure by exploring and exploiting the environment, improving its strategy over time.
## Results
The training loop will print the loss, win count, and win rate for each epoch.
The agent's progress can be visualized at each step in the maze using Matplotlib.

## Example Output
Epoch 001/1000 - Loss: 0.4532
Epoch 002/1000 - Loss: 0.3456
...
Epoch 1000/1000 - Loss: 0.0123
Training complete.

## Conclusion
This project demonstrates the power of deep reinforcement learning using Q-learning to solve a maze navigation problem. The trained agent learns an optimal strategy to find the treasure while avoiding obstacles by adjusting its policy over multiple training episodes.

## Connecting to the Larger Field of Computer Science
### What Do Computer Scientists Do and Why Does It Matter?
Computer scientists develop algorithms and computational models to solve problems across various domains. In this project, I used machine learning algorithms to design an intelligent agent that can learn optimal strategies through experience. By creating systems that can "learn" from their environment, computer scientists contribute to innovations in fields such as healthcare, finance, and autonomous systems, making our world more efficient and interconnected.

### How Do I Approach a Problem as a Computer Scientist?
As a computer scientist, I break down problems into manageable components, design algorithms, and create models to test and solve them. In this project, I started by defining the environment and the agent’s objectives, then selected an appropriate reinforcement learning technique—Deep Q-Learning—to guide the agent’s learning process. I iterated on this process to optimize the agent’s performance, testing and adjusting the model to improve results.

### What Are My Ethical Responsibilities to the End User and the Organization?
When developing systems like the one in this project, my ethical responsibilities include ensuring fairness, privacy, and transparency. For the end user, it’s essential that the agent’s decisions are explainable and that the system is transparent about its learning process. Additionally, any data collected from users or environments must be handled responsibly, with user consent and data security measures in place. In an organizational context, I must ensure that the system aligns with company goals while maintaining a focus on user welfare and societal impact.
