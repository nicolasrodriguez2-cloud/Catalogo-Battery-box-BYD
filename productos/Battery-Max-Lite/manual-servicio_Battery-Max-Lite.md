# Battery-Max Lite — Manual de servicio

- **Producto:** Battery-Max Lite (Battery-Max Lite)
- **Tipo de documento:** Manual de servicio
- **Versión/fecha del PDF:** V1.0
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/Service%20Manual_Battery-Max%20Lite_EN_V1.0-68524b9b41076.pdf
- **SHA-256 del PDF:** 003ecd17b0be068c00feb69f8be78164a3fbd8d634df55e15cdc1c7af2fa1702
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/Service Manual_Battery-Max Lite_EN_V1.0-68524b9b41076.pdf
- **Conversión:** pymupdf4llm 1.28.2, 19 págs.

> ⚠ Este documento tiene 9 tabla(s) dudosa(s) y 1 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BATTERY-MAX LITE Service Manual** 

LITE 30.0/ 37.5/ 45.0/ 52.5/ 60.0/ 67.5/ 75.0/ 82.5/ 90.0 

Version 1.0 



Always make sure to use the latest version of this service manual, available at: https://bydbatterybox.com and www.bydenergy.com

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
|2.1. System cannot be turned on/off.....................................................................................................6|
|2.2. Indicator is red or off after a period of operation...........................................................................6|
|**3. Frequently Asked Questions..................................................................................................................... 7**|
|3.1. WiFi Issues.......................................................................................................................................7|
|3.2. Firmware Update Issue...................................................................................................................8|
|3.3. Changes in SOC...............................................................................................................................8|
|**4. Tools and Methods....................................................................................................................................9**|
|4.1. BYD Max Lite Plus (For Battery-Max Lite).......................................................................................9|
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

Before contacting the service team, please read this manual to try to solve the problem. If the problem persists, please contact BYD service team. 

**Attention: High Voltage! Improper handling can cause danger and damage.** 

**Important Note: The installation and all other kinds of works or measurements related to the battery are only allowed by professional and qualified personnel.** 

### **1.1. Claim and Contact** 

If after completing the inspection with the steps described in this manual or under the guidance of the service team, it is confirmed that there could be a part failure that needs to be resolved by replacement. 

If the appearance of the product is damaged, please take photos of the product and the packaging on site and provide them to the service team. 

##### **The contact information for the service team is as follows:** 

|**Europe**|**EFT-Systems GmbH**|
|---|---|
|Email|service@eft-systems.de|
||+49 9352 8523999|
|Telephone|+44 (0) 2037695998 (UK)<br>+34 91 060 22 67 (ES)<br>+39 02 87368364 (1T)|
|Address|Bruchtannenstr. 28, 63801 Kleinostheim, Germany|
|Website|www.eft-systems.de|



4

<!-- pág. 5 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

### **1.2. General Steps** 

If there is any problem of the battery system, please follow the steps for an initial check. 

> ⚠ REVISAR TABLA — pág. 5: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Inspection items**|**Inspection steps**|
|---|---|---|
|1|Settings|Check if the settings are correct. Refer to the latest “Battery-Max<br>Lite Operating Manual” or “Battery-Max Lite Quick Start Guide”,<br>available at: https://bydbatterybox.com and www.bydenergy.com.<br>Make sure the inverter is configured correctly.|
|||1)<br>Please check if the wrong port is plugged in;|
|2|External connections|2)<br>Check whether the cable is loose;<br>3)<br>Check the cable itself for any problems.|
|3|Latest Firmware|Check if the firmware is the latest, if not, please use the BYD Max<br>Lite Plus to update it.|
|||**Note: It is important that the battery system is switched on before**<br>**the inverter! Otherwise, the PDU might not start and not show any**<br>**reaction (e.g., no Wi-Fi).**<br>(mind the sequence)<br>1)<br>Switch off the inverter;<br>2)<br>Switch off the air switch on the PDU|
|4|Restart|3)<br>Press the LED button on the PDU for 5 seconds<br>4)<br>Rotate the handle switch 90° counterclockwise；<br>5)<br>Wait at least 3 minutes;<br>6)<br>Rotate the handle switch 90° clockwise;<br>7)<br>Press the LED button on the PDU for 3 seconds<br>8)<br>Switch on the air switch on the PDU<br>9)<br>Switch on the inverter.|
|5|Check if the system<br>operates properly|The system runs properly if :<br>- Inverter displays battery SOC correctly;<br>- System charges/discharges.<br>**Note: If you cannot complete the commissioning, then turn off the**<br>**battery before you leave the site. If it is not possible, remove the**<br>**PDU and then close the cabinet. After that, contact the service**<br>**team.**|
|6|Black start|1) If you are not sure if the fault is from the battery system or<br>external circuits, you can try a black start by disconnecting all<br>external cables, and restart the system, after the battery is on, press<br>the button again for 3 seconds.|



