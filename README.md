# ROS-Sharp-Movement
Movement example Unity repo for ROS Sharp. When running properly, the movement of the cube should be published to the topic `\cube_pos` when the Unity project is running

## To run
- Clone this git repo to any location on your machine
- Open the Unity Project in the folder `ROSSharp` (the editor used was 6000.0.038f1, but this should be transferrable to any version)
- Before running: 
    - Make sure to configure the proper IP details in the `ROS Connector` object
    - Run `ros2 run rosbridge_server rosbridge_websocket.py` in your terminal window to start the connection between Unity and ROS2
- Run the Unity project and test the output using `ros2 topic echo \cube_pos` in another terminal window
    - **NOTE**: It sometimes takes move from *Game Mode* to *Scene Mode* in Unity for the messages to start sending, or it may be that Unity just needs to be in focus, but it can sometimes be a bit funky. If the topic shows up in `ros2 topic list`, then the connection is likely working