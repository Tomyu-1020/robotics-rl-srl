# Gym wrappers for state representation learning with robotic arms (Baxter + Kuka)

**Requirement: Python 3 (python 2 not supported because of OpenAI baselines)**

[PyBullet Documentation](https://docs.google.com/document/d/10sXEhzFRSnvFcl3XxNGhnD4N2SedqwdAvK3dsihxVUA)

```
git clone git@github.com:araffin/gym-baxter-rl.git --recursive
```

or
```
git submodule update --init
```

## Kuka Arm \w PyBullet

```
python main.py --num-processes 4 --num-stack 1 --env-name KukaButtonGymEnv-v0 --algo a2c
```


## Baxter Robot \w Gazebo and ROS
Gym Wrapper for baxter environment + RL algorithms

```
roslaunch arm_scenario_simulator baxter_world.launch
roslaunch arm_scenario_simulator spawn_objects_example

python -m gazebo.gazebo_server
python -m gazebo.teleop_client
```

```
sudo netstat -lpn | grep :7777
```
