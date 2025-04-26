# Autonomous Maze Solving Turtlebot3 Simulation

This repository contains the code to produce a **Gazebo Classic Simulation** of a **Turtlebot3** (***waffle***) robot (designed by *Robotis*) that navigates its way through a simple maze **autonomously**.


The software tools mainly used in building this project are :

- Python3 Interpreter
- Basic ROS2 Framework
- Gazebo Classic Simulator
- *turtlebot3_gazebo* ROS2 package
- *slam_toolbox* ROS2 package
- Navigation2 Stack

Operating System :
- Ubuntu  

In order to deploy this project successfully, all the above listed softwares must be installed in Ubuntu OS.


## Deployment

To deploy this project, below mentioned steps to be follow.

- **Create a new folder** at a suitable space in Ubuntu OS. 

- Open a **new terminal** inside the folder.

- **Clone this repository** inside the folder by running the following terminal command.

    
bash
    


- This will create a new folder named **Autonomous-Maze-Solving-Turtlebot3-Simulation** inside the **Cloned Repo** directory.

- Go inside the **Autonomous-Maze-Solving-Turtlebot3-Simulation** folder through the previously opened terminal.

    
cd Autonomous-Maze-Solving-Turtlebot3-Simulation/


- Next, we need to build this project. So run the following command from the same terminal.

    
bash
    colcon build

    
    This will generate 3 (three) new folders inside the **Autonomous Maze Solving Turtlebot3 Simulation** folder namely - **build**, **install** and **log**.

- Close the previous terminal.

- Next, finally we can deploy the project.
    
    - Open a new terminal inside the **Autonomous Maze Solving Turtlebot3 Simulation** directory and run the following commands:
        
bash
        source install/setup.bash
        ros2 launch autonomous_tb3 tb3_maze_navigation.launch.py


        This will open a **Gazebo Classic Simulator Window** (with the simulated ***maze world*** and a ***Turtlebot3*** robot - inside of it) AND a **RViz2 Window** (where we can see a 2D map of the maze world). 
        
        Use ***Mouse Scroll Wheel*** to ***Zoom IN/Zoom OUT*** in both the **Gazebo** and **RViz2** enviroments.

        Use **left mouse button** (to PAN) and ***Mouse Scroll Button*** (to ROTATE) -- for adjusting the position and view of the **maze world** in the **Gazebo** environment 

        Use **left mouse button** (to ROTATE) and ***Mouse Scroll Button*** (to PAN) -- for adjusting the position and view of the **2D maze map** in the **RViz2** environment 

        Also, before proceeding to the next step, it is recomended to keep both the **Gazebo** and **Rviz2** windows opened side by side, so that you that we can see see what's happening in both the windows at the same time.

    - Open a second parallel terminal inside the **Autonomous Maze Solving Turtlebot3 Simulation** directory (while keeping the previous terminal alive) and run the following command from it :
        
bash
        source install/setup.bash
        ros2 run autonomous_tb3 maze_solver.py
        
**output**

**Deployment** section, the following **simulation output** can be seen in the **Gazebo Classic Simulator** window.

<figure class="video_container">
  <video controls="true" allowfullscreen="true" poster="Thumbnail.png">
    <source src="Gazebo_Sim_Recording.mp4" type="video/mp4">
  </video>
</figure>

