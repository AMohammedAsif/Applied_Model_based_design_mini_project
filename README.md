# Applied_Model_based_design_mini_project

## SIMPLE AUTOPILOT DESIGN

The equations governing the motion of an aircraft are a very complicated set of six nonlinear coupled differential equations. However, under certain assumptions, they can be decoupled and linearized into longitudinal and lateral equations. Aircraft pitch is governed by the longitudinal dynamics. In this example we will design an autopilot that controls the pitch of an aircraft.

In this example we will simulate the linearized aircraft model with the state-feedback controller designed earlier in the example. We will specifically use the linearized state-space model obtained in Aircraft Pitch: System Modeling page.

![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Equation.png)

The above equations match the general, linear state-space form.
![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/difference.png)


This is a basic demo of simulation of an SIMPLE AUTOPILOT DESIGN
 using Matlab & Simulink. This file complements [this YouTube video](https://youtu.be/CJGlKCfGEA0)
 
 ## Building the state-space model
 
 We will now build a Simulink model of the above equations. One option is to build a model of the plant with state-feedback that emulates the figure shown below.
 ![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/statefeedback_pitch2.png)
 
 

## Screenshot of the model
![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Model.png)


## output of the model


![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Picture5.png)



![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/output.png)
