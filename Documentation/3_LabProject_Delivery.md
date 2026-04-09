# Seminar: Project Tools
### Aitana Mata Flor, Elena Prat Ferrer

#### Introduction
This seminar consisted on understanding and applying the GitHub app in our projects. The main goal was to prepare the development environment in VS Code, program the ESP32 using PlatformIO, and synchronize physical movements with a 3D virtual model.

#### What have we done?
In this project, we connected an ESP32 Endo-module to a local network and used PlatformIO to upload the code that reads 3D orientation from an IMU sensor. By using RoboDK and a code in Python, we were able to make a virtual plane move at the same time that the physical sensor. We verified the accuracy by testing each axis of rotation and even learned how to emulate the hardware using a slider-based script. 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/4ee034f0-f77d-4f07-b3a3-62a88fab3ab7" />

Once the communication was established, we moved on to a medical robotics application. We modified the Python code to change the target object, allowing us to control the orientation of a surgical needle instead of the plane. This step was crucial to show how the system can be adapted for surgical simulations.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/82d57c00-a90a-452b-958a-442a6411902c" />

At the end of the project, we focused on the precise verification of the rotation. By monitoring the RPY (Roll, Pitch, and Yaw) data in the Python terminal and checking the object details in RoboDK, we confirmed that the axes rotated correctly. This final verification ensured that the virtual movement matched the real-world angles exactly.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/2661066e-21c8-49f1-81a8-822b32675311" />

This workflow successfully demonstrated how to bridge hardware sensors with digital twins, providing a solid foundation for future engineering and surgical robotics projects.

#### Laboratory Questions
- Is the plane 3D object in RoboDK moving properly?

Yes, the plane follows the sensor's orientation in real-time. Once the IP addresses were correctly configured, the virtual movement matched the physical movement of the board.

- What have you done to properly verify the orientation angles (Roll, Pitch, and Yaw)?

We tested each axis individually. We tilted the board forward/backward for Pitch, side-to-side for Roll, and rotated it horizontally for Yaw. We verified that the visual response in RoboDK matched these specific physical movements.

- Change the 3D object orientation to "surgical_needle". What do you have to change in the python code?

In the Receive_data_RPY_IMU_world.py script, we have to find the line where the object is defined (usually RDK.Item('plane')) and change the string to RDK.Item('surgical_needle').

#### Conclusion
This laboratory session helped us understand how to connect different tools to complete an engineering task, combining version control, embedded systems programming, and 3D simulation. Using GitHub was essential to organize the project, manage code safely, and work efficiently as a team.

For future projects like the TFG or avant-projecte, these tools will be especially useful. RoboDK and Python allow us to visualize and test robotic movements and tool orientations in a simulated environment, ensuring the Roll, Pitch, and Yaw are correct before building physical prototypes. The ESP32 with PlatformIO is ideal for programming microcontrollers and reading sensors, while sending data via WiFi demonstrates a key hardware–software integration skill. Overall, using these tools provides a structured and reliable workflow for managing complex engineering projects.

