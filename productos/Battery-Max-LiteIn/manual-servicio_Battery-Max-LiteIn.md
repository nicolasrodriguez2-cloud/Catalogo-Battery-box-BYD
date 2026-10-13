# Battery-Max LiteIn — Manual de servicio

- **Producto:** Battery-Max LiteIn (Battery-Max LiteIn)
- **Tipo de documento:** Manual de servicio
- **Versión/fecha del PDF:** V1.0
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/Service%20Manual_Battery-Max%20Litin_EN_V1.0-68524bc91b408.pdf
- **SHA-256 del PDF:** aade70f615628e2fb4d244fd7d841d61dceaebb390faf09892856503683df718
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/Service Manual_Battery-Max Litin_EN_V1.0-68524bc91b408.pdf
- **Conversión:** pymupdf4llm 1.28.2, 18 págs.

> ⚠ Este documento tiene 8 tabla(s) dudosa(s) y 1 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BATTERY-MAX LITEIN Service Manual** 

LITEIN 30.0/ 37.5/ 45.0/ 52.5/ 60.0/ 67.5/ 75.0/ 82.5 

Version 1.0 



Always make sure to use the latest version of this service manual, available at: https://bydbatterybox.com

<!-- pág. 2 -->
> ⚠ REVISAR: página sin texto extraíble (imagen/escaneo); no se aplicó OCR.


<!-- pág. 3 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **Content** 

|**1. Overview....................................................................................................................................................4**|
|---|
|1.1. Claim and Contact...........................................................................................................................4|
|1.2. General Steps..................................................................................................................................5|
|**2. Error Analysis.............................................................................................................................................6**|
|2.1. System cannot be turned on...........................................................................................................6|
|2.2. LED is red or off after a period of operation...................................................................................6|
|**3. Frequently Asked Questions..................................................................................................................... 7**|
|3.1. WiFi Issues.......................................................................................................................................7|
|3.2. Firmware Update Issue...................................................................................................................8|
|3.3. Changes in SOC...............................................................................................................................8|
|**4. Tools and Methods....................................................................................................................................9**|
|4.1. BCP（For LITE/LITEIN）..................................................................................................................9|
|4.2. Faulty module identification.........................................................................................................10|
|4.2.1. Single Module Failure.........................................................................................................10|
|4.2.2. Communication failure between modules........................................................................10|
|4.2.3. Voltage Measurement........................................................................................................10|
|4.2.4. Under-voltage....................................................................................................................12|
|**Appendix 1 Event and Operation................................................................................................................13**|



3

<!-- pág. 4 -->
Service Manual V 1.0 

Shenzhen BYD Electronic Co., Ltd. 

## **1. Overview** 

This manual is subject to technical revisions, and no responsibility is accepted for the accuracy of this manual. 

Before contacting the service team, please read this manual to try to solve the problem. If the problem remains, please contact BYD service team. 

**Attention: High Voltage! Improper handling can cause danger and damage.** 

**Important Note: The installation and all other kinds of works or measurements in correlation with the battery are only allowed by professional and qualified personnel.** 

### **1.1. Claim and Contact** 

If after completing the inspection with the steps described in this manual or under the guidance of the service team, it is confirmed that there could be a part failure that needs to be resolved by replacement. 

If the appearance of the product is damaged, please take photos of the product and the packaging on site and provide them to the service team. 

**The contact information for the service team is as follows:** 

Africa BYD Global Service Email bboxservice@byd.com Telephone +86 755 89888888- 47175 (CN) Address No.3009, BYD Road, Pingshan, Shenzhen, 5118118, P.R. China Website www.bydbatterybox.com / www.bydenergy.com 

4

<!-- pág. 5 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

### **1.2. General Steps** 

If there is any problem of the battery system, please follow the steps for an initial check. 

