# README #

Launch and configuration files for demonstrating nonholonomic navigation using the [lattice_planner package](https://github.com/larics/lattice_planner.git).

Currently, the package allows you to spawn a Pioneer P3-DX robot in an empty Gazebo world and control it by providing navigation goals.

## Installation ##

The package has been tested with ROS Kinetic on Ubuntu 16.04.

In addition to `ros-kinetic-desktop-full`, the following packages must be available in your workspace:

* [p2os](https://github.com/allenh1/p2os) - URDF model of the P3-DX
* [lattice_planner](https://github.com/larics/agv_control_msgs) - the lattice path planner
* [agv_control_msgs](https://github.com/larics/agv_control_msgs) - path planner dependency
* [pure_pursuit](https://github.com/larics/pure_pursuit) - path following algorithm

Make sure to `catkin_make` or `catkin build` the package and sourcing `setup.bash` for your workspace before running the demo.

## Running the demo ##

```
roslaunch lattice_navigation_demos p3dx-gazebo-empty-lattice-ppursuit
```

You can set navigation goals through `rviz`.

## Citing ##

These packages have been developed within our research on AGV coordination in warehouses. The path planner implementation is described in the following paper:
```
@ARTICLE{7571170,
author={I. Draganjac and D. Miklić and Z. Kovačić and G. Vasiljević and S. Bogdan},
journal={IEEE Transactions on Automation Science and Engineering},
title={Decentralized Control of Multi-AGV Systems in Autonomous Warehousing Applications},
year={2016},
volume={13},
number={4},
pages={1433-1447},
keywords={},
doi={10.1109/TASE.2016.2603781},
ISSN={1545-5955},
month={Oct},}
```

