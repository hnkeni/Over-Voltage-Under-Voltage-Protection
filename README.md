#  Under-Voltage and Over-Voltage Protection System with ThingSpeak Cloud Monitoring 
 Introduction 
 Electrical appliances and industrial equipment require a stable voltage supply for 
 efficient operation. However, voltage fluctuations can occur due to power grid 
 instability, load variations, or faulty wiring. Both  under-voltage  and  over-voltage 
 conditions can cause severe damage to electronic devices. 
 This project aims to develop an  automatic voltage  protection system  using 
 Arduino  ,  relay module  ,  voltage and current sensors  ,  and  LabVIEW  for local 
 real-time monitoring. Additionally,  ThingSpeak IoT  integration  is implemented to 
 send  voltage data to the cloud, allowing users to  monitor it remotely via a web 
 dashboard.
 
 <img width="688" height="490" alt="image" src="https://github.com/user-attachments/assets/7928662f-6d18-4994-80b7-5f16c1b1b6bd" />

Working Principle 

Step 1: Voltage Measurement 

●  The  voltage sensor  reads the input voltage.

●  The  current sensor  monitors the load current. 

Step 2: Data Processing 

●  Arduino reads sensor data and compares voltage with predefined limits. 

●  The data is  displayed in LabVIEW  for local monitoring. 

Step 3: Relay Control 

●  The relay  disconnects the power supply  if voltage  is unsafe. 

●  The Load status is updated  locally on LabVIEW  and  logged on  ThingSpeak  . 

Step 4: IoT Data Transmission to ThingSpeak 

●  Voltage and current data are uploaded at regular intervals to ThingSpeak via HTTP API 
calls.

Virtual Interface

<img width="612" height="354" alt="image" src="https://github.com/user-attachments/assets/88e58845-612a-4dc7-94a9-fdb1cabb4b62" />

<img width="621" height="361" alt="image" src="https://github.com/user-attachments/assets/70f78b73-4efe-4dd7-b5f5-01fb58462dec" />

IOT Interface

<img width="694" height="728" alt="image" src="https://github.com/user-attachments/assets/9cc485d8-0867-43be-b16f-19e450819c02" />


Circuit Diagram


<img width="533" height="820" alt="image" src="https://github.com/user-attachments/assets/1637bac6-cfed-4118-b6eb-6aa9eadabd65" />

Working Procedure 

A. System Initialization and Sensor Calibration 

1.  Power Up:
   
○  Connect the 9V battery to power the Arduino and peripherals. 

○  Initialize the Arduino, LabVIEW, and Wi-Fi module. 

3.  Sensor Calibration:
    
○  Verify that the voltage and current sensors are providing accurate readings. 

○  Use the potentiometer to simulate different voltage levels and adjust calibration
as necessary. 

B. Local Monitoring and Control via LabVIEW 

1.  Data Acquisition:
   
○  The Arduino collects real-time data from the voltage and current sensors. 

○  Data is transmitted via serial communication to LabVIEW running on the Linux 
system. 

3.  Real-Time Display:
   
○  LabVIEW displays numeric indicators, LED statuses, and graphs that show live 
voltage trends.

○  The system’s status (Normal, Under-Voltage, Over-Voltage) is updated in 
real-time. 

5.  Relay Operation:
   
○  Based on the processed sensor data, LabVIEW helps visualize whether the relay 
is in the ON (normal) or OFF (fault) state. 

C. IoT Data Transfer and Cloud Monitoring with ThingSpeak 

1.  Data Preparation:
    
○  The Arduino processes voltage and current data and formats it for transmission. 

3.  Cloud Upload:
   
○  Using the ESP8266/ESP32 module, the Arduino sends the formatted data to the 
ThingSpeak cloud at set intervals. 

○  API keys are used to authenticate and ensure that data is correctly uploaded to 
the designated ThingSpeak channel. 

5.  Remote Monitoring:
   
○  Users access the ThingSpeak web dashboard from any internet-connected 
device. 

○  The dashboard displays live voltage and current data through real-time graphs 
and numerical indicators. 

7.  Data Logging:
   
○  ThingSpeak logs historical data, allowing users to review trends and analyze 
voltage fluctuations over time.

Plots

<img width="571" height="437" alt="image" src="https://github.com/user-attachments/assets/d0b8c7aa-db3d-47ef-9a3b-e30f59582c67" />

<img width="567" height="912" alt="image" src="https://github.com/user-attachments/assets/336d0ad9-6736-4dae-9922-6c1a66ff31f8" />

Conclusion: 

The Under-Voltage and Over-Voltage Protection System with ThingSpeak enhances safety by 
enabling real-time local monitoring (LabVIEW) and remote monitoring (ThingSpeak cloud). The 
integration of Arduino, LabVIEW, and ThingSpeak ensures that users can track voltage levels 
from anywhere, while automated relay control protects connected devices from unsafe voltage 
levels. 




