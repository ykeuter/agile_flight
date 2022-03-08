## Installation Test

To test if the Flightmare simulator has been correctly installed as a python package, run vision demo script via the following command. 

```
cd agile_flight/envtest
python3 -m python.run_vision_demo --render 1
```

You should have TWO opencv windows open: one RGB image and one depth image. 

(Antonio) Why is this relevant?


Each [vision_env](/flightmare/flightlib/include/flightlib/envs/vision_env/vision_env.hpp) simulate one quadrotor, which has a monocular camera attached. We use vectorized environment [vision_vec_env](/flightmare/flightlib/include/flightlib/envs/vision_env/vision_env.hpp) for parallel simulation. As a result, you will have multiple simulated cameras. 

![vision_demo](/docs/imgs/vision_demo.png)

## Policy Training  

We provide a simple reinforcement learning code for you. Run the training via the following command. 

```
cd agile_flight/envtest
python3 -m python.run_vision_ppo --render 0 --train 1
```

### About the RL environment

### About the Python Binding 

### About the RL Algorithm 

## Policy Evaluation in ROS

Follow the steps on [this guide](https://github.com/uzh-rpg/agile_flight/blob/main/README.md#testing-todo) to evaluate your policies with our flight stack API.