# Battery-Box Premium HVS/HVM — Guía de servicio y checklist

- **Producto:** Battery-Box Premium HVS/HVM (HVS&HVM)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.5 / 2022-01-11
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/2022-01-11_BYD_Battery-Box_Premium_HVS_HVM_Service_Guideline_and_Checklist_EN_V1.5-620b5f836f34c.pdf
- **SHA-256 del PDF:** 42e37c394578eb9e61b5a88bb51f7283c4cda87c6b985a08ddf50bb3635acd89
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/2022-01-11_BYD_Battery-Box_Premium_HVS_HVM_Service_Guideline_and_Checklist_EN_V1.5-620b5f836f34c.pdf
- **Conversión:** pymupdf4llm 1.28.2, 16 págs.

> ⚠ Este documento tiene 5 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium HVS/HVM Service Guideline and Checklist** Version 1.5 

Valid for HVS 5.1 / 7.7 / 10.2 / 12.8 HVM 8.3 / 11.0 / 13.8 / 16.6 / 19.3 / 22.1 







**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** 

This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com</u> / <u>www.eft-systems.de</u> / <u>www.alpspower.com.au.</u> Subject to technical modifications; no responsibility is accepted for the accuracy of this information. Attention: High Voltage! Improper handling can cause danger and damage.

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
|2.7 Module Extension / Parallel connection|8|
|2.8 Be Connect Plus (BCP)|9|
|2.9 LED event code (EC)|10|
|2.10 Voltage measurement and undervoltage|13|
|2.11 Identifying a faulty module / Module exclusion method|14|
|**3. SERVICE TASKS**|**15**|
|3.1 BCU replacement|15|
|3.2 Module Replacement|15|
|**SERVICE CHECKLIST AND CONTACT INFORMATION**|**16**|





2

<!-- pág. 3 -->
## 1. GENERAL STEPS 

**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** Please proceed first with the installation steps by: 

- **No. Name Description** 1 Configuration Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium HVS & HVM Compatible Inverter List” (V1.8 or above) available at: **<u>www.bydbatterybox.com</u>** Make sure the inverter is configured correctly. 

- 2 Only HVS or HVM Do not mix up HVS-modules  (“I”) with HVM-modules (“II”). 3 External connections 



1. Communication to inverter 2. Ports for parallel connection 3. Dip-Switches 4. Ethernet-Cable for Internet ( **strongly recommended!** ) 5. DC-Ports 6. Grounding 

4 Closed Connection The Connection Area must be closed in order to start the system (else the system switch Area will immediately shut off!) 

5 Latest Firmware Always install / update the **newest Firmware** ! (also use the latest App Version!) Note: If not stated otherwise, the Wi-Fi password is BYDB-Box 

6 App Configuration To complete the commissioning, the configuration of the battery via  “BYD Be Connect” App or “BYD Be Connect Plus” (BCP) Tool for PC is **mandatory** ! 

7 Proper Restart NOTE: It is important that the battery is switched on before the inverter! Else, the BCU might not start and not show any reaction (no LED, no WiFi) Defined restart (mind the sequence) 1) Switch off Battery (press power button for 5 seconds)* 2) Turn off DC switch of the inverter 3) Turn off AC switch 4) Kostal only: Pull out the PV strings from inverter 5) wait 10 minutes 6) Turn on the battery (switch up) 7) Kostal only: Connect PV strings back to inverter 8) Turn on the AC switch 9) Turn on the DC switch on the inverter *if the battery does not switch off despite pressing the LED for 5 seconds, lift off the BCU to avoid further discharge and contact the service. 

8 Checking the correct The system runs properly if: operation - Inverter displays battery SOC correctly - System charges / discharges Note: **If you can not complete the commissioning, then turn off the battery before you leave the site and make sure all LEDs are off. If this is not possible, remove the BCU. Make sure the system will be set into operation quickly.** 

*if the battery does not switch off despite pressing the LED for 5 seconds, lift off the BCU to avoid further discharge and contact the service. 



3

<!-- pág. 4 -->
## 2. ERROR ANALYSIS 

### **2.1 BCU shows no reaction / No LED** 

LEDs do not light up, although the system switch is ON. 