> ⚠ REVISAR TABLA — pág. 5: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Inspection items**|**Inspection steps**|
|---|---|---|
|1|Settings|Check if the settings are correct. Refer to the latest “BATTERY-MAX<br>LITEIN Operating Manual” or “BATTERY-MAX LITEIN Quick Start<br>Guide”, available at:<br>https://bydbatterybox.com. Make sure the<br>inverter is configured correctly.|
|||1)<br>Please check if the wrong port is plugged in;|
|2|External connections|2)<br>Check whether the cable is loose;<br>3)<br>Check the cable itself for any problems.|
|3|Latest Firmware|Check if the firmware is latest, if not, please use the BCP to update<br>it.|
|||**Note: It is important that the battery system is switched on before**<br>**the inverter! Otherwise, the PDU might not start and not show any**<br>**reaction (e.g., no Wi-Fi).**<br>(mind the sequence)<br>1)<br>Switch off the inverter;<br>2)<br>Switch off the air switch on the PDU|
|4|Restart|3)<br>Press the button on the PDU for 5 seconds<br>4)<br>Rotate the handle switch 90° counterclockwise；<br>5)<br>Wait at least 3 minutes;<br>6)<br>Rotate the handle switch 90° clockwise;<br>7)<br>Press the button on the PDU for 3 seconds<br>8)<br>Switch on the air switch on the PDU<br>9)<br>Turn on the inverter.|
|||The system runs properly if :<br>- Inverter displays battery SOC correctly;|
|5|Checking the correct<br>operation|- System charges/discharges.<br>**Note: If you can not complete the commissioning, then turn off the**<br>**battery before you leave the site. If it is not possible, remove the**<br>**PDU and then close the PDU. After that, contact the service team.**|



5

<!-- pág. 6 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **2. Error Analysis** 

If a fault occurs, the red LED on the PDU will light up. 

If there is an alarm but it has not yet failed, the yellow LED on the PDU will light up. 

If the battery is functioning properly, the green LED on the PDU stays on and the yellow LED and red LED go off. 

### **2.1. System cannot be turned on** 

- 1) PDU shows no reaction. 

- a. If you are commissioning the battery, but Wi-Fi is not detected and the LED on the PDU does not turn on, please try to restart the system in the correct sequence (refer to Step 4 in **1.2** ). 

- b. If the problem remains, please refer to **4.3** to check the voltage. If the voltage is normal, replace the PDU 

- c. If the voltage is abnormal, please refer to the events on BCP to identify the faulty module. 

- 2) The relay is heard to trip immediately after battery is powered on. 

> ⚠ REVISAR TABLA — pág. 6: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Inspection items**|**Inspection steps**|
|---|---|---|
|1|Wiring|1)<br>Switch off the inverter and battery, disconnect all external cables and<br>restart the battery in the correct sequence.<br>2)<br>If it works, check if the inverter is short-circuited; If the problem<br>remains, proceed to the next step.|
|||Refer to**4.3**for the voltage check:|
|2|Voltage|1)<br>If the voltage is abnormal, identify the faulty module referring to**the**<br>**events on BCP**.|
|||2)<br>If the voltage is normal, replace the PDU|



### **2.2. LED is red or off after a period of operation** 

Restart the system in the correct order: 

- 1) If successful: 

- a. If events appear on the BCP, please refer to Appendix 1 for more details. 

- b. If not, please download the logs and send them to BYD service team. Repair under the guidance of the service team. 

(Sporadic alarms can be difficult to detect because they only occur occasionally. Therefore, it is very important to download and provide all historical battery log files available to find the root cause.) 

- 2) If failed: Refer to **2.1** . 

6

<!-- pág. 7 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **3. Frequently Asked Questions** 

### **3.1. WiFi Issues** 

Common WiFi failures: no Wi-Fi signal / unstable WiFi / unable to connect to WiFi. 

When these failures occur, follow the steps below: 

##### **1) Disconnect LAN cable** 

Remove the LAN cable when your device is connecting to the Wi-Fi. After that you can connect it again to the Internet. 

