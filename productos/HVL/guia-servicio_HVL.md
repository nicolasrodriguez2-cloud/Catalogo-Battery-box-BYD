# Battery-Box Premium HVL — Guía de servicio y checklist

- **Producto:** Battery-Box Premium HVL (HVL)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.0 / 2022-01-11
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/2022-01-11_BYD_Battery-Box_Premium_HVL_Service_Guideline_and_Checklist_EN_V1.0-620b63c789472.pdf
- **SHA-256 del PDF:** 3914ed063f256000798421c27e175b07d3cf89e9371e029c7b741a1cf1d7ddfa
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/2022-01-11_BYD_Battery-Box_Premium_HVL_Service_Guideline_and_Checklist_EN_V1.0-620b63c789472.pdf
- **Conversión:** pymupdf4llm 1.28.2, 15 págs.

> ⚠ Este documento tiene 3 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium HVL Service Guideline and Checklist** Version 1.0 

Valid for HVL 12.0 / 16.0 / 20.0 / 24.0 / 28.0 / 32.0 





**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** 

This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com / www.eft-systems.de. Subject to technical modifications; no responsibility</u> is accepted for the accuracy of this information. Attention: High Voltage! Improper handling can cause danger and damage.

<!-- pág. 2 -->
## CONTENT 

|**CONTENT**|**2**|
|---|---|
|**1. GENERAL STEPS**|**3**|
|**2. ERROR ANALYSIS**|**4**|
|2.1 BCU shows no reaction / No LED|4|
|2.2 BCU switch cannot be pulled up / LED remains on|4|
|2.3 Problem with the Firmware Update / App Configuration / Battery WiFi|5|
|2.4 Battery <> inverter communication / no charging or discharging|6|
|2.5 SOC & charging logic|7|
|2.6 Unexpected shutdown|7|
|2.7 Module Extension|7|
|2.8 Be Connect Plus (BCP)|8|
|2.9 LED event code (EC)|9|
|2.10 Voltage measurement and undervoltage|12|
|2.11 Identifying a faulty module / Module exclusion method|13|
|**3. SERVICE TASKS**|**14**|
|3.1 BCU replacement|14|
|3.2 Module Replacement|14|
|**SERVICE CHECKLIST AND CONTACT INFORMATION**|**15**|





2

<!-- pág. 3 -->
## 1. GENERAL STEPS 

**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** Please proceed first with the installation steps by: 

- **No. Name Description** 1 Configuration Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium HVL Compatible Inverter List” available at: **<u>www.bydbatterybox.com</u>** Make sure the inverter is configured correctly. 

- 3 External connections 1. Communication to inverter 2. Not used 3. Dip-Switches 4. Ethernet-Cable for Internet ( **strongly recommended!** ) 5. DC-Ports 6. Grounding 

- 3 Closed Connection The Connection Area must be closed in order to start the system (else the system switch Area will immediately shut off!) 

- 4 Latest Firmware Always install / update the **newest Firmware** ! (also use the latest App Version!) Note: If not stated otherwise, the Wi-Fi password is BYDB-Box 

- 5 App Configuration To complete the commissioning, the configuration of the battery via  “BYD Be Connect” App or “BYD Be Connect Plus” (BCP) Tool for PC is **mandatory** ! 

- 6 Proper Restart NOTE: It is important that the battery is switched on before the inverter! Else, the BCU might not start and not show any reaction (no LED, no WiFi) Defined restart (mind the sequence) 1) Switch off Battery (press power button for 5 seconds)* 2) Turn off DC switch of the inverter 3) Turn off AC switch 5) wait 5 minutes 6) Turn on the battery (switch up) 8) Turn on the AC switch 9) Turn on the DC switch on the inverter *if the battery does not switch off despite pressing the LED for 5 seconds, lift off the BCU to avoid further discharge and contact the service. 

- 7 Checking the correct The system runs properly if: operation - Inverter displays battery SOC correctly - System charges / discharges Note: **If you can not complete the commissioning, then turn off the battery before you leave the site and make sure all LEDs are off. If this is not possible, remove the BCU. Make sure the system will be set into operation quickly.** 



3

<!-- pág. 4 -->
## 2. ERROR ANALYSIS 

### **2.1 BCU shows no reaction / No LED** 

LEDs do not light up, although the system switch is ON. 

