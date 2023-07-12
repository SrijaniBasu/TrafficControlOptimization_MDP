
# Optimal Policy for Traffic Signal Control using MDP

This code implements a simple traffic signal control problem and calculates the optimal policy using the value iteration algorithm. The goal is to determine the best action (green light direction) for each state (traffic conditions) to maximize the cumulative rewards.

## Code Overview

1. The code begins by importing the necessary libraries, including random, pandas, matplotlib, and seaborn.

2. A list named data is created to store the randomly generated traffic data. Each entry in data represents a state and consists of volume, speed, and status (0 for NS direction, 1 for EW direction).

3. The set of unique states is obtained by converting data into a set named states.
The set of possible actions is defined as {'green for NS direction', 'green for EW direction'} and stored in the actions variable.

4. The transition probabilities are calculated and stored in the transitions dictionary. The probabilities represent the likelihood of transitioning from a current state-action pair to a next state.

5. The rewards for each state-action-next_state combination are calculated and stored in the rewards dictionary. The rewards represent the immediate benefits of choosing a particular action in a given state.

6. The discount factor (gamma) and convergence threshold (convergence_threshold) are defined.

7. The value iteration algorithm is implemented to compute the optimal state values (V). The algorithm iterates until the change in values between iterations falls below the convergence threshold.

8. The optimal policy is extracted by selecting the action with the highest expected value for each state.
The optimal policy is displayed as a dictionary mapping each state to its corresponding optimal action.
The optimal policy is visualized using various methods:

    A pandas DataFrame is created to represent the optimal policy.
    A 3D scatter plot is generated using matplotlib to visualize the relationship between volume, speed, and direction, with colors representing the optimal actions.
    A heatmap is created using seaborn and matplotlib to visualize the optimal policy based on volume and speed. The heatmap displays the actions as color-coded cells.

## Usage
To run the code, ensure that the required libraries (random, pandas, matplotlib, and seaborn) are installed in your Python environment. Then, execute the code in a Python environment that supports the required libraries.

The code generates a pandas DataFrame (df) that represents the optimal policy. It also creates visualizations of the optimal policy, including a 3D scatter plot and a heatmap.

Please note that this code assumes a simple traffic signal control problem with randomly generated data. You can modify the code to suit your specific requirements or extend it for more complex scenarios.

## Requirements

    Python 3.x
    Required Libraries: random, pandas, matplotlib, seaborn