> ⚠ REVISAR TABLA — pág. 4: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|9|Module quantity|Check if the module quantity fulfills the minimum requirement (HVS: 2, HVM: 3<br>modules) and check the “Compatible Inverter List” for inverter requirements.|
|10|Voltage measurement|See**section 2.10**|
|11|Use correct turn on<br>procedure|NOTE: It is important that the battery is switched onbeforethe inverter!**Else, the**<br>**BCU might not start and not show any reaction (no LED, no WiFi). See following:**|
|||1) Switch off Battery (press power button for 5 seconds)<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch<br>4) Kostal only: Pull out the PV strings from inverter<br>5) wait 10 minutes (inverter should be completely off now!)<br>6) Turn on the battery (switch up)→LED should light up again<br>7) Kostal only: Connect PV strings back to inverter<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter|
|12|Only LED off?|Check if there is a wifi access point of the Battery-Box. If so, only the external LED<br>is inactive and a commissioning could still work. In that case make sure that the<br>internal cable of the LED is connected properly.|
|13|BCU exchange|Only if cover is closed and voltage look good:<br>Test another BCU, if available.|



### **2.2 BCU switch cannot be pulled up / LED remains on** 

The system switch switches off immediately (within 5 seconds) / LED remains on eventhough system switch is down 

|**No.**|**Name**|**Description**|
|---|---|---|
|14|Close the cover|Make sure the cover for the connection area on the BCU is properly closed.<br>Important: If the panel is open, the battery won’t turn on (for safety reasons)|
|15|Switch was pulled down<br>by hand|If the switch was pulled down manually, then it cannot be pushed up again within<br>10 minutes. (Please refer to the manual for the correct switch off procedure)|
|16|Solid blue LED?<br>EC102? (1xwhite, 2xblue)|Try to properly shut down the BCU (press the LED power button for more than 5<br>Sec.)<br>- If LED goes off: check the installation and restart the system. (battery first, then<br>inverter, second)<br>- If the LED remains on (solid blue or 2xblue blinking): Remove the BCU from the<br>tower to avoid a deep discharge. Measure the voltage of the system (see**section**<br>**2.10**) and contact your service partner. You can use another BCU, if available.|
|17|BCU exchange|Only if the cover is closed and voltage looks good:<br>Test another BCU, if available.|





4

<!-- pág. 5 -->
### **2.3 Problem with the Firmware Update / App Configuration / Battery WiFi** 

The BCU consists of two components: the BMU and the BMS. The  Firmware Update from the App will update the BMU, which will then update the BMS. **The BMS will only be updated once there is communication between the battery and the inverter or just after the App configuration. It can take up to 20 Minutes until the firmware is updated on the BMS** . 

