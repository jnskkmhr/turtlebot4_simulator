# Turtlebot4 Simulator

Turtlebot4 Simulation using Ignition Gazebo.

Visit the [TurtleBot 4 User Manual](https://turtlebot.github.io/turtlebot4-user-manual/software/turtlebot4_simulator.html) for details.

## Installation

### dependencies
```bash
sudo apt-get update && sudo apt-get install wget
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
sudo apt-get update
sudo apt-get install ignition-fortress
```

### build
```bash
cd {/simulator_ws}
rosdep install --from-paths src -yi
colcon build --symlink-install
```

### Run simulation in the office
```bash
ros2 launch turtlebot4_ignition_bringup turtlebot4_ignition.launch.py world:=office model:=lite x:=0.5 y:=0.5
```

Here is how the environment (7.7m x 10.0m) looks like. 
<img src="media/gazebo_office.png">