# HIL Based CLBC using LabVIEW and Thingspeak Cloud


## INTRODUCTION
In recent years, the demand for efficient and reliable power conversion systems has surged, driven by the growing integration of renewable energy sources, electric vehicles, and portable electronic devices. Among various power conversion topologies, the boost converter stands out as a fundamental and widely used DC-DC converter that steps up a lower input voltage to a higher output voltage. Its simplicity, compact design, and high efficiency make it an essential component in numerous applications, ranging from photovoltaic systems to battery-powered devices. However, the performance of an open-loop boost converter is significantly affected by input voltage variations, load fluctuations, and component tolerances. These disturbances can lead to instability, output voltage deviations, and reduced system reliability. To address these challenges, closed-loop control mechanisms are implemented to dynamically regulate the output voltage and enhance the overall performance of the converter. 

<img width="49%" height="496" alt="Font" src="https://github.com/user-attachments/assets/e82e3dd3-132c-4ae3-a05a-a0dbabb483d9" /> <img width="49%" height="640" alt="Back" src="https://github.com/user-attachments/assets/3440f65f-eac5-4f4d-86b3-3258ce2d8b2f" />


This project presents the design and implementation of a closed-loop boost converter using a feedback control system to maintain a constant output voltage under varying operating conditions. A suitable control algorithm, typically Proportional-Integral (PI) or Proportional Integral-Derivative (PID), is deployed to compare the output voltage with a predefined reference and adjust the duty cycle of the switching device accordingly. The controller is implemented using Arduino UNO, enabling real-time monitoring and correction of output variations. 

## HOW IT WORKS?
The feedback circuit senses the output voltage.
A controller (Arduino/LabVIEW PID) compares it with the reference voltage.
The PWM duty cycle is adjusted to maintain the set voltage.
The boost converter steps up the voltage using inductor energy storage and high-speed switching.

## PROCEDURE
1) Construct the hardware for boost converters as show in this figure.
   
<img width="979" height="651" alt="circuit" src="https://github.com/user-attachments/assets/5f3d8530-3c34-4d26-a191-bbc8144b5514" />

3) Code Your Aduino UNO R3 using the tool pallets of LabVIEW as show below.

<img width="926" height="453" alt="Overall_code" src="https://github.com/user-attachments/assets/a18d7c39-1fd4-4cf3-ac1b-0027ffafa8d2" />

5) Code for generating PWM pulses using PID algoritm to convert OLBC (open loop boost converter) into CLBC (closed loop boost converter).
   
<img width="920" height="427" alt="PID_code" src="https://github.com/user-attachments/assets/8a446e1f-f236-4b46-8771-71664aa09eca" />

7) Simultaneously you will get your Control and Montoring tools at the control and Monitoring panel of the LabVIEW. Arrange it as shown.
   
<img width="873" height="481" alt="Control_Monitoring_panel" src="https://github.com/user-attachments/assets/e6036a65-b474-411f-be25-a83357be5842" />

9) Tune your PID to get the desired output at quickest possible range.

<img width="871" height="541" alt="PID_tunning_setup" src="https://github.com/user-attachments/assets/e608d015-b00d-4c42-b9e7-13bf73a7d112" />

10) Configure Port and baudrate for type of Arduino connected.

<img width="866" height="462" alt="Configuration_panel" src="https://github.com/user-attachments/assets/27730f6f-f9d4-4609-a4db-2a80cf273ef1" />

11) Simultaniously You can montior your readings on front panel as well as on the cloud (Thingspeak IOT)

<img width="872" height="482" alt="IOT_Thingspeak_integration" src="https://github.com/user-attachments/assets/6f8da41c-427c-4b6f-aac4-ad92d1ee96e4" />


## FEATURES
1) Physical control of output voltage using hardware POT (potientiometer connected).
2) Manual Control of output voltage using LabVIEW slider.
3) Automatic Control of output Voltage based on desired voltage setting by user (PID) - No need of varying POT or slider.


## APPLICATIONS
Renewable energy systems (solar PV voltage regulation).
Battery-powered devices needing higher voltage.
Power electronics research and education.

## VIDEO DEMONSTRATION
1) Manual Open loop control using Hardware POT and LabVIEW Slider.



https://github.com/user-attachments/assets/25b60313-9223-4363-91cd-f76872a88439



2) Automatic Closed loop control.



https://github.com/user-attachments/assets/1b6dd405-033b-4a6c-94da-8c4b0ea18c5f




## PROJECT REPORT
[SS2_project_sem6.pdf](https://github.com/user-attachments/files/29436566/SS2_project_sem6.pdf)

