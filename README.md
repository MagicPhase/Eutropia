
![Screenshot 2022-04-27 044346](https://user-images.githubusercontent.com/104283546/165511208-096bcb36-2eb3-4768-abb3-4975332bfc1a.jpg | width=500)
![Screenshot 2022-04-27 044554](https://user-images.githubusercontent.com/104283546/165511366-3dfcaa68-a1d1-427f-8283-d8a27caedd4f.jpg | width=500)



# Eutropia
Open Source ESP32 Multi Sensor Platform I/O

This PCB design offers numerous optional features and configurations built around the ESP-WROOM-32 30PIN module. 

## Feature list:

>2 High Power Outputs  
2 Optocouple Outputs  
2 Medium Power Outputs  
Current/Voltage sensing  
RTC Clock  
Low Pressure Sensor  
Accelerometer/Gyro  
Humidity Sensor  
Water Ingress Sensor  
1 Input/Output Port  
1 Input Port  
2 Neo Pixel LEDs  
Mounting Holes For Nextion 2.8" Serial Display

## ESP32 I/O configuration:

>D39(I) Attached to INA3221 programable warning for over current monitor.  
>D36(I) Labelled (AUX1) pin is attached to 3-pin header for general use as default. JP3 can connect the MPU (INT) pin for auto calibration. JP1 can connect to water ingress sensor. Only one function can be used.  
>D35(I) Input for thermal sensor near CH2 FET.  
>D34(I) Input for thermal sensor near CH' FET.  
>D33(IO) Output PWM for CH2 FET via driver (MIC4127 CHB).  
>D32(IO) Output PWM for CH1 FET via driver (MIC4127 CHA).  
>D23(IO) Labelled (AUX2) pint is attached to 3-pin JST header for general purpose.  
>D22(IO) I2C SCL pin.  
>D21(IO) I2C SDA pin.  
>D17(IO) Serial TX2 pin.  
>D16(IO) Serial RX2 pin.  
>D19(IO) Output PWM for CH4 FET.  
>D18(IO) Output PWM for CH3 FET.  
>D5(IO) Attached to 2 JTS headers with 4.7k pullup resistor. These are intended for DS18D20 temp sensors.  
>D1(IO) Attached to the input of the Neo Pixel (SK6805). This pin is also used for Serial1 during programing.  
All other IO pins are left unattached as to not interfere during WiFi operations.  

## Board Headers:
>CH1 High Output XT30 Female  
>CH2 High Output XT30 Female  
>CH3 Low Output JST_PH_B2B-PH-K_1x02_P2.00mm  
>CH4 Low Output JST_PH_B2B-PH-K_1x02_P2.00mm  
>HEADER1 I2C PULLUP PinHeader_2x02_P2.00mm  
>HEADER2 VIN/5V SELECT PinHeader_2x03_P2.00mm  
>HEADER3 FET/OPTO SELECT PinHeader_2x03_P2.00mm  
>HEADER4 I2C HEADER	PinHeader_1x04_P2.00mm  
>HEADER5 Serial2  PinHeader_1x04_P2.50mm  

![FRONT](https://user-images.githubusercontent.com/104283546/164965498-b922744d-df44-4200-ac65-a51fc8249713.jpg)
![BACK](https://user-images.githubusercontent.com/104283546/164965507-1e455e87-d51f-41b4-841b-f92ce21fc81c.jpg)


Two High Power FET's capable of >50watt output. These channels have current/voltage monitoring, thermal monitoring, and safety fuses. These outputs are selectable with two optocoupler drivers via a jumper header.
  
Two Medium power FET's capable of 10watt output. These channels Have selectable input voltages of either VIN(12-24) or 5V.
  
Three channels of current/voltage monitoring. Monitoring is split between the 2 high current channels and the remainder of all devices on the board. Total power usage is a sum of all three channels.
  
RTC clock is used for basic time keeping and has battery backup.
  
The low pressure sensor is an absolute pressure type and designed for low pressure monitoring of <10psi. The sensor has a metal port.
  
Accelerometer/gyro optional port is compatible with the MPU-6050 board. It is also possible to fit the MPU-9250, however the board will protrude from the top approximately 5mm and the two lower pins should be clipped. There is also a footprint on the main board for an MPU-6050 chip with selectable I2C address. If the chip is present on the main board, do not populate with an expansion board!
  
One input/output via a three pin JST(2mm pitch) header.
  
One input only pin via a three pin JST(2mm pitch) header. This input is a shared input. See D36 pin configuration.
  
  