> ⚠ REVISAR TABLA — pág. 5: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No**|**Name**|**Descript**|**ion**|
|---|---|---|---|
|18|Correct App and<br>Firmware|Make su<br>the App)<br>If the Ap<br>-<br>-<br>-|re to have the latest App Version (>1.7.4) and Battery Firmware (download inside<br>on your mobile device before connecting the app with the battery Wi-Fi.<br>p cannot be installed, or other general Problems occur with the App:<br>try with a different mobile device<br>Deinstall and reinstall the App<br>or try with PC Tool BCP (**section 2.8**).|
|19|WiFi cannot be found /<br>WiFi unstable|The Batt<br>press th<br>To reset<br>If proble<br>- remove      i      i<br>correctly<br>- check         i<br>- try anot|ery WiFi turns off 5 hours after the start of the Battery. To reactivate the WiFi,<br>e LED button about 1 second or restart the system.<br>the WiFi, press the LED button three times 1 second within 6 seconds.<br>m remains:<br>the lan cable during the configuration. Once the Battery has been configured<br>you can connect it again to the Internet.<br>whether other mobile devices are connected the same wifi<br>her mobile device|
|20|BMS Version not<br>updated|The App<br>updated<br>configur<br>If the BM<br>the belo|will only update the BMU. The BMU will update the BMS, Once the BMU is<br>and the inverter communication is established correctly or right after the<br>iation is done, the BMS update can take about 20 Minutes<br>S Version is not updated after 20min with stable inverter communication, follow<br>w Process:|
|||1.<br>2.<br>3.<br>4.|Update Firmware through the App again<br>Restart the system<br>a.<br>Switch off the Inverter first,  then switch off the battery second (Press<br>LED for 5 seconds)<br>b.<br>Wait for 30 Seconds<br>c.<br>Turn on the Battery first, then turn on the inverter second<br>Wait for 20 Minutes<br>Check BMS Firmware Version again with App. If Version is still wrong, do the<br>update process again (if possible with another mobile device).|





5

<!-- pág. 6 -->
### **2.4 Battery <> inverter communication / no charging or discharging** 

> ⚠ REVISAR TABLA — pág. 6: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|21|Configuration|Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium<br>HVS & HVM Compatible Inverter List” (V2.2 or above) available at:<br>**www.bydbatterybox.com**<br>Make sure the inverter is configured correctly.|
|22|**App Configuration and**<br>**Firmware**|Please check if the App configuration was successful and the Firmware is the<br>most recent one. If there are problems, please refer to**Section 2.3**|
|23|Check DIP Switch|If only one tower, or two towers parallel connected, all DIP switches should be in<br>position: LEFT  (except for Kostal PIKO MP plus - refer to manual)<br>If 3 towers HVS/HVM are in parallel connection, see manual for DIP configuration|
|24|Communication<br>connection|Does the inverter properly detect the battery? Check if the inverter detects the<br>battery parameters (e.g SOC, battery temperature) correctly. If not, check cabling:<br>- Confirm PIN / Cable Configuration for the specific inverter model<br>- Replace the communication cable (min. CAT5! - better CAT7)<br>- For Fronius & SMA: check the enable signal (necessary for battery activation)<br>Depending on the Inverter model, one or two of the three options of<br>communication ports shown below can be used (refer to the manual!).<br>Please try the other port and communication option if available for the inverter<br>type.|
|25|Grounding|Connect Battery-Box directly to the ground-bus of the house (do not connect over<br>inverter casing or other devices!). Only with a correct grounding of the battery, a<br>trouble-free and secure data transmission can be guaranteed.|
|26|Battery relay closed? /<br>output voltage available?|Once communication has been established between battery and inverter, the BCU<br>is supposed to close the relay. Only then there will be output voltage. Therefore<br>please check if output voltage is there. You can check either by Be Connect App /<br>Be Connect plus tool or by checking if the inverter correctly shows battery voltage.|
|27|Restart the system|Defined restart (mind the sequence)<br>1) Switch off Battery (press power button for 5 seconds)*<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch<br>4) Kostal only: Pull out the PV strings from inverter<br>5) wait 10 minutes<br>6) Turn on the battery (switch up)<br>7) Kostal only: Connect PV strings back to inverter<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter<br>*Note: if the battery does not switch off despite pressing the LED for 5 seconds,<br>lift off the BCU to avoid further discharge and contact the service.|





6

<!-- pág. 7 -->
### **2.5 SOC & charging logic** 

|**No**|**Name**|**Description**|
|---|---|---|
|28|SOC at commissioning|New HVS / HVM modules have 30%SOC upon delivery.  A new BCU might show a different<br>SOC at the beginning (mostly 50% / 30% / 0%). However, this is only to be understood as a<br>placeholder value, as a new BCU cannot measure the SOC of modules. As soon as the<br>system starts to run (charge/discharge) the SOC detection is corrected gradually. The SOC<br>calibration is completed at the latest after a full cycle.|
|29|SOC jumps|The SOC of an LFP battery cannot be measured. It is a calculated value. In general, the<br>state of charge (SOC) of a battery is calculated using the voltage, but other factors such<br>as temperature, current flow and charging behavior also play a role. The calculation of the<br>state of charge is generally more precise if the battery regularly sees full cycles. Every now<br>and then an SOC correction / calibration might occur. That is normal.|



### **2.6 Unexpected shutdown** 

System has been successfully commissioned in the past and did run for some time. Later on an unexpected shutdown occured. 

