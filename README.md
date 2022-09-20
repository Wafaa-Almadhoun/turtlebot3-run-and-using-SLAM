# turtlebot3-run-and-using-SLAM


## Table of contents
* [Introduction](#Introduction)
* [Algorithm](#Algorithm)

## Introduction

     TurtleBot is a ROS standard platform robot. Turtle is derived from the Turtle robot, 
     which was driven by the educational computer programming language Logo in 1967, There are
     3 versions of the TurtleBot model TurtleBot1,TurtleBot2 , and TurtleBot3

     TurtleBot3 is a small, affordable, programmable, ROS-based mobile robot for use in education, research,
     hobby, and product prototyping. The goal of TurtleBot3 is to dramatically reduce the size of the platform
     and lower the price without having to sacrifice its functionality and quality, while at the same time 
     offering expandability.
     
     The TurtleBot3’s core technology is SLAM, Navigation and Manipulation, making it suitable for home service
     robots. The TurtleBot can run SLAM(simultaneous localization and mapping) algorithms to build a map and 
     can drive around your room
  
   we will at first install turtlebot3 in ROS then SLAM mapping with TurtleBot3 by  testing and simulating it
   in Gazebo and Rviz


 ## Algorithm
 
 Step 1 : install ROS click [here](https://github.com/Wafaa-Almadhoun/Ros-install-in-Windows-10-with-64-bit-operating-system)
 
 step 2 :  install the TurtleBot3 , Open the terminal and install the dependents packages , copy and paste in terminal window
 
 
            cd ~/catkin_ws/src/
            
            git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
            
            git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
            
            cd ~/catkin_ws && catkin_make
            


 
 Step 3 : you have to choose which version you want to simulated before install
 
          export TURTLEBOT3_MODEL=burger

          export TURTLEBOT3_MODEL=waffle

          export TURTLEBOT3_MODEL=waffle_pi
 
 
 Step 4 : i will use burger version to do that use this command 
 
              gedit ~/.bashrc
            
         and copy " export TURTLEBOT3_MODEL=burger " and paste in the end of file then save and close it 
   
   
step 5 : Reload.bashrc

          source ~/.bashrc
          
          
 Step 6 : To download the TurtleBot3 simulation files, run these commands:
 
         cd ~/catkin_ws/src/
         
         git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
         
         cd ~/catkin_ws && catkin_make
 
 
 
 Step 7 : Now open TurtleBot3 in RViz simulator 
 
 
            roslaunch turtlebot3_fake turtlebot3_fake.launch
            
   ![burger Rivs](https://user-images.githubusercontent.com/64277741/191304511-cf512cdf-40c8-4d5b-a8e5-7727a4bb454c.png)

    Figure (1): TurtleBot3 in RViz simulator 
    

 Step 8 :  Now open TurtleBot3 in Gazebo simulator 
 
    
            roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
            
            
 ![burger gazebo ](https://user-images.githubusercontent.com/64277741/191305201-0126e135-94e7-4b05-b912-8123b4d9a869.png)
 

         Figure (2): TurtleBot3 in Gazebo simulator with empty world 
 
  
  Step 9 :  Now simulating TurtleBot3 by SLAM 
  
  
