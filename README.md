# DeepRacer Autonomous Racing Model README

## Overview

This repository contains the implementation, training, and deployment of an autonomous racing model using AWS DeepRacer. The model is built using reinforcement learning principles, where the agent learns to navigate a racing track through interactions with a simulation environment. The README provides an in-depth understanding of the key components, including the reward function, waypoints, hyperparameters, and the iterative refinement process.

## Contents

1. **Reward Function (reward_function.py):**
    - The reward function is a crucial element in shaping the model's behavior. It considers parameters such as distance from the center, track width, and waypoints for different lanes and speeds. The goal is to reward staying on the track, following the racing line, and maintaining appropriate speeds based on waypoints.

2. **Waypoints:**
    - Waypoints are defined for the left, center, and right lanes, as well as for fast and slow speeds. These waypoints play a significant role in guiding the model's behavior during training.

![Screenshot 2024-01-08 001551](https://github.com/vishalkodam/awsdeepracer_reward/assets/57845753/f8ca02c2-888f-423d-aa07-696456fda9d1)


3. **Action Space Type :**
    - The model uses a continuous action space where speed and steering angle are set to specific values. This choice influences the model's actions during training and racing.

![Screenshot 2024-01-08 001434](https://github.com/vishalkodam/awsdeepracer_reward/assets/57845753/c5d8be17-3c70-4935-b6eb-b348582af533)


4. **Hyperparameter Tuning :**
    - Hyperparameters play a crucial role in the training process. The chosen hyperparameters include Gradient Descent Batch Size, Entropy, Discount Factor, Loss Type, Learning Rate, Number of Experience Episodes Between Each Policy-Updating Iteration, and Number of Epochs.

![Screenshot 2024-01-08 001356](https://github.com/vishalkodam/awsdeepracer_reward/assets/57845753/06f1b2a6-f536-48ee-9256-532bd15fb618)



5. **Building the Model:**
    a. **Define Reward Function:** Implement the provided reward function and adjust waypoints based on the oval track's characteristics.
    b. **Set Up Waypoints:** Clearly define waypoints for each lane and speed category.
    c. **Configure Hyperparameters:** Use the provided hyperparameter values to configure the model.
    d. **Training and Evaluation:** Launch training simulations using the defined components and parameters. Monitor training progress and evaluate the model's performance.
    e. **Iterative Refinement:** Fine-tune the reward function, adjust waypoints, or experiment with hyperparameters based on observed model behavior.

## Deployment

1. **Simulation Deployment:**
    - After successful training, deploy the model in simulation environments (AWS DEEPRACER) to assess its performance in diverse scenarios.

2. **Physical Deployment (Optional):**
    - Transfer the knowledge gained in the simulation environment to a physical DeepRacer car for real-world autonomous racing. Ensure a seamless transition from virtual training to practical application.