5

<!-- pág. 6 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **2. Error Analysis** 

If a fault occurs, the indicator on the cabinet will be red; if the indicator is green, it means the battery is working properly. 

### **2.1. System cannot be turned on/off** 

- 1) PDU shows no reaction. 

- a. If you are commissioning the battery, but Wi-Fi is not detected and the indicator on the cabinet does not turn on, please try to restart the system in the correct sequence (refer to Step 4 in **1.2** ). 

- b. If the problem persists, please refer to **4.3** to check the voltage. If the voltage is normal, try another PDU if available. 

- c. If the voltage is abnormal, please refer to the events on BYD Max Lite Plus to identify the faulty module. 

- 2) The relay trips immediately after battery is powered on. 

> ⚠ REVISAR TABLA — pág. 6: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Inspection items**|**Inspection steps**|
|---|---|---|
|||1)<br>Try to black start..|
|1|Wiring|2)<br>If it works, check if the inverter is short-circuited; If the problem|
|||persists, proceed to the next step.|
|||Refer to**4.3**for the voltage check:|
|2|Voltage|1)<br>If the voltage is abnormal, identify the faulty module referring to the<br>events on BYD Max Lite Plus.|
|||2)<br>If the voltage is normal, try another PDU if available.|



3) The system can not be turned off. 

If you cannot turn off the system. The indicator will become solid red and greed at the same time to show the system cannot be switched off. Please try another PDU if available. 

### **2.2. Indicator is red or off after a period of operation** 

Restart the system in the correct sequence: 

- 1) If successful: 

- a. If events appear on the BYD Max Lite Plus, please refer to Appendix 1 for more details. 

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

Press the LED button three times (each time around one second) within six seconds could reset the Wi-Fi. 

##### **4) Restart the system** 

Restart the system in the correct sequence (refer to Step 4 in **1.2** ). 

##### **5) Replace the WiFi unit** 

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

##### **3) Try again with other laptop or mobile phones.** 

Sometimes the problem comes from the laptop computer or the mobile device itself, try to see if other devices can finish the update. 

##### **4) Replace the PDU** 

If none of the above steps work, please try another PDU if available. 

### **3.3. Changes in SOC** 

##### **1) SOC jumps** 

The SOC of a battery cannot be measured. It is an estimated value. In general, the state of charge (SOC) of a battery is estimated using the voltage, but other factors such as temperature, current flow and charging behavior also play a role. The calculation of the SOC is generally more precise if the battery regularly sees full cycles. It is normal to have a SOC correction/calibration once in a while, e.g. every month. 

##### **2) SOC at commissioning** 

New modules have 30% SOC upon delivery. A new PDU might show a different SOC at the beginning (mostly 30%). However, this is only to be understood as a placeholder value, as a new PDU cannot measure the SOC of modules. As soon as the system starts to run (charge/discharge), the SOC is corrected gradually. The SOC calibration is completed after the latest full cycle. 

8

<!-- pág. 9 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **4. Tools and Methods** 

### **4.1. BYD Max Lite Plus (For Battery-Max Lite)** 

With the BYD Max Lite Plus you can: 

- 1) read the battery information; 

- 2) update firmware; 

- 3) export / download battery logs. 

The BYD Max Lite Plus is constantly being improved and updated. Make sure to use the latest version of the program. 

For the service analysis, please download and provide the data / logs as described in the program instructions. 

