# Homework1
 
## Istruzioni 
1. Clona il repository in una cartella:
```bash 
git clone https://github.com/Emacif/RL24_HW1.git

2. Avvia il container con immagine da ros2_docker_scripts, con lo scopo di configurare e costruire tutti i pacchetti presenti nel workspace:
```bash 
colcon build 
source install/setup.bash

## Lancio dei pacchetti: 
1. Per lanciare arm_description:

```bash 
ros2 launch arm_description display.launch.py 

2. Per lanciare arm_gazebo senza controlli: 

```bash 
ros2 launch arm_gazebo arm_world.launch.py 

3. Per lanciare arm_gazebo con i controlli: 

```bash 
ros2 launch arm_gazebo arm_gazebo.launch.py 

4. Per lanciare arm_control: 

```bash 
ros2 launch arm_control control.launch.py 

5. Avviare il nodo ros_publisher: 

```bash 
ros2 topic pub /position_controller/command std_msgs/msg/Float64MultiArray "{data: [0.0, 0.0, 0.0, 0.0]}"