> ⚠ REVISAR TABLA — pág. 4: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|8|Module quantity|Check if the module quantity fulfills the minimum requirement (min 3 modules).|
|9|Voltage measurement|See**section 2.10**|
|10|Use correct turn on<br>procedure|NOTE: It is important that the battery is switched onbeforethe inverter!**Else, the**<br>**BCU might not start and not show any reaction (no LED, no WiFi)**|
|||Defined restart (mind the sequence)<br>1) Switch off Battery (press power button for 5 seconds)<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch (inverter should be completely off now!)<br>5) wait 5 minutes<br>6) Turn on the battery (switch up)→LED should light up again<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter|
|11|Only LED off?|Check if there is a wifi access point of the Battery-Box. If so, only the external LED<br>is inactive and a commissioning could still work. In that case make sure that the<br>internal cable of the LED is connected properly.|
|12|BCU exchange|Only if cover is closed and voltage look good: Test another BCU, if available.|



### **2.2 BCU switch cannot be pulled up / LED remains on** 

The system switch switches off immediately (within 5 seconds) / LED remains on eventhough system switch is down 

|**No.**|**Name**|**Description**|
|---|---|---|
|13|Close the cover|Make sure the cover for the connection area on the BCU is properly closed.<br>Important: If the panel is open, the battery won’t turn on (for safety reasons)|
|14|Switch was pulled down<br>by hand|If the switch was pulled down manually, then it cannot be pushed up again within<br>10 minutes. (Please refer to the manual for the correct switch off procedure)|
|15|Solid blue LED?<br>EC102? (1xwhite, 2xblue)|Try to properly shut down the BCU (press the LED power button for more than 5<br>Sec.)<br>- If LED goes off: check the installation and restart the system. (battery first, then<br>inverter, second)<br>- If the LED remains on (solid blue or 2xblue blinking): Remove the BCU from the<br>tower to avoid a deep discharge. Measure the voltage of the system (see**section**<br>**2.10**) and contact your service partner. You can use another BCU, if available.|
|16|BCU exchange|Only if the cover is closed and voltage looks good: Test another BCU, if available.|





4

<!-- pág. 5 -->
### **2.3 Problem with the Firmware Update / App Configuration / Battery WiFi** 

The BCU consists of two components: the BMU and the BMS. The  Firmware Update from the App will update the BMU, which will then update the BMS. **It can take up to 20 Minutes until the firmware is updated on the BMS** . 

|**No**|**Name**|**Description**|
|---|---|---|
|17|Correct App and<br>Firmware|Make sure to have the latest App Version and Battery Firmware (download inside the App)<br>on your mobile device before connecting the app with the battery Wi-Fi.<br>If the App cannot be installed, or other general Problems occur with the App:<br>-<br>try with a different mobile device<br>-<br>Deinstall and reinstall the App<br>-<br>or try with PC Tool BCP (**section 2.8**).<br>-|
|18|WiFi cannot be found /<br>WiFi unstable|The Battery WiFi turns off 5 hours after the start of the Battery. To reactivate the WiFi,<br>press the LED button about 1 second or restart the system.<br>To reset the WiFi, press the LED button three times 1 second within 6 seconds.<br>If problem remains:<br>- remove the lan cable during the configuration. Once the Battery has been configured<br>correctly you can connect it again to the Internet.<br>- check whether other mobile devices are connected the same wifi<br>- try another mobile device|
|19|BMS Version not<br>updated|The App will only update the BMU. The BMU will update the BMS, Once the BMU is<br>updated and the inverter communication is established correctly or right after the<br>configuration is done, the BMS update can take about 20 Minutes<br>If the BMS Version is not updated after 20min with stable inverter communication, follow<br>the below Process:|



1. Update Firmware through the App again 2. Restart the system a. Switch off the Inverter first,  then switch off the battery second (Press LED for 5 seconds) 

b. Wait for 30 Seconds c. Turn on the Battery first, then turn on the inverter second 

3. Wait for 20 Minutes 

4. Check BMS Firmware Version again with App. If Version is still wrong, do the update process again (if possible with another mobile device). 



5

<!-- pág. 6 -->
### **2.4 Battery <> inverter communication / no charging or discharging** 

> ⚠ REVISAR TABLA — pág. 6: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|20|Configuration|Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium<br>HVL Compatible Inverter List”  available at: **www.bydbatterybox.com**<br>Make sure the inverter is configured correctly.|
|21|App Configuration and<br>Firmware|Please check if the App configuration was successful and the Firmware is the<br>most recent one. If there are problems, please refer to**Section 2.3**|
|22|Check DIP Switch|- make sure all dip switches are in the correct position. For most configurations all<br>on the left side. Refer to Manual!|
|23|Communication<br>connection|Does the inverter properly detect the battery? Check if the inverter detects the<br>battery parameters (e.g SOC, battery temperature) correctly. If not, check cabling:<br>- Confirm PIN / Cable Configuration for the specific inverter model<br>- Replace the communication cable (min. CAT5! - better CAT7)<br>- For Fronius & SMA: check the enable signal (necessary for battery activation)<br>Depending on the Inverter model, one or two of the three options of<br>communication ports shown below can be used (refer to the manual!).<br>Please try the other port and communication option if available for the inverter<br>type.|
|24|Grounding|Connect Battery-Box directly to the ground-bus of the house (do not connect over<br>inverter casing or other devices!). Only with a correct grounding of the battery, a<br>trouble-free and secure data transmission can be guaranteed.|
|25|Battery relay closed? /<br>output voltage available?|Once communication has been established between battery and inverter, the BCU<br>is supposed to close the relay. Only then there will be output voltage. Therefore<br>please check if output voltage is there. You can check either by Be Connect App /<br>Be Connect plus tool or by checking if the inverter correctly shows battery voltage.|
|26|Restart the system|Defined restart (mind the sequence)<br>1) Switch off Battery (press power button for 5 seconds)*<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch<br>5) wait 5 minutes<br>6) Turn on the battery (switch up)<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter<br>*Note: if the battery does not switch off despite pressing the LED for 5 seconds,<br>lift off the BCU to avoid further discharge and contact the service.|





6

<!-- pág. 7 -->
### **2.5 SOC & charging logic** 

|**No**|**Name**|**Description**|
|---|---|---|
|27|SOC at commissioning|New HVL modules have 30%SOC upon delivery.  A new BCU might show a different SOC at<br>the beginning (mostly 50% / 30% / 0%). However, this is only to be understood as a<br>placeholder value, as a new BCU cannot measure the SOC of modules. As soon as the<br>system starts to run (charge/discharge) the SOC detection is corrected gradually. The SOC<br>calibration is completed at the latest after a full cycle.|
|28|SOC jumps|The SOC of an LFP battery cannot be measured. It is a calculated value. In general, the<br>state of charge (SOC) of a battery is calculated using the voltage, but other factors such<br>as temperature, current flow and charging behavior also play a role. The calculation of the<br>state of charge is generally more precise if the battery regularly sees full cycles. Every now<br>and then an SOC correction / calibration might occur. That is normal.|



### **2.6 Unexpected shutdown** 

System has been successfully commissioned in the past and did run for some time. Later on an unexpected shutdown occured. 

|**No**|**Name**|**Description**|
|---|---|---|
|29|Inverter<br>Communication|The battery only works with an compatible external inverter. If for whatever reason the<br>communication between battery and inverter is lost, the battery will shut down itself within<br>30minutes. Therefore, check which one did shut down first (battery or inverter) and check<br>if inverter is properly detecting battery (e.g showing correct SOC or temperature). If<br>communication problem remains, check according to**section 2.4**.|
|30|Battery Logs / History<br>Data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log files in order to identify the<br>root cause.  See**section 2.8**for details.|
|31|Inverter Warning &<br>Monitoring|Unexpected Shutdown can be caused by overall system settings. Therefore, it is necessary<br>to evaluate inverter data as well.<br>-<br>Which error message are shown in inverter portal?<br>-<br>Please provide access to Inverter portal (add info@eft-systems.de and tell us<br>the name of the system in the portal)|



### **2.7 Module Extension** 

|**No**|**Name**|**Description**|
|---|---|---|
|32|Extension|Note: It is important that all modules of a storage tower have a similar state of charge<br>(tolerance 5%). New modules have about 30%. Therefore, please only add the new module<br>to the battery when the state of charge (SOC) is between 25% and 35% charge. Don't forget<br>to adjust the number of modules in the configuration if it is necessary.|
|||If the 30% SOC rule has not been followed, temporary capacity loss and SOC jumps might<br>occur. In this case a charger may be required to align the module SOCs. Contact your local<br>service provider.|





7

<!-- pág. 8 -->
### **2.8 Be Connect Plus (BCP)** 

Be Connect Plus is a PC tool. With Be Connect Plus (BCP) you can: 

