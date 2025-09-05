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