##### **2) Try other mobile devices** 

Sometimes the problem comes from the mobile device itself, try to see if other mobile devices can connect to the Wi-Fi. 

##### **3) Reset the WiFi** 

Press the button on the PDU once one second for WiFi reset 

##### **4) Restart the system** 

Restart the system in the correct sequence (refer to Step 4 in **1.2** ). 

##### **5) Replace WiFi unit** 

If none of the steps above work, please replace the WiFi unit on PDU. 

7

<!-- pág. 8 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

### **3.2. Firmware Update Issue** 

##### **1) Fix WiFi** 

If it is caused by unstable WiFi, please refer to 3.1. 

##### **2) Restart** 

Restart the system in the correct sequence. 

##### **3) Try again with other devices.** 

Sometimes the problem comes from the mobile device itself, try to see if other devices can update. 

##### **4) Replace the PDU** 

If none of the above steps work, please replace the PDU 

### **3.3. Changes in SOC** 

##### **1) SOC jumps** 

The SOC of a battery cannot be measured. It is an estimated value. In general, the state of charge (SOC) of a battery is estimated using the voltage, but other factors such as temperature, current flow and charging behavior also play a role. The calculation of the SOC is generally more precise if the battery regularly sees full cycles. It is normal to have a SOC correction/calibration now and then. 

##### **2) SOC at commissioning** 

New modules have 30% SOC upon delivery. A new PDU might show a different SOC at the beginning (mostly 30%). However, this is only to be understood as a placeholder value, as a new PDU cannot measure the SOC of modules. As soon as the system starts to run (charge/discharge), the SOC is corrected gradually. The SOC calibration is completed after the latest full cycle. 

8

<!-- pág. 9 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **4. Tools and Methods** 

### **4.1. BCP** （ **For LITE/LITEIN** ） 

With the BCP you can: 

- 1) read the battery information; 

- 2) update firmware; 

- 3) export / download battery logs. 

The BCP is constantly being improved and updated. Make sure to use the latest program version. 

For the service analysis, please download and provide the data / logs as described in the program instructions. 

##### **Note: You need a Windows computer that can connect to the battery WiFi.** 



9

<!-- pág. 10 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

### **4.2. Faulty module identification** 

#### **4.2.1. Single Module Failure** 

When a module failure occurs, you can view the number of the failed module through BCP. 

#### **4.2.2. Communication failure between modules** 

When the BCP indicates that a communication failure has occurred between modules, there may be a communication failure in this module or in the module below it. 

Try removing both modules separately to determine the which is fault. If the BCP shows that module 1 has a communication failure, it may be caused by PDU or module 1. You can remove module 1 and restart the system to check whether the system can operate normally, if not, please try another PDU. 

#### **4.2.3. Voltage Measurement** 

##### **ATTENTION: High voltage!** 

You can see the max./min. cell voltage in the BCP. You can also get the detailed voltage of the modules and cells in the BCP or measure it manually according to the below description: 

##### **Measurement of Tower Voltage** 

Disconnect the PDU and measure the tower voltage between the P+ and P- for PDU. 





**B+ and B- of tower voltage** 

**Measurement of tower voltage** 

10

<!-- pág. 11 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

##### **Measurement of Module Voltage** 

**Note: The nominal voltage for per module is 64.8V~88.8V** 



**Individual module measurement** 

If the measured voltage of the tower deviates from the nominal value, please check the voltage of the individual modules 

11

<!-- pág. 12 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

#### **4.2.4. Under-voltage** 

A module in which one of the cells has a voltage of <1.5 V is in over-charged (check with BCP if possible). 

A LITEIN module with >64.8 V should be fine and you can continue to check other points according to the service manual. Always make sure the version of firmware is the latest! If the module voltage is <64.8 but the single cell voltage is >1.5 V, the battery needs to be charged as soon as possible. 