##### **Note: You need a Windows computer that can connect to the battery WiFi.** 



9

<!-- pág. 10 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

### **4.2. Faulty module identification** 

#### **4.2.1. Single Module Failure** 

When a module failure occurs, you can view the number of the failed module through BYD Max Lite Plus. 

#### **4.2.2. Communication failure between modules** 

When the BYD Max Lite Plus indicates that a communication failure has occurred between modules, there may be a communication failure in this module or in the module below it. 

Try removing both modules separately to determine the which is fault. If the BYD Max Lite Plus shows that module 1 has a communication failure, it may be caused by PDU or module 1. You can remove module 1 and restart the system to check whether the system can operate normally, if not, please try another PDU. 

#### **4.2.3. Voltage Measurement** 

##### **ATTENTION: High voltage!** 

You can see the max./min. cell voltage in the BYD Max Lite Plus. You can also get the detailed voltage of the modules and cells in the BYD Max Lite Plus or measure it manually according to the below description: 

##### **Measurement of Tower Voltage** 

Disconnect the PDU and measure the tower voltage between the B+ and B- for the entire cabinet. 





**B+ and B- of tower voltage** 

**Measurement of tower voltage** 

10

<!-- pág. 11 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

##### **Measurement of Module Voltage** 

**Note: The nominal voltage for per module is 64.8V~88.8V** 



Individual module measurement 



Multiple Module Measurement 

If the measured voltage of the tower deviates from the nominal value, please check the voltage of the individual modules 

11

<!-- pág. 12 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

#### **4.2.4. Under-voltage** 

A module in which one of the cells has a voltage of <1.5 V is in undercharged (check with BYD Max Lite Plus if possible). 

A LITE module with >64.8 V should be fine and you can continue to check other points according to the service manual. Always make sure the version of firmware is the latest! If the module voltage is <64.8 but the single cell voltage is >1.5 V, the battery needs to be charged as soon as possible. 

If only one module is in under-voltage: remove that module and try to start the system without it (if the number of the remaining modules still meets the requirement of minimum number of modules). Otherwise, make sure to avoid further discharge (e.g., remove PDU) 

If more than one, or all modules are in under-voltage: Contact the service team and make sure to avoid any further discharge of the battery (e.g remove PDU from the system) 

When contacting the service team, make sure to fill the service checklist completely and add the following information: 

- 1) Serial Numbers of the PDU and all (affected) modules; 

- 2) Tower voltage and individual module voltages of all modules (with respect to the Serial Number) 

- 3) Detailed description of how and why the system reached under-voltage if known. Information of when the system was installed and commissioned and in which circumstance and when the under-voltage occurred. If the battery was never running before: Why did it never work before, and what was the status of the battery when the battery was left (on / off / Display). 

- 4) If possible: Logs from the battery using BYD Max Lite Plus showing the cell voltages and Initial Firmware Version of the Battery when under-voltage occurs. 

12

<!-- pág. 13 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

## **Appendix 1 Event and Operation** 

> ⚠ REVISAR TABLA — pág. 13: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|Incorrect<br>module number|Different number of modules in a<br>parallel-connected system|Make sure that the number of modules in a<br>parallel-connected system are the same|
|Cabinet door<br>not closed|Battery cabinet door is open|Check whether the cabinet doors are completely<br>closed. If not, close the doors completely.|
|No.# Module<br>Failures|Failure within the modules|The number in front of ‘#’ represents the<br>number of the faulty module, please replace the<br>faulty module corresponding to the number.|
|No.# Fan Failure|1)Fan Failure of Module<br>2)Fan communication failure<br>3)Abnormal power supply from PDU<br>to fan|<br>1) Check if the cables of the fans are normal. If no,<br>replace the cables. If yes, proceed to the next step<br>2) Check if the fans are faulty. If yes, replace the<br>fans. If no, proceed to the next step.<br>3）If all the fans do not turn on, please check if the<br>AC switch is on.|
||1) Internal CAN communication<br>fault.|1) Check if the terminal resistor is in place|
|Internal<br>communication<br>failure|2) BMU and BMS communication<br>failure<br>3) Communication interface<br>failure<br>4) Address assignment failure|2) For multiple tower systems, check whether the<br>communication cable between towers is faulty. If<br>cables are normal, exchange the PDUs of the<br>master and slave towers and check if the PDUs are<br>faulty.<br>3) For a single tower system, try another PDU if<br>available.|