> ⚠ REVISAR TABLA — pág. 7: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No**|**Name**|**Description**|
|---|---|---|
|30|Inverter<br>Communication|The battery only works with an compatible external inverter. If for whatever reason the<br>communication between battery and inverter is lost, the battery will shut down itself within<br>30minutes. Therefore, check which one did shut down first (battery or inverter) and check<br>if inverter is properly detecting battery (e.g showing correct SOC or temperature). If<br>communication problem remains, check according to**section 2.4**.|
|31|Battery Logs / History<br>Data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log files in order to identify the<br>root cause.  See**section 2.8**for details.|
|32|Inverter Warning &<br>Monitoring|Unexpected Shutdown can be caused by overall system settings. Therefore, it is necessary<br>to evaluate inverter data as well.<br>-<br>Which error message are shown in inverter (portal?<br>-<br>Please provide access to Inverter portal (add info@eft-systems.de and tell us<br>the name of the system in the portal)|





7

<!-- pág. 8 -->
### **2.7 Module Extension / Parallel connection** 

|**No**|**Name**|**Description**|
|---|---|---|
|33|Extension|Note: It is important that all modules of a storage tower have a similar state of charge<br>(tolerance 5%). New modules have about 30%. Therefore, please only add the new module<br>to the battery when the state of charge (SOC) is between 25% and 35% charge. Don't forget<br>to adjust the number of modules in the configuration if it is necessary.<br>If the 30% SOC rule has not been followed, temporary capacity loss and SOC jumps might<br>occur. In this case a charger may be required to align the module SOCs. Contact your local<br>service provider.|
|34|Parallel connection|Cabling / installation (including parallel connection) is described in the short installation<br>guide. Some notes:<br>-<br>DC bus bar needed to collect DC cables. There is a matching DC combiner box<br>from BYD for the HVS / HVM. Details in the corresponding data sheet and<br>manual of the BYD combiner box.<br>-<br>Towers need to be the same type (module type & quantity)<br>-<br>Communication established via master/slave. Only master unit needs to be<br>configured and updated. No configuration of the slave BCUs necessary<br>-<br>Check DIP switches: If only one tower, or two towers parallel connected, all DIP<br>switches should be in position: LEFT (except for Kostal PIKO MP plus - refer to<br>manual). If 3 towers HVS/HVM are in parallel connection, see manual for DIP<br>configuration|





- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 





8

<!-- pág. 9 -->
### **2.8 Be Connect Plus (BCP)** 

Be Connect Plus is a PC tool. With Be Connect Plus (BCP) you can: 

- read the battery information, 

- configure the battery system 

- update BMU & BMS firmware 

- Export / download battery logs 

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the Tool on www.bydbatterybox.com / www.eft-systems.de / www.alpspower.com.au** . 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual included). 

Note: You need a computer with Windows that will be connected to the battery WiFi. Login as Installer to Be Connect Plus, the password is the same as for the WiFi: BYDB-Box 





9

<!-- pág. 10 -->
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
|EC 103|Voltage Sensor Failure / BMU<>BMS communication failure.<br>- make sure all dip switches are in the correct position. For most configurations all on the left<br>side (exception e.g. parallel connection of 3 towers and/or Kostal Piko MP). Refer to Manual!<br>- Remove the topmost module and check whether the event code disappears. Note: A module<br>with communication problems often works without restrictions at the lowest module position,<br>since no communication with the base is necessary.|
||If problem remains:<br>-<br>Test another BCU, if available.|
|EC 104|Faulty temperature sensor.<br>- Check via BCP to identify the root cause module. Alternatively, follow “Module exclusion<br>method” (see**Section 2.11**).|
|EC 105|PackVoltage Sensor Failure.<br>- Check DC-cable connection on battery, inverter and combiner box (if there is any).<br>- Restart system properly (see**step 7, section 1**)<br>If problem remains:<br>-<br>Test another BCU, if available.|





10