If only one module is in under-voltage: remove that module and try to start the system without it (if the number of the remaining modules still meets the minimum module number requirement). Otherwise, make sure to avoid further discharge (e.g., remove PDU) 

If more than one, or all modules are in under-voltage: Contact the service team and make sure to avoid any further discharge of the battery (e.g remove PDU from the system) 

When contacting the service team, make sure to fill the service checklist completely and add the following information: 

- 1) Serial Numbers of the PDU and all (affected) modules; 

- 2) Tower voltage and individual module voltages of all modules (related to Serial Number) 

- 3) Detailed description of how and why the system reached under-voltage if known. Information of when the system was installed and commissioned and in which circumstance and when the under-voltage occurred. If the battery was never running before: Why did it never work before, and what was the status of the battery when the battery was left (on / off / Display). 

- 4) If possible: Logs from the battery using BCP showing the cell voltages and Initial Firmware Version of the Battery when under-voltage occurs. 

12

<!-- pág. 13 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **Appendix 1 Event and Operation** 

> ⚠ REVISAR TABLA — pág. 13: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|No.# Module<br>Failures|Failure within the modules|The number in front of ‘#’ represents the<br>number of the faulty module, please replace the<br>faulty module corresponding to the number.|
|Over current<br>occurs in<br>charging/<br>discharging|1) The charging/discharging power<br>is too high and the inverter fails to<br>limit the charging/discharging<br>current in time.<br>2) PDU fault.|1)<br>Check whether there is a high-power load<br>starts when this fault occurs. If yes, check<br>whether the load power is within the power<br>range of the inverter:<br>a) If yes, reduce the loads to ensure that the<br>power is within the range.<br>b) If not, please also contact the inverter<br>service; If not, proceed to the next step.<br>2)<br>Restart, if the problem remains, replace the<br>PDU|
|Over/under<br>temperature in<br>charging/discha<br>rging|1) Ambient temperature too high/<br>low<br>2) PDU fault|1) Determine if the ambient temperature is<br>suitable for battery operation<br>2) Restart, if the problem remains, replace the<br>PDU|



13

<!-- pág. 14 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 14: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|Memory<br>Abnormal|Memory chipset fault.|Restart, if the problem remains, replace the<br>PDU|
|Communications<br>failure between<br>modules|Single or multiple modules are not<br>recognized|Please refer to**4.2.2**for processing|
|||1) Disconnect external connections.|
|Pack V-sensor<br>failed|Battery voltage is too different from<br>the output voltage|2) Restart, if the problem remains, check if<br>the fuse in the PDU is blown.<br>3) If the fuse is normal, replace the PDU|
||1) When the SOC is 0% or 100%, there|Restart, if the problem remains, replace the<br>PDU|
|Current sensor<br>failed|is still discharge/charge current in the<br>system.<br>2) Current value exceeds system limit.|(If it’s possible, observe the current value on<br>the BCP and on the inverter during charging<br>or discharging the battery, and record the<br>results for feedback to BYD service team).|



14

<!-- pág. 15 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 15: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|Relay failed|Positive or negative relay<br>disconnected|Restart, if the problem remains, replace the PDU|
||The voltage between P+ and P- of the|1)<br>Check whether the power cable connection is<br>correct (if correct, proceed to the next step;<br>if incorrect, then connect the power cable<br>correctly).<br>2)<br>Check whether there is a high-power load<br>starts when this fault is reported.|
|Failure to<br>start|PDU is 0<br>1) DC connection faults|If yes, check whether the load power is within<br>the power range of the inverter:|
|pre-charge|2) Inverter DC side short circuit<br>3) PDU main circuit failure|a) If yes, stop using some loads to ensure<br>that the power is within the range.<br>b) If not, please also contact the inverter<br>service;<br>If not, proceed to the next step.<br>3)<br>Restart, if the problem remains, replace the<br>PDU|
|||1)<br>Check if the settings are correct.<br>2)<br>Restart.|
|Parameter<br>Abnormal|1) Data loss when loading<br>parameters<br>2) BMU failure|3)<br>Use BCP to update the firmware and restart<br>again.<br>4)<br>If this is a parallel system, replace the<br>communication cable between the PDU.|
|||5)<br>If the problem remains, replace the PDU|