13

<!-- pág. 14 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 14: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|Communication<br>failure between<br>modules|one or more modules are not<br>recognized|Please refer to**4.2.2**|
|Communication|1) The match test with the Inverter<br>has not started or completed|1) Check if the external connections<br>(Communication cables/Ground cables) are<br>normal.<br>2) Restart in correct order.|
|failure with the<br>inverter|2) Communication cable failure<br>between battery and inverter|3）Re-upgrate the firmware.|
||Wrong type of battery/inverter is<br>set in the BYD Max Lite Plus|4) Measure the CAN output of the PDU with a<br>multimeter, if the output voltage is normal, then<br>troubleshoot the inverter; if the output is 0, then<br>replace the PDU.|
||1) Ground cable not connected|1) Check the ground cable ( ground cable of|
|Insulation<br>failure|2) Ground cable fault<br>3) Module Leakage<br>4) PDU leakage|battery and inverter should be connected<br>separately)<br>2) Restart, if the problem persists, contact BYD<br>service|
||The output voltage of the battery<br>differs from the tower voltage by<br>more than 5V.|1) Check whether the power cable connection is<br>correct|
|Pre-charge<br>failure|1) DC connection faults|(if correct, proceed to the next step; if incorrect,<br>then connect the power cable correctly).|
||2) Inverter DC side short circuit<br>3) PDU main circuit failure|2) Restart, if the problem persists, try another<br>PDU if available.|



14

<!-- pág. 15 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 15: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|||1) Restart|
|Pre-charge not<br>completed|1) Inverter failure that prevents the<br>battery from pre-charging it.<br>2) PDU fault|2) If the problem persists, turn off the battery and<br>disconnect all the power cables from the inverter,<br>black start the battery.<br>a) If the problem persists, replace the PDU;|
|||b) If the problem disappears, check the<br>connection of power cables between the battery<br>and the inverter.|
|||1) Disconnect external electrical connections and<br>restart.|
|Pack V-sensor<br>alarm|Difference between tower voltage<br>and output voltage is more than 5V.|2) If the problem disappears, please check the<br>electrical connections. If problem persists, check if<br>the fuse in the PDU is blown.|
|||3) If the fuse is blown, replace the fuse. If it’s<br>normal, try another PDU if available.|
|Over current<br>occurs in<br>charging/<br>discharging|1) The charging/discharging power<br>is too high and the inverter fails to<br>limit the charging/discharging<br>current in time.<br>2) Unknown reasons|Check whether there is a high-power load starts<br>when this fault occurs. If yes, check whether the<br>load power is within the power range of the<br>inverter:<br>If yes, reduce the loads to ensure that the power<br>is within the range.<br>If not, please contact the service team of the<br>inverter|
|Over/under<br>temperature in<br>charging/discha<br>rging|Unknown reasons|Please contact BYD Service|



15

<!-- pág. 16 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 16: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|Parameter<br>Abnormal|Data loss when loading parameters|Restart,<br>If problem persists, upload battery logs and<br>contact BYD service|
|Current sensor<br>alarm|1) When the SOC is 0% or 100%,<br>there is still discharge/charge<br>current in the system.<br>2) Current value exceeds system<br>limit.|Upload battery logs and contact BYD service|
|DC switch<br>abnormal|Handle switch is off|Restart, if the problem persists, try another PDU if<br>available.|
|Relay abnormal|<sup>Positive or negative relay</sup><br>disconnected|Restart, if the problem persists, try another PDU if<br>available.|
|Memory<br>Abnormal|Memory chip fault|Restart, if the problem persists, try another PDU if<br>available.|
|Chip Function<br>Alarm|Chip running lagging|Restart, if the problem persists, try another PDU if<br>available.|



16