- read the battery information, 

- configure the battery system 

- update BMU & BMS firmware 

- Export / download battery logs 

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the Tool on www.bydbatterybox.com / www.eft-systems.de** 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual included). 

Note: You need a computer with Windows that will be connected to the battery WiFi. Login as Installer to Be Connect Plus, the password is the same as for the WiFi: BYDB-Box 





8

<!-- pág. 9 -->
### **2.9 LED event code (EC)** 

A constant white LED refers to the standby mode. White blinking LED means charge or discharge. 

When the battery is initiating, the LED will flash white and blue with an interval time of 0.5 seconds (normal during startup). When the LED flashes blue with an interval time of 1 second it indicates an event code.  Please start to count when the white LED begins to flash, then count how many times white and blue LED flashes. (also refer to the manual!) Examples: 

1xwhite, 3xblue → EC 103 

1xwhite, 11xblue → EC 111 

3xwhite, 3xblue → EC 303 

Most Errors are caused by faulty communication, incorrect app configuration or missing restart after the app or BCP configuration. Please go in detail through: **Section 2.3 & 2.4** 

##### **Note: if the battery is not correctly configured with the app, the event code (EC) might be misleading.** 

|**Event Code**<br>**(EC)**|**Measure**|
|---|---|
|EC 102|Abnormal shutdown (open panel) / PreCharge failure / DC reverse connection.|
||- Check the DC-cable connection to the battery, inverter and combiner box (if there is any).<br>- Make sure the cover for the connection area on the BCU is properly closed.<br>Important: If the panel is open, the battery won’t turn on (for safety reasons)<br>-  Try to properly shut down the BCU (press for 5 seconds the LED power button)<br>If LED goes off: check installation and restart (battery first, then inverter second).<br>If LED remains on (solid blue or 2xblue blinking): Remove the BCU from the tower to avoid a<br>deep discharge. Measure the voltage of the system (see**section 2.10**) and contact your<br>service partner.|
||If problem remains:<br>-<br>Test another BCU, if available.|
|EC 103|Voltage Sensor Failure / BMU<>BMS communication failure.<br>- make sure all dip switches are in the correct position. For most configurations all on the left<br>side. Refer to Manual!<br>- Remove the topmost module and check whether the event code disappears. Note: A module<br>with communication problems often works without restrictions at the lowest module position,<br>since no communication with the base is necessary.|
||If problem remains:<br>-<br>Test another BCU, if available.|
|EC 104|Faulty temperature sensor.<br>- Check via BCP to identify the root cause module. Alternatively, follow “Module exclusion<br>method” (see**Section 2.11**).|
|EC 105|PackVoltage Sensor Failure.<br>- Check DC-cable connection on battery, inverter and combiner box (if there is any).<br>- Restart system properly (see**step 6, section 1**)<br>If problem remains:<br>-<br>Test another BCU, if available.|





9

<!-- pág. 10 -->
|EC 203<br>EC 303|Incorrect module quantity / Module not detected.|
|---|---|
|EC 403<br>EC 503<br>EC 603<br>EC 703<br>EC 803|- Make sure app-configuration has been completed correctly (especially module type and<br>quantity!).<br>- EC 203 to EC 803 means that a module is not recognized. The first number (= number of<br>white flashes) indicates which module is probably affected. This module, or the module above<br>it, can be responsible for the event code.<br>Example: EC 203 = second module from the top / EC 403 = fourth-top module.<br>- Remove the affected module and check whether the event code disappears. If not, check the<br>module above.<br>- Rearrange the modules in the tower.<br>Note: A module with communication problems often works without restrictions at the lowest<br>module position, since no communication with the base is necessary.|
|EC 106|Current Sensor Failure.<br>- Make sure that the latest firmware is installed and that the battery has been properly<br>restarted.<br>If the problem remains:<br>-<br>Test another BCU if available.|
|EC 107|Undervoltage.<br>- Shut down the system quickly to avoid further discharge. Check whether the system can shut<br>down normally (by pressing the LED button for 5s).<br>- If the system cannot shut down normally, lift the BCU<br>- Follow**section 2.10**(Voltage measurement and undervoltage instruction)|
|EC 108|PreCharge Fault.<br>- Check DC-cable connection on battery, inverter and combiner box (if there is any).<br>- Restart system according to manual. (note: to properly shut down you need to press the LED<br>button for 5 seconds. Make sure to start the battery before starting the inverter!)<br>If problem remains:<br>-<br>Test another BCU, if available.|
|EC 109|Make sure that the latest firmware is installed and that the battery has been properly restarted.<br>If the problem remains: it is Probably caused by a module. Follow the “Module exclusion<br>method” (see**Section 2.11**).|
|EC 110|Low voltage.<br>The system needs to charge very soon and should not be further discharged!<br>1. Shut down the system quickly to avoid further discharge. Check whether the system can<br>shut down normally (by pressing the LED button for 5s).<br>- If the system cannot shut down normally, lift the BCU<br>- Follow**section 2.10**(Voltage measurement and undervoltage)<br>2. Avoid further discharge of the battery, by searching the problem while the battery is<br>completely off / BCU is lifted.<br>- Check the other steps in the service guideline and also check the inverter (latest FW /<br>correct/defined restart?) and with the inverter service, why the force charge doesn’t work<br>(e.g. any fault at the inverter). Do not turn on the battery before making sure the inverter<br>should be able to charge the battery.<br>3. If everything has been checked and the system cannot be charged, make sure to avoid<br>further discharge (e.g remove BCU) and contact the service.|