15

<!-- pág. 16 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 16: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Op**|**eration**|
|---|---|---|---|
|Incorrect<br>module number|1) The number of setting modules is<br>different from the actual number<br>installed<br>2) Different amounts of modules in<br>parallel system|1)<br>2)<br>3)|Check if the settings are correct.<br>Make sure that the amount of modules<br>in the parallel system is the same<br>If the problem remains, replace the<br>PDU|
|Internal<br>communication<br>failure|1) Internal CAN communication fault.<br>2) BMU and BMS communication failure<br>3) Communication interface failure<br>4) Address assignment failure|1)<br>2)<br>3)<br>4)|Check if the terminal resistor is normal<br>Check whether the communication<br>cable is faulty.<br>For a single tower system, replace the<br>PDU<br>For multiple tower systems, separate<br>them into single towers, and follow the<br>instructions according to the events on<br>each display. If there are no events on<br>each display, but this event remains<br>after connecting all the towers, check<br>whether the RJ45 ports have<br>mechanical damage.|



16

<!-- pág. 17 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 17: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
||1) Inverter not matched|1)<br>Check the settings:<br>If the Terminal Res is normal.<br>Default Set<br>2)<br>Check the connection|
|Communicatio<br>n failure with<br>the inverter|2) Communication cable failure<br>between battery and inverter<br>3) Wrong type of battery/inverter is<br>set|Does the inverter properly detect the battery?<br>Check if the inverter detects the battery<br>parameters (e.g., SOC, battery temperature)<br>correctly. If not, check the cabling, especially the<br>pin definition.<br>3)<br>Restart in the correct order.<br>4)<br>If none of the above work, replace the PDU|
|Pre-charge<br>not completed|1) Inverter failure that prevents the<br>battery from pre-charging it<br>2) PDU fault|1)<br>Restart<br>2)<br>If the problem remains, turn off the battery<br>and disconnect all the power cables from the<br>inverter, black start through the LCD.<br>a) If the problem remains, replace the PDU;<br>b) If the problem disappears, check the<br>connection of power cables between the<br>battery and the inverter.|
|Update<br>Failed|1) Data loss during update<br>2) BCP fault<br>3) PDU fault|1)<br>Restart.<br>2)<br>Re-download BCP or use another device，<br>update the firmware again and restart.<br>3)<br>If the problem remains, replace the PDU|



17

<!-- pág. 18 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 18: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|DC switch<br>abnormal|Hand switch abnormal|Restart, if the problem remains, replace<br>the PDU|
|Fire<br>Alarm|1) Smoke or overheating is detected in the<br>PDU<br>2) A fire has been detected in the battery<br>PDU.|For Cause 1<br>1) Send trainedpersonnel to the site<br>and observe thesystem for 30 minutes<br>from a safedistance. If there is smoke or<br>fire,remotely power off the<br>system,evacuate the onsite personnel as<br>soonas possible, and call the<br>fireemergency number.<br>2) If no exception is found during<br>observation, manually clear the alarm<br>remotely by restart the system. If the<br>alarm persists, contact BYD service.|
|||For Cause 2<br>Do not open the PDU doors. Evacuate<br>onsite personnel.<br>Contact BYD service|
||1) Ground cable not connected|1) Check the ground cable ( ground<br>cable of battery and inverter should be<br>connected separately)|
|Insulation<br>failures|2) Ground cable fault<br>3) Module Leakage<br>4) PDU leakage|2) Restart, if the problem remains,<br>replace the PDU<br>If the problem still remains, find the<br>faulty module by BCP or exclusionary<br>method|
|Chip Function<br>Alarm|Chip running lagging|Restart, if the problem remains, replace<br>the PDU|



18
