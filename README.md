This project comprises two files: **Player.py and 3X3Puzzle.py**. 
The Player class in Player.py contains various methods, managing visited and revisited states, and variables such as cube and QV representing the cube's state (solved/unsolved) and the corresponding Q-values.

Initially, Q-values are unspecified, randomly set, and then assigned based on the states. The start state can be provided as either an array of arrays or a dictionary representing the cube's sides and their values.

Previous and second previous states are stored as the current state depends on them. Initial state patterns are registered in the database and assigned Q-values using a hash function.

The project employs Feature-based Q-learning, incorporating a pattern database to assess the cube's proximity to the solved state. This algorithm is particularly powerful for learning and optimizing strategies in complex environments.

The Qlearn method initializes parameters such as learning rate (alpha), discount factor, and epsilon, along with the number of episodes. It utilizes an epsilon-greedy policy, selecting actions based on the maximum reward while allowing for exploration of new actions.

The process continues for a set number of episodes until the player reaches the goal state, which signifies convergence. Throughout this iterative process, the algorithm learns from the rewards and refines its strategies to achieve better performance over time.

Supporting methods in 3X3Puzzle.py handle tasks such as shuffling the cube if the initial input is absent and checking if the cube has reached the goal state. These methods contribute to the robustness and functionality of the puzzle-solving system.

The variable n determines the number of rotations used to shuffle the cube initially, assuming it can rotate 180 degrees to manage the state space branching factor. This parameterization enhances the efficiency of the algorithm by controlling the complexity of the initial state.

Implemented by Jyothsna Priyanka Sakhamuri and Pranay Gudupally, this project represents a sophisticated approach to solving the 3x3 puzzle through machine learning and reinforcement learning techniques.
