# Applied_Model_based_design_mini_project

## SIMPLE AUTOPILOT DESIGN

The equations governing the motion of an aircraft are a very complicated set of six nonlinear coupled differential equations. However, under certain assumptions, they can be decoupled and linearized into longitudinal and lateral equations. Aircraft pitch is governed by the longitudinal dynamics. In this example we will design an autopilot that controls the pitch of an aircraft.

In this example we will simulate the linearized aircraft model with the state-feedback controller designed earlier in the example. We will specifically use the linearized state-space model obtained in Aircraft Pitch: System Modeling page.


 # This is a basic demo of simulation of an SIMPLE AUTOPILOT DESIGN
 using Matlab & Simulink. This file complements [this YouTube video](https://youtu.be/CJGlKCfGEA0)

![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Equation.png)

The above equations match the general, linear state-space form.
![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/difference.png)


Open Simulink and open a new model window.
Insert a Step block from the Simulink/Sources library.
To provide an appropriate step input at t=0, double-click the Step block and set the Step time to "0". Also set the Final value to "0.2" to represent the 0.2-radian reference we are assuming.
Insert a Demux block from the Simulink/Signal Routing library. Double-click on the block and enter "3" for the Number of outputs; one output for each of the three state variables.
Insert a Scope from the Simulink/Sinks library and connect the third output of the Demux block to the scope. We will only plot the third state variable which corresponds to the system's output which is the aircraft's pitch theta.
Add Terminator blocks from the Simulink/Sinks library to the two signals of the Demux block that we are not plotting.
Insert a State-Space block from the Simulink/Continuous library and connect the input to the Step block and the output to the Demux block.
Double-click on the State-Space block and enter the system parameters as shown in the figure below.

![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Picture1.png)


Note, that in the above figure the $C$ matrix is entered as a 3x3 identity matrix using the eye command rather than [0 0 1] as given in the original state-space equations. The reason for this is because in state-feedback control it is assumed that all of the state variables are measured, not just the output. If this is not the case, then an observer needs to be designed to estimate any state variables that are not measured. Refer to the Introduction: State-Space Methods for Controller Design page, for further detail.

When finished, the completed model should appear as shown below.


![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Picture3b.png)



 ## Building the state-space model
 
 We will now build a Simulink model of the above equations. One option is to build a model of the plant with state-feedback that emulates the figure shown below.
 ![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/statefeedback_pitch2.png)
 
 

## Screenshot of the model
![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Model.png)


## output of the model


![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/Picture5.png)



![Autopilot - Simulink](https://github.com/AMohammedAsif/Applied_Model_based_design_mini_project/blob/main/output.png)