<!-- pág. 11 -->
|EC 203<br>EC 303|Incorrect module quantity / Module not detected.|
|---|---|
|EC 403<br>EC 503<br>EC 603<br>EC 703<br>EC 803|- Make sure app-configuration has been completed correctly (especially module type and<br>quantity!).<br>- EC 203 to EC 803 means that a module is not recognized. The first number (= number of<br>white flashes) indicates which module is probably affected. This module, or the module above<br>it, can be responsible for the event code.<br>Example: EC 203 = second module from the top / EC 403 = fourth-top module.<br>- Remove the affected module and check whether the event code disappears. If not, check the<br>module above.<br>- Rearrange the modules in the tower.<br>Note: A module with communication problems often works without restrictions at the lowest<br>module position, since no communication with the base is necessary.|
|EC 106|Current Sensor Failure.<br>- Make sure that the latest firmware is installed and that the battery has been properly<br>restarted.<br>If the problem remains:<br>-<br>Test another BCU if available.|
|EC 107|Undervoltage.<br>- Shut down the system quickly to avoid further discharge. Check whether the system can shut<br>down normally (by pressing the LED button for 5s).<br>- If the system cannot shut down normally, lift the BCU<br>- Follow**section 2.10**(Voltage measurement and undervoltage instruction)|
|EC 108|PreCharge Fault.<br>- Check DC-cable connection on battery, inverter and combiner box (if there is any).<br>- Restart system according to manual. (note: to properly shut down you need to press the LED<br>button for 5 seconds. Make sure to start the battery before starting the inverter!)<br>If problem remains:<br>-<br>Test another BCU, if available.|
|EC 109|Make sure that the latest firmware is installed and that the battery has been properly restarted.<br>If the problem remains: it is Probably caused by a module. Follow the “Module exclusion<br>method” (see**Section 2.11**).|
|EC 110|Low voltage.<br>The system needs to charge very soon and should not be further discharged!<br>1. Shut down the system quickly to avoid further discharge. Check whether the system can<br>shut down normally (by pressing the LED button for 5s).<br>- If the system cannot shut down normally, lift the BCU<br>- Follow**section 2.10**(Voltage measurement and undervoltage)<br>2. Avoid further discharge of the battery, by searching the problem while the battery is<br>completely off / BCU is lifted.<br>- Check the other steps in the service guideline and also check the inverter (latest FW /<br>correct/defined restart?) and with the inverter service, why the force charge doesn’t work<br>(e.g. any fault at the inverter). Do not turn on the battery before making sure the inverter<br>should be able to charge the battery.<br>3. If everything has been checked and the system cannot be charged, make sure to avoid<br>further discharge (e.g remove BCU) and contact the service.|





11