10

<!-- pág. 11 -->
EC 111 Normal when the battery has just started. LED will turn to solid white when: - inverter communication works (--> Check inverter communication, **Section 2.4** ) - right after saving / redoing the configuration (Be Connect: go through whole wizard // Be Connect Plus: resave the configuration by using the “Setup” button and restart tool to refresh) Please also make sure all dip switches are in the correct position. For most configurations all on the left side. Refer to Manual! If EC111 remains even after the inverter detects battery and even after redoing app configuration: Remove the topmost module and check whether the event code disappears. If not, test another BCU if available. EC 112 No communication with inverter. Check inverter communication ( **Section 2.4** ) 



11

<!-- pág. 12 -->
### **2.10 Voltage measurement and undervoltage** 

#### **ATTENTION: High voltage!** 

**You can see the max. and min. cell voltage in the BeConnect App. You can also get the detailed module and cell voltage in the BCP Program (section 2.8) or measure it manually according to the below description:** 

#### **Measurement of Tower Voltage** 

Take down the BCU and measure the tower voltage on the topmost module as shown below. Note: The nominal voltage should be module quantity times 50V (for HVL). 



If the measured voltage deviates significantly from the nominal value, please check the electrical voltage at the individual modules, as shown in the following section. 

#### **Measurement of Individual Module Voltage** 

**Positive** 

**Negative Measurement:** 









12

<!-- pág. 13 -->
#### **Undervoltage** 

A HVL Module in which one of the 16 cells  cells has a voltage of <1.5 V is in undervoltage (check with BCP [ **section 2.8** ] / BC if possible). 

HVL Modules with >45 V should be fine and you can continue to check other points according to this service guideline. Always **make sure the firmware is the latest!** If the HVL module voltage <45V () but the single cell voltage is >1.5V, the battery needs to be charged quickly - follow the instructions of EC110 in **section 2.9** 

- If only one module is in undervoltage: remove that one and try to start the system without it (if the remaining modules still comply with the Compatible Inverter List). Otherwise, make sure to avoid further discharge (e.g. remove BCU) 

- If one, or all modules are in undervoltage: Contact the service as stated below and make sure to avoid any further discharge of the battery (e.g remove BCU from the system) 

When contacting the service, make sure to fill the service checklist completely and add the following information: 

- Serial Numbers (of the BCU and all (affected) modules) 

- Tower voltage and individual module voltages of all modules (related to Serialnumber) 

- What was the status of the system switch on the BCU when the undervoltage (UV) happened? (tripped or not) 

- If possible: Logs from the battery using BCP ( **section 2.8** ) and Screenshots showing the cell voltages 

- Initial Firmware (FW) Version of the Battery when the UV happened (BMU and BMS) 

- Inform if the BCU could shut down normally by pressing the LED button (note: if you have updated the FW after UV, write down here whether the battery could be switched off manually before the FW update.) 

- Detailed description how and why the system reached Undervoltage if known. Information when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the battery's status when the battery was left (on / off / LED). 

- Inverter Model, Serial Number and inverter logs. 

- Access to the inverter portal (add USservice@eft-systems.de and tell us the name of the system in the portal) 

### **2.11 Identifying a faulty module / Module exclusion method** 

#### **The module quantity must be adjusted in the app whenever the number of modules is changed!** 

**1.** Build the Battery-Box with the minimum available number of Modules (HVL:3 modules). 

**2. Check System. If Okay** , add one module at a time, adjust the module number in the app and check again. 



**3. If not okay** : The faulty module is probably one of the modules in the tower. Take one of the spare modules and exchange each of the remaining modules with the spare module one at a time. Check the battery status after each step. If battery status turns to “OK”, the faulty module is the one that was exchanged. 





13

<!-- pág. 14 -->
## 3. SERVICE TASKS 

Please go through the general steps beforehand, see chapter 1. 

### **3.1 BCU replacement** 

**Have you detected a faulty BCU?:** 

After replacing the BCU, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.2 Module Replacement** 

#### **Have you detected a faulty module?:** 

In the meantime you can use the battery system with the remaining modules and a correspondingly reduced capacity (take into account the minimum number of modules). 

Please note: It is important that all modules of a battery tower have a similar state of charge (SOC) with a tolerance of 5%. New modules have about **30** % SOC. If the remaining modules have not yet been put into operation (not charged / discharged), the new module can easily be added. Otherwise, it is basically a module extension. In this case, please add the new module to the system only when the system has a SOC between 25% and 35% (see extension process in the manual). Make sure to configure correctly after any change in module number. 





14

<!-- pág. 15 -->
|**BYD Battery-Box Premium HVL Service Checklist - V1.1 US**|
|---|



> ⚠ REVISAR TABLA — pág. 15: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Bo<br>allowed by professional and qualified electricians. Improper handling can cause danger and damage. This docum<br>not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the informa<br>.|x are only<br>i          ent does<br>fi              tion.|
|---|---|
|**1.**<br>**GENERAL STEPS**<br>i|i|
|i<br>Please carefully check**all**„General Steps“ from page 3 of the Service Guideline and confirm this in the|i    boxes below|
|1.1 Configuration<br>1.4 Latest Firmware<br>1.7 C|orrect Operation|
|1.2 External Connections<br>1.5 App Configuration||
|1.3 Closed Connection Area<br>1.6 Proper Restart||
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the**error related**Analysis from Chapter 2 (page 4-10) of the Service Guideline that you c<br>all the information related to those Sections|hecked, and collect|
|2.1 BCU shows no reaction / No LED<br>2.5 SOC & charging logic|2.9 LED event code (EC)|
|2.2 BCU switch cannot be pulled up / LED remains on<br>2.6 Unexpected shutdown|2.10 Voltage measurement and<br>dl|
|2.3 Problem with the FW Update / App Configuration / WiFi<br>2.7 Module Extension|unervotage<br>|
|2.4 Battery <> inverter communication / no charging or discharging<br>2.8 Be Connect Plus (BCP)|2.11 Identifying a faulty module<br>/ Module exclusion method|
|**3.**<br>**SERVICE INFORMATION**||
|Please fill all available information in below table. Some information like the Serial Number of the BCU|i                is mandatory to receive service.|
|**•**<br>**Service Ticket Number or System ID:**||
|**•**<br>**Installer / Delivery Address / Contact:**||
|Company<br>ZIP / City||
|Contact Person<br>Phone||
|Street / Nr.<br>Email||
|**•**<br>**System Information**||
|Battery Configuration (HVL..)<br>BMU Firmware||
|BCU Serial Number<br>BMS Firmware||
|BCU Connected to Internet<br>Inverter Firmware<br>Yes<br>No||
|Inverter Brand + Model<br>System Name on<br>Inverter Portal||
|Inverter Serial Number<br> <br>( Provide access )||
|Commissioning Date||
|**•**<br>**Service Information**||
|BCU EventCode (EC)<br>Inverter Error Code||
|Was the battery charging / discharging before (was the system working normally before?)|Yes<br>No|
|Take pictures of open communication port in the BCU and Inverter clearly showing connection cables||
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see chapter 2.8)||
|Description of<br>the Problem<br>Please provide any additional information that is necessary or could help in the analysis of the service c<br>wrong module, video of a special behaviour; pictures; app screenshots; module voltages... )<br>By contacting us you confirm, that a qualified person has done the necessary control and collected all available in|ase (e.g. serial number of a<br>i   i           formation above.|
|Service Contact:<br>EFT US<br>||
|www.eft-systems.de<br>USservice@eft-systems.de<br>+1 83333 88721||