<!-- pág. 17 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 17: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|||For Cause 1|
|||1) Send trained personnel to the site and observe<br>the system for 30 minutes from a safe distance. If<br>there is smoke or fire, remotely power off the<br>system from AC, evacuate the onsite personnel as<br>soon as possible, and contact the fire<br>extinguishing department.|
||1) Smoke or overheating is detected<br>in the battery cabinet|<br>2) If no exception is found during observation,<br>manually clear the alarm by restarting the system.<br>If the alarm persists, contact BYD Service.|
|Fire Alarm|2) A fire has been detected in the<br>battery cabinet.||
||3) System misstatement|For Cause 2|
|||Do not open the cabinet doors. Evacuate the<br>onsite personnel, and contact BYD Service.|
|||For Cause 3|
|||Restart the system, if the fault persists, then<br>contact BYD Service|
||1) Communication cable of the Air|Restart, if the problem persists, try another<br>communication cable.|
|Air Conditioner|Conditioner fails.||
|Alarm|2) Air conditioner failure.|If the problem still persists, please refer to the Air<br>Conditioner Troubleshooting Method<br>（Scan the QR code on the air conditioner to get)|



17

<!-- pág. 18 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 18: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|Air conditioning<br>sensor<br>malfunction|1) Loose sensor or wiring<br>2) Faulty sensor|1) Check whether each temperature sensor is<br>connected loosely and whether the position is<br>correct. If the re-plugging does not work, the<br>sensor is considered damaged and needs to be<br>replaced.|
|||2) If it is not solved, contact BYD service.|
|||1. Confirm that the power cable of the air<br>conditioner is connected correctly.|
|Air conditioner<br>voltage<br>abnormal|1) Unstable voltage<br>2) Cable failure<br>3) Abnormal power supply<br>detection|2. Turn off , measure whether the input voltage<br>exceeds the specified range, if the voltage exceeds<br>the specified range, you need to adjust the<br>voltage; if the voltage is normal, then the next<br>step.<br>3. Replace the control board, restart to confirm if<br>problem persists.|
|||4. If the problem is not resolved with the above<br>steps, contact BYD Service.|
|||1) Check if there are other faults on the display of<br>the Air Conditioner, if so, proceed with other<br>faults first.|
|Air conditioning<br>temperature<br>abnormal|1)Temperature sensor failure<br>2)Condenser blocked|2) Check the value of the temperature sensor in<br>the cabinet (after being stationary for ten<br>minutes) on the display screen of the Air<br>Conditioner to see if it is consistent with the<br>ambient temperature. If it is consistent, the sensor<br>is not faulty. If the temperature deviation is large,<br>check whether the condenser is blocked. If it is<br>blocked, clean the condenser.<br>3) If the fault is not resolved, contact BYD Service.|



18

<!-- pág. 19 -->
Service Manual V 1.0 

Shenzhen BYD Electronic.Co., Ltd. 

> ⚠ REVISAR TABLA — pág. 19: 30% de celdas vacías (posibles celdas combinadas)
|**Events**|**Possible Cause**|**Operation**|
|---|---|---|
|||1. Clean the condenser|
||1. Condenser is blocked|2. Clean the air inlet|
|Air conditioni<br>system<br>abnormal|ng<br>2. Air inlet is blocked<br>3. Ambient temperature is too high|3. If the ambient temperature is too high, add a<br>sunshade|
||4. Blower is abnormal|4. Replace the blower<br>5. If the problem is not resolved with the above<br>steps, contact BYD Service|
|||1. Clean the air inlet/outlet|
|Evaporator<br>abnormal|1. The air inlet/outlet is blocked<br>2. The blower is abnormal|2. Replace the blower<br>3. If the problem is not resolved with the above<br>steps, contact BYD Service.|
|Blower abnorm|al<br>1.The cable of internal/external<br>blower is loose<br>2.Internal/external blower is<br>damaged|1. Check whether the cable of the<br>internal/external blower isnormal<br>2. If the cable is normal, replace the<br>internal/external blower<br>3. If the problem is not resolved with the above|
|||steps, contact BYD Service.|
|||1. Check the cable of compressor|
|Compressor<br>abnormal|1. The cable of compressor is loose<br>2. The condenser is blocked|2. Clean the condenser<br>3. If the problem is not resolved with the above<br>steps, contact BYD Service.|



19