<!-- pág. 12 -->
EC 111 Normal when the battery has just started. LED will turn to solid white when: - inverter communication works (--> Check inverter communication, **Section 2.4** ) - right after saving / redoing the configuration (Be Connect: go through whole wizard // Be Connect Plus: resave the configuration by using the “Setup” button and restart tool to refresh) Please also make sure all dip switches are in the correct position. For most configurations all on the left side (exception e.g. parallel connection of 3 towers and/or Kostal Piko MP). Refer to Manual! If EC111 remains even after the inverter detects battery and even after redoing app configuration: Remove the topmost module and check whether the event code disappears. If not, test another BCU if available. EC 112 No communication with inverter. Check inverter communication ( **Section 2.4** ) 



12

<!-- pág. 13 -->
### **2.10 Voltage measurement and undervoltage** 

#### **ATTENTION: High voltage!** 

**You can see the max. and min. cell voltage in the BeConnect App. You can also get the detailed module and cell voltage in the BCP Program (section 2.8) or measure it manually according to the below description:** 

#### **Measurement of Tower Voltage** 

Take down the BCU and measure the tower voltage on the topmost module as shown below. Note: The nominal voltage should be module quantity times 100V (for HVS) or module quantity times 50V (for HVM). 



If the measured voltage deviates significantly from the nominal value, please check the electrical voltage at the individual modules, as shown in the following section. 

#### **Measurement of Individual Module Voltage** 

**Positive** 

**Negative** 

**Measurement:** 









13

<!-- pág. 14 -->
#### **Undervoltage** 

A Module in which one of the 32 (HVS) / 16 (HVM) cells has a voltage of <1.5 V is in undervoltage (check with BCP [section 2.8] / BC if possible). 

Modules HVS with >90 V and HVM with >45 V should be fine and you can continue to check other points according to this service guideline. Always **make sure the firmware is the latest!** If the module voltage is <90V (HVS) / <45V (HVM) but the single cell voltage is >1.5V, the battery needs to be charged quickly - follow the instructions of EC110 in **section 2.9** 

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

- Access to the inverter portal (add info@eft-systems.de and tell us the name of the system in the portal) 

### **2.11 Identifying a faulty module / Module exclusion method** 

#### **The module quantity must be adjusted in the app whenever the number of modules is changed!** 

**1.** Build the Battery-Box with the minimum available number of Modules (HVS: 2 modules, HVM: 3 modules). 

**2. Check System. If Okay** , add one module at a time, adjust the module number in the app and check again. 



**3. If not okay** : The faulty module is probably one of the modules in the tower. Take one of the spare modules and exchange each of the remaining modules with the spare module one at a time. Check the battery status after each step. If battery status turns to “OK”, the faulty module is the one that was exchanged. 





14

<!-- pág. 15 -->
## 3. SERVICE TASKS 

Please go through the general steps beforehand, see chapter 1. 

### **3.1 BCU replacement** 

**Have you detected a faulty BCU?:** 

After replacing the BCU, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.2 Module Replacement** 

#### **Have you detected a faulty module?:** 

In the meantime you can use the battery system with the remaining modules and a correspondingly reduced capacity (take into account the minimum number of modules). 

Please note: It is important that all modules of a battery tower have a similar state of charge (SOC) with a tolerance of 5%. New modules have about **30** % SOC. If the remaining modules have not yet been put into operation (not charged / discharged), the new module can easily be added. Otherwise, it is basically a module extension. In this case, please add the new module to the system only when the system has a SOC between 25% and 35% (see extension process in the manual). Make sure to configure correctly after any change in module number. 





15

<!-- pág. 16 -->
|**BYD Battery-Box Premium HVS/HVM Service Checklist - V1.5 EN**|
|---|



|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Box are only<br>i|
|---|
|allowed by professional and qualified electricians. Improper handling can cause danger and damage. This document does<br>fi|
|not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the information.|



> ⚠ REVISAR TABLA — pág. 16: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**1.**<br>**GENERAL STEPS**<br>Please carefully check**all**„General Steps“ from page 3 of the Service Guide  i|line and confirm this in t|i   he boxes below|
|---|---|---|
|1.1 Configuration<br>1.4 Closed Connecti|on Area<br>1.7|Restart|
|1.2 Only HVS or HVM<br>1.5 Latest Firmware|1.8|Correct Operation|
|1.3 External Connections<br>1.6 App Configuratio|in||
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the**error related**Analysis from Chapter 2 of the Service Guid<br>information related to those Sections|eline that you checked, a|nd collect all the|
|2.1 BCU shows no reaction / No LED<br>2.5 S|OC & charging logic|2.9 BCU LED event code (EC)|
|2.2 BCU switch cannot be pulled up / LED remains on<br>2.6|Unexpected shutdown|2.10 Voltage measurement<br>|
|2.3 Problem with FW Update / App Configuration / Battery WIFI<br>2.7<br>|Module Extension /<br>Parallel connection|and undervoltage<br>211 Identifin a fault|
|2.4 Battery <> Inverter communication / no charging or<br> <br> <br>|<br>|. yg  y<br>module / Module<br>|
|discharging<br>2.8|e Connect Plus (BCP)|exclusion method|
|**3.**<br>Please fill all available information in below table. Some information like th<br>**SERVICE INFORMATION**|i          e Serial Number of the B|i               CU is mandatory to receive service.|
|**•**<br>**Service Ticket Number or System ID:**|||
|**•**<br>**Installer / Delivery Address / Contact:**|||
|Company|ZIP / City||
|Contact Person|Phone||
|Street / Nr.|Email||
|**•**<br>**System Information**|||
|Battery Configuration (e.g. HVS5.1 / 2xHVM11.0 /...)|BMU Firmware||
|BCU Serial Number|BMS Firmware||
|BCU Connected to Internet<br>Yes<br>No|Inverter Firmware||
|Inverter Brand + Model|System Name on<br>Inverter Portal||
|Inverter Serial Number|<br>( Provide access for: i|nfo@eft-systems.de )|
|Commissioning Date|||
|**•**<br>**Service Information**|||
|BCU EventCode (EC)|Inverter Error Code||
|Was the battery charging / discharging before (was the system working nor|mally before?)|Yes<br>No|
|Take pictures of open communication port in the BCU and Inverter clearly s|howing connection cable|s|
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see|chapter 2.8)||
|Description of<br>the Problem<br>Please provide any additional information that is necessary or could help in<br>wrong module, video of a special behaviour; pictures; app screenshots; mo|the analysis of the servic<br>dule voltages... )|e case (e.g. serial number of a|
|By contacting us you confirm, that a qualified person has done the necessary control a<br>Service Contact:<br>Europe: EFT-Systems GmbH<br>www.eft-systems.de<br>service@eft-sstemsde|i   i       nd collected all available<br>Australia:  Alps Power<br>www.alpsp<br>service@al|i   i           information above.<br>Pty Ltd<br>ower.com.au<br>sowercomau|
|y.<br>+49 9352 8523999<br>+34 9106 02267 (ES)<br>|+61 02 800|p..<br>5 6688|
|+44 2037 695998 (UK)        +39 0287 368364 (IT)<br>For Europe only: Register Ticket directly in the Online Service Center: https://support.e|ft-systems.de/||
