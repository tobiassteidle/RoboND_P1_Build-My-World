[![Udacity - Robotics NanoDegree Program](https://s3-us-west-1.amazonaws.com/udacity-robotics/Extra+Images/RoboND_flag.png)](https://www.udacity.com/robotics)

# RoboND_P1_Build-My-World
The **RoboND_P1_Build-My-World** lab part of RoboND Gazebo Basics lesson. The purpose of this lab is to learn how to build a robot model with the Model Editor tool in Gazebo. Include this model in an empty Gazebo World. And, finally write a plugin to interact with this world.  

### Directory Structure
```
    .RoboND_P1_Build-My-World.git      # repository main folder 
    ├── images                         # Code output image                   
    │   ├── output.png
    ├── model                          # Model files of the two-wheeled robot
    │   ├── robot
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script      
    │   ├── hello.cpp
    ├── world                          # Gazebo main World empty scene
    │   ├── Flat
    ├── CMakeLists.txt                 # Link libraries 
    └──                              
```

### Steps to launch the simulation

#### Step 1 Update and upgrade the Workspace image
```sh
$ sudo apt-get update
$ sudo apt-get upgrade -y
```

#### Step 2 Clone the lab folder in /home/workspace/
```sh
$ cd /home/workspace/
$ git clone https://github.com/tobiassteidle/RoboND_P1_Build-My-World.git
```

#### Step 3 Compile the code
```sh
$ cd /home/workspace/RoboND_P1_Build-My-World/
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

#### Step 4 Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/RoboND_P1_Build-My-World/build
```

#### Step 5 Run the Gazebo World file  
```sh
$ cd /home/workspace/RoboND_P1_Build-My-World/world/
$ gazebo Flat
```

### Output
The hello world message and two of my four-wheeled robots inside a Gazebo World should both launch as follow: 
![alt text](images/output.png)


    
 
