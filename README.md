# Water-Tank-Contreoller-Simulink
Dual Gravity Drain Tank System with PID Control Using Simulink
This tutorial guides you through the steps to design a PID controller for a dual gravity drain tank system using Simulink. The objective is to maintain the liquid level in the second tank by adjusting the pump flow rate.

System Overview
The system consists of two tanks with the following setup:

First Tank: Receives water from a pump.
Second Tank: Receives water drained from the first tank.
Reservoir: The second tank drains into a reservoir.
Pump: Controls the flow into the first tank.
Valve: Allows direct flow into the second tank (not used in this example).
The goal is to design a level controller that adjusts the pump flow rate to maintain a specified level in the second tank.

Steps to Implement the PID Controller
1. Setting Up the Model
Create a Simulink Model:

Add components for the tanks, pump, and sensors.
Ensure the flow from the pump enters the first tank and then drains into the second tank.
Initial Setup:

Go to the APMonitor.com website.
Navigate to the Process Control course.
Select Homework and then Problem 3.
2. Obtaining a First-Order Plus Dead Time (FOPDT) Model
Perform Step Tests:

Conduct step tests or pulse response tests on the pump output.
Record the liquid levels in both tanks over time.
Data Analysis:

Extract the data and save it to a file.
Use Excel to fit a FOPDT model to the data.
Input the time, pump output, and tank levels into the Excel sheet.
Use Excel Solver to minimize the sum of squared errors and obtain model parameters: gain (K), time constant (τ), and dead time (θ).
3. PID Controller Tuning
Initial PID Parameters:

Calculate initial PID parameters using the FOPDT model:
𝐾
𝑐
=
1
𝐾
K 
c
​
 = 
K
1
​
 
𝜏
𝑖
=
𝜏
τ 
i
​
 =τ
𝜏
𝑑
=
0
τ 
d
​
 =0
Configure PID Controller in Simulink:

Insert a PID Controller block from the Simulink Library.
Set the PID parameters:
Proportional gain 
𝐾
𝑐
K 
c
​
 
Integral gain 
𝐾
𝑐
𝜏
𝑖
τ 
i
​
 
K 
c
​
 
​
 
Derivative gain 
0
0
Connect PID Controller:

Compare the setpoint with the measured level to calculate the error.
Feed the error into the PID controller.
Connect the PID controller output to the pump input.
4. Simulation and Results
Run the Simulation:

Set the initial setpoint for the second tank level.
Run the simulation and monitor the response.
Adjust the setpoint dynamically and observe the controller's performance.
Analyze Performance:

Plot the tank levels and pump output.
Ensure the controlled level reaches and maintains the setpoint.
Conclusion
By following these steps, you have successfully designed and implemented a PID controller for a dual gravity drain tank system using Simulink. The controller adjusts the pump flow rate to maintain the desired liquid level in the second tank.

Example Files
Download the example files from the provided link and extract them. Ensure all files are properly saved and extracted before running the Simulink model.

Contact
For further assistance or questions, please contact:

Email: fikret.yildirim00@gmai.com
GitHub: expactopatronas
