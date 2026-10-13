# Battery-Box Premium LVL — Guía de servicio y checklist

- **Producto:** Battery-Box Premium LVL (LVL)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.2 / 2022-01-11
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/2022-01-11_BYD_Battery-Box_Premium_LVL_Service_Guideline_and_Checklist_EN_V1.2-620b633a4f403.pdf
- **SHA-256 del PDF:** 8c897b86d76862aa5159d75cb1e27ef8810c9d5a276daa82d60cd34f6229cc6e
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/2022-01-11_BYD_Battery-Box_Premium_LVL_Service_Guideline_and_Checklist_EN_V1.2-620b633a4f403.pdf
- **Conversión:** pymupdf4llm 1.28.2, 15 págs.

> ⚠ Este documento tiene 2 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium LVL Service Guideline and Checklist** Version 1.2 

# Valid for Premium LVL 15.4 



LVL 15.4  (max. 64 per system) 



BMU (1 x per system) 



**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com</u> / <u>www.eft-systems.de</u> / <u>www.alpspower.com.au.</u> Subject to technical modifications; no responsibility is accepted for the accuracy of this information. Attention: Improper handling can cause danger and damage.

<!-- pág. 2 -->
## CONTENT 

|**CONTENT**|**2**|
|---|---|
|**1. GENERAL STEPS**|**3**|
|**2. ERROR ANALYSIS**|**4**|
|2.1 BMU does not turn on / BMU LED is off or flickering abnormally|4|
|2.2 Problem with the Firmware Update / App Configuration / Battery WiFi|5|
|2.3 Incorrect output voltage / No BMS Data / BMU EC102|6|
|2.4 Communication issue with Inverter / BMU EC106|7|
|2.5 SOC & charging logic|7|
|2.6 Unexpected shutdown|7|
|2.7 BMU/BMS LED event code (EC)|8|
|2.8 Be Connect Plus (BCP)|11|
|2.9 Voltage measurement and undervoltage|12|
|2.10 Unit Exclusion Method (only when at least 2 LVLs / parallel connection)|13|
|**3. SERVICE TASKS**|**14**|
|3.1 BMU Replacement|14|
|3.2 BMS Replacement|14|
|3.3 BIC Replacement|14|
|**SERVICE CHECKLIST AND CONTACT INFORMATION**|**15**|





2

<!-- pág. 3 -->
## 1. GENERAL STEPS 

**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** Please proceed first with the installation steps by: 

|**No.**<br>1|**Name**<br>Configuration|**Description**<br>Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium LVL<br>Minimum Configuration List” (V1.8 or above) available at: **www.bydbatterybox.com**<br>Make sure the inverter is configured correctly.|
|---|---|---|
|2|Correct internal<br>cabling||
|||Please double check, referring to the manual|
|3|Correct external<br>cabling|1.<br>Communication to inverter<br>a.<br>Depending on the choice of inverter the cable between the BMU<br>port and the inverter must be specially made. Please check the<br>specifications in the installation manual.<br>b.<br>Recommended CAT5 or higher;<br>c.<br>Check the cables and replace them if necessary<br>2.<br>Grounding<br>a.<br>Battery-Box connected directly to the ground-bus of the house.<br>b.<br>The battery must not be earthed via the inverter! Otherwise,<br>communication problems are possible.<br>3.<br>Ethernet-Cable for Internet (**strongly recommended!**)<br>4.<br>DC-Ports - Make sure that**+**and**-**are properly connected.<br>5.<br>Correct parallel connection cabling if applicable|
|4|Latest Firmware|Always update the**newest Firmware**! (with using the latest App Version)<br>Note: If not stated otherwise, wifi password is BYDB-Box|
|5|App Configuration|To complete the commissioning, the configuration of the battery via  “BYD Be<br>Connect” App or PC tool “Be Connect Plus” (BCP)  is**mandatory**!|
|6|Restart|After app configuration, please perform a proper restart of the system by switching off<br>the battery correctly (press LED Button on**BMU**for 5 sec). Make sure all LEDs of the<br>battery are completely off. Then follow the correct switch on procedure (see step 7)|
|7|Switch on procedure|Correct switch on procedure is important for a correct operation!<br>1.<br>Switch on the fuse between Inverter and Battery (if there is any)<br>2.<br>Switch on the Battery-Box (button on LVL)<br>3.<br>Activate the inverter after the battery|
|8|Checking the correct<br>operation|The system runs properly if:<br>- Inverter displays battery SOC correctly<br>- System charges / discharges<br>Note: **If you can not complete the commissioning, then turn off the battery before**<br>**you leave the site and make sure all LEDs are off to avoid a discharge of the battery.**|





3

<!-- pág. 4 -->
## 2. ERROR ANALYSIS 

Please refer to the general steps before proceeding, see chapter 1. 

### **2.1 BMU does not turn on / BMU LED is off or flickering abnormally** 

LEDs of BMU do not light up, although the battery is ON. 

|**No.**|**Name**|**Description**|
|---|---|---|
|9|Check correct cable port|Make sure that the correct data cable port has been used at the BMU (“BMS” port.<br>Do not mix with “inverter” or “Ethernet” port).|
|10|Replace Comm Cable|Try a completely new communication cable between battery and BMU.<br>Note: Sometimes it might be necessary to unplug the communication cable and<br>plug it again while batteries are switched on.|
|11<br>12|Voltage measurement on<br>pin 7&8<br>Only LED faulty?|Measure the voltage of PIN 7 & 8 while the other side of the cable is connected to<br>the IN port of the Battery-Box and while the Battery-Box is powered on. Voltage<br>should be around 50V. If yes: try another BMU (if available). If no: check another<br>cable or try another LVL if multiple batteries are installed in the system.<br>In some rare cases, the LED of the BMU is faulty. To check that: check if there is a<br>WIFI access point of the Battery-Box and check if there are internal LEDs inside the<br>BMU. If so, only the external LED is inactive and a commissioning could still work.|
|13|Voltage measurement|Check voltage of battery. See**Section 2.9**|
|14|BMU exchange|If problem remains:<br>Test another BMU, if available.|





4

<!-- pág. 5 -->
### **2.2 Problem with the Firmware Update / App Configuration / Battery WiFi** 

The Battery Management consists of two components: the BMU and the BMS. The  Firmware Update from the App will update the BMU, which will then update the BMS. **The BMS update can take up to 30 Minutes** . 

|**No.**|**Name**|**Description**|
|---|---|---|
|15|Correct App and<br>Firmware|Make sure to have the latest App version (>1.7.4) and Battery Firmware (download<br>inside the App) on your mobile device before connecting the app with battery WiFi.<br>If the App cannot be installed, or other general Problems occur with the App:<br>-<br>Try with a different mobile device (For Android: min Android version<br>requirement is 4.4. )<br>-<br>Try with PC Tool BCP (**section 2.8**)<br>-<br>Note: If the WiFi connection is not stable you might remove the lan cable<br>during the configuration. Once the battery has been configured correctly<br>you can connect it again to the Internet.|
|16|WiFi cannot be found /<br>WiFi unstable|The Battery WiFi turns off 5 hours after the start of the Battery. To reactivate the WiFi,<br>press the LED button of the BMU about 1 second or restart the system.<br>To reset the WiFi, press the LED button of the BMU  three times 1 second within 6<br>seconds.<br>If problem remains:<br>- remove the lan cable during the configuration. Once the Battery has been configured<br>correctly you can connect it again to the Internet.<br>- check whether other mobile devices are connected the same wifi<br>- try another mobile device|
|17|Proper restart|Note: Whenever the configuration via Be Connect app / Be Connect Plus tool is<br>changed, a restart of the battery is necessary to make sure that all changes come<br>into effect.<br>1. Switch off the Inverter<br>2. Switch off the battery (Press button on BMU for 5 seconds until all batteries switch<br>off. All LEDs should be off)<br>3. Wait for 2 Minutes<br>4. Turn on the Battery (button on battery connected to BMU) and then<br>5. Turn on inverter second|
|18|Close and restart the App|If the App does not react anymore after some minutes loading during the update<br>process, close (close the program completely) and restart the App. Or try with PC<br>Tool BCP (**section 2.8)**|
|19|BMS Version not updated|The App will only update the BMU. The BMU will update the BMS, which**can take up**<br>**to 30 minutes**.<br>If the BMS Version is not updated after 30min with stable inverter communication,<br>follow the below Process:<br>1.<br>Update Firmware through the App again<br>2.<br>Restart the system<br>a.<br>Switch off the Inverter first,  then switch off the battery second<br>(Press the LED of the BMU for 5 seconds)<br>b.<br>Wait for 2 Minutes<br>c.<br>Turn on the Battery first, then turn on the inverter second<br>3.<br>Wait for 30 Minutes<br>4.<br>Check BMS Firmware Version again with App. If Version is still wrong,<br>please do the update process again (if possible with another mobile<br>device).<br>5.<br>Note: if Voltage of Battery is not shown in Be Connect, the update will not<br>be transferred to BMS. Make sure the BMU recognizes BMS properly.|





5

<!-- pág. 6 -->
### **2.3 Incorrect output voltage / No BMS Data / BMU EC102** 

Wrong PDU output voltage (e.g 16V) is normally an indicator for incorrect configuration or  BMU<>BMS communication issue 

|**No.**|**Name**|**Description**|
|---|---|---|
|20|Battery correctly<br>configured?|Please check if the App configuration was successful and the Firmware is the<br>most recent one. If there are problems, please refer to**Section 2.2**<br>**Note: It is important to select the correct system quantity. Else, the output**<br>**voltage might be wrong!**The quantity you need to select refers to the overall<br>quantity of LVL15.4 units. If you have 2xLVL15.4 connected in parallel, you need to<br>select the system quantity of “2” in the Be Connect app / BCP tool.<br>Note: Don’t forget to**properly restart system**after changing configuration!|
|21|Proper restart|Note: Whenever the configuration via Be Connect app / Be Connect Plus tool is<br>changed, a restart of the battery is necessary to make sure that all changes come<br>into effect.|
|||1. Switch off the Inverter<br>2. Switch off the battery (Press button on BMU for 5 seconds until all batteries<br>switch off. All LEDs should be off)<br>3. Wait for 2 Minutes<br>4. Turn on the Battery (button on battery connected to BMU) and then<br>5. Turn on inverter second|
|22|BMU<>BMS<br>communication|make sure that the comm cable is connected to the right port of BMU (the one<br>labeled as "BMS"). Replace comm cable between BMU and battery.|
|23|Check terminal resistor|Make sure that the terminal resistor is connected to the OUT port (Terminal<br>resistor properties: 120 Ω resistor between pin 5 and 6)<br>If it was connected already, then please remove it and try without it to rule out a<br>faulty terminal resistor. Don't forget to properly restart system afterwards.|
|24|No output voltage /<br>incorrect output voltage|When there is no output voltage, this typically means that the BMS relay is not<br>closed. This can have many reasons:<br>-<br>Check if BMU properly detects BMS data (cell voltages, cell<br>temperatures). If not, see following step 25.<br>-<br>Check LED codes (see**section 2.7**)|
|25|BMU<>BMS<br>communication / No BMS<br>data shown / BMS data is<br>0|make sure that the comm cable is connected to the right port of BMU (the one<br>labeled as "BMS"). Replace comm cable between BMU and battery.<br>**Note: as long as there is a communication problem between BMU & BMS, you**<br>**won’t be able to see any BMS data / values will appear as zero and the relay will**<br>**remain open (no output voltage)  In that case, redo app configuration (unit**<br>**quantity must be correct!) and don’t forget to properly restart system!**|
|26|LVL Exclusion Method<br>(for parallel connected<br>systems)|- If multiple LVL batteries connected in parallel: Try the Exclusion Method (**see**<br>**section 2.10)**: Check if the system works when removing the suspected LVL unit<br>Very important: don't forget to reconfigure  and to restart always when changing<br>the configuration!|
|27|Further checking|If problem remains:<br>- Download all data with BCP**(section 2.8)**<br>- Check the inverter<br>- Try replacing the BMU, if available|





6

<!-- pág. 7 -->
### **2.4 Communication issue with Inverter / BMU EC106** 

Output voltage is normal and you can see BMS (cell) data in BCP, but inverter does not detect battery. _Note: if output voltage is incorrect or BMS (cell) data cannot be seen in BCP, then go though_ **_section 2.3_** _first_ 

|**No.**|**Name**|**Description**|
|---|---|---|
|28|Configuration|Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium LVL<br>Minimum Configuration List” (V1.8 or above) available at: **ww.bydbatterybox.com**<br>Make sure the inverter is configured and working correctly.|
|29|Output voltage incorrect?<br>No BMS Data?|Check according to**section 2.3**. Especially make sure to configure battery via app<br>and to properly restart afterwards.|
|30|Inverter settings|Make sure to configure the battery correctly on the inverter interface. Refer to<br>inverter manual for details.|
|31|Replace comm cable|Replace the communication cable (min. CAT5!). Confirm PIN cable configuration<br>for the specific inverter model (see manual)|
|32|Further checking|If problem remains:  Test another BMU, if available|



### **2.5 SOC & charging logic** 

|**No**|**Name**|**Description**|
|---|---|---|
|33|SOC jumps|The SOC of an LFP battery cannot be measured. It is a calculated value. In general, the<br>state of charge (SOC) of a battery is calculated using the voltage, but other factors such<br>as temperature, current flow and charging behavior also play a role. The calculation of the<br>state of charge is generally more precise if the battery regularly sees full cycles. Every now<br>and then an SOC correction / calibration might occur. That is normal.|



### **2.6 Unexpected shutdown** 

System has been successfully commissioned in the past and did run for some time. Later on an unexpected shutdown occured. 

> ⚠ REVISAR TABLA — pág. 7: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No**|**Name**|**Description**|
|---|---|---|
|34|Minimum Configuration<br>fulfilled?|Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium LVL<br>Minimum Configuration List” (V1.8 or above) available at:**www.bydbatterybox.com**<br>Make sure the inverter is configured and working correctly.<br>Note:<br>-<br>if the minimum configuration list is not met, unexpected shutdown(e.g during<br>backup) might occur.<br>-<br>peak power devices can cause shutdowns. Check the peak power of your loads|
|35|Inverter<br>Communication|The battery only works with an compatible external inverter. If for whatever reason the<br>communication between battery and inverter is lost, the battery will shut down itself within<br>30minutes. Therefore, check which one did shut down first ( battery or inverter) and check<br>if inverter is properly detecting battery (e.g showing correct SOC or temperature). If<br>problem remains, check according to**section 2.4**.|
|36|Battery Logs / History<br>Data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log files in order to identify the<br>root cause.  See**section 2.8**for details.|
|37|Inverter Warning &<br>Monitoring|Unexpected Shutdown can be caused by overall system settings. Therefore, it is necessary<br>to evaluate inverter data as well.<br>-<br>Which error message are shown in inverter (portal?<br>-<br>Please provide access to Inverter portal (add info@eft-systems.de and tell us<br>the name of the system in the portal)|





7

<!-- pág. 8 -->
### **2.7 BMU/BMS LED event code (EC)** 

A constant white LED refers to standby mode. White blinking means charge or discharge. 

When the battery is initiating, the LED will flash white and blue with an interval time of 0.5 seconds (normal during startup). When the LED flashes blue with an interval time of 1 second it indicates an event code.  Please start to count when the white LED begins to flash, then count how many times the white and blue LED flashes. (also refer to the manual!) **Example:** 1xwhite, 6xblue → EC 106 / 1xwhite, 11xblue → EC 111 / 3xwhite, 3xblue → EC 303 **Note: every LVL has its own BMS. The Event Code of the BMS will therefore be shown in the LED of the individual LVL.** 



Most errors are caused by a faulty communication line, an incorrect app configuration or the missing restart after the app-configuration. Please go in detail through: **Section 2.2 & 2.3** 

##### **Note: if the system is not correctly configured with the app, the event code (EC) might be misleading.** 

> ⚠ REVISAR TABLA — pág. 8: 33% de celdas vacías (posibles celdas combinadas)
|**EC**<br>**BMU**|**EC**<br>**BMS**|**Measure**|
|---|---|---|
|EC 101|/|Initialisation Failure.|
|||- Make sure the app-configuration has been completed correctly (especially quantity!).<br>- Restart the system according properly (see**step 17, section 2.2**)|
|||If problem remains:<br>-<br>Download all data with BCP (especially the historical data)**(section 2.8)**<br>-<br>replace BMU, if available|
|EC 102<br>EC 105|/|Incorrect module quantity / Module not detected.<br>- Make sure the app-configuration has been completed correctly (especially quantity!).<br>- Check the terminal resistor. The terminal resistor (120 Ω at pin 5+6) is responsible for a<br>clean communication between BMS and BMU. In rare cases it can be damaged and can<br>disturb the signal. In these rare cases it is recommended to remove the terminal resistor.<br>- replace communication cable between Battery and BMU<br>- Restart the system according properly (see**step 17, section 2.2**)<br>- If multiple LVL batteries connected in parallel: Unit Exclusion Method (**see section 2.10)**:<br>Check if the system works when removing the suspected LVL unit|
|||If problem remains:<br>-<br>Download all data with BCP (especially the historical data)**(section 2.8)**<br>-<br>replace BMU, if available|





8

<!-- pág. 9 -->
PreCharge Fault. EC 103 EC 108 - Check the DC cabling and make sure that the Minimum Configuration is met. - Restart the system according properly (see **step 17, section 2.2** ) - If multiple LVL batteries connected in parallel: Exclusion Method ( **see section 2.10)** : Check if the system works when removing the suspected LVL unit If problem remains: - Download all data with BCP (especially the historical and the cell data) **(section 2.8)** - provide the SN and voltage of the suspected LVL unit (see checklist on last page) EC 104 EC 101 Short circuit / DC reverse connection. - Check DC cabling (is there any short circuit? Is the fuse between battery and inverter closed?) - Disconnect the battery system from the inverter and restart the battery system alone (battery isolated), to evaluate if the error is being caused externally (i.e. short circuit in inverter or MPPT). If the Event Code remains, the error might be in the battery. If the Event Code has changed, there might be an error in the inverter side. - If multiple LVL batteries connected in parallel: Exclusion Method ( **see section 2.10)** : Check if the system works when removing the suspected LVL unit If problem remains: - Download all data with BCP (especially the historical and the cell data) **(section 2.8)** - provide the SN and voltage of the suspected LVL unit (see checklist on last page) EC 104 EC 103 BIC Communication Failure. Turn on battery and check whether the blueLED lights on the two BIC boards are on (BIC = circuit boards directly on the two battery modules inside LVL - see **section 3.3** ). - If blue LED on BIC boards are on: - try to exchange the upper BIC with the lower one. - if problem remains: BIC replacement might be necessary - If blue LED on BIC boards are off: - Check if there is any sign of short circuit in the BICs (e.g. component damage). - Check the sampling cables connection: B2+ up left / B1+ bottom left / B2- up right / B1- bottom right - if problem remains: BIC replacement might be necessary - If multiple LVL batteries connected in parallel: Exclusion Method ( **see section 2.10)** : Check if the system works when removing the suspected LVL unit. Try swapping the BIC boards of two different LVL units. If problem remains: - Download all data with BCP (especially the historical and the cell data) **(section 2.8)** - Measure the cell voltage according to **section 2.9** - provide the SN and voltage of the LVL with the EC (see checklist on last page) EC 104 EC 107 Undervoltage. EC 113 - Shut down the system quickly to avoid further discharge. Check whether the system can shut down normally (by pressing the LED button in BMU for 5s). - Follow **section 2.9** (Voltage measurement of cells) 



9

<!-- pág. 10 -->
|EC 104|EC 102<br>up to<br>EC112<br>(All other than<br>101, 103, 107,<br>113)|One of the BMS (LVL units) reports an event message.<br>- If multiple LVL batteries connected in parallel: Exclusion Method (**see section 2.10)**:<br>Check if the system works when removing the suspected LVL unit<br>If problem remains:<br>-<br>Check the voltage of the batteries according to**section 2.8**9Download all data<br>with BCP (especially the historical and the cell data)**(section 2.8)**<br>-<br>provide the SN and voltage of the suspected LVL (see checklist on last page)|
|---|---|---|
|EC 106|/|No communication with Inverter.|
|||- Make sure the inverter is on, configured and working correctly.<br>- Check according to**section 2.4**|





10

<!-- pág. 11 -->
### **2.8 Be Connect Plus (BCP)** 

Be Connect Plus is a Windows-PC tool. With Be Connect Plus (BCP) you can: 

   - read the battery information, 

- configure the battery system 

- update BMU & BMS firmware 

- Export / download battery logs (From BMU and all BMS) 

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the Tool on www.bydbatterybox.com / www.eft-systems.de / www.alpspower.com.au** . 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual inside of program ZIP archive). 

Note: You need a computer with Windows that will be connected to the battery Wifi. Login as Installer to Be Connect Plus, the password is the same as for WiFi: BYDB-Box 





11

<!-- pág. 12 -->
### **2.9 Voltage measurement and undervoltage** 

**Attention: Make sure not to create a short circuit!** 

- **You can see the max. and min. cell voltage in the BeConnect App or in PC Tool Be Connect plus (BCP)** 

- **You can get the detailed module and cell voltage in the BCP Program (section 2.8)** 

- **or measure it manually according to the below description:** 

**Measure the module voltage:** Open the front door and measure the tower voltage between **B+/B-** (red circle). Measure also between **P+/P-** (green circle) on the BMS as shown below. 



**Measure the cell voltages** in case of BMS EC 107, EC 103, or if BCP shows cells with <1.5 V / does not show cell voltages. This will help us to understand if the issue is in the cell or in the BICs. The voltage has to be measured in pairs as shown below. If the voltage is 0, in most cases this value is not correct and the measuring device is not in correct contact with the PINs. (please establish a correct and good contact) 







Please record these measurements of 16 cells in total. (Cell Number 1-8 for button module, 9-16 for upper module) 



12

<!-- pág. 13 -->
#### **Undervoltage** 

A LVL in which one of the 16 cells has a voltage of <1.5 V is in undervoltage (check with BCP ( **section 2.8** ) / BC if possible). 

- LVL with >45 V should be fine and you can continue to check other points according to this service guideline. - If the LVL voltage is <45V but the single cell voltage is >1.5V, the battery needs to be charged quickly while avoiding any further discharge. Therefore shutdown the system and search the problem according to the guideline, while the battery is completely off. Also check on the inverter side why the force charge doesn’t work. Do not turn on the battery before making sure the inverter should be able to charge the battery. 

- If only one LVL is in undervoltage: remove that one and try commissioning without it. Otherwise, make sure to avoid further overdischarge. (Turn off the system completely) 

- If one, or all LVL are in undervoltage: Contact the service as stated below and make sure to avoid any further discharge of the battery (Turn off the system completely) 

When contacting the service, make sure to fill the service checklist completely and add the following information: 

- Serial Numbers (of the BMU and all (affected) LVL) 

- Individual LVL voltages of all LVL (related to Serialnumber) 

- Logs from the battery using BCP ( **section 2.8** ) and Screenshots showing the cell voltages, or manual cell voltage measurements 

- Initial Firmware (FW) Version of the Battery when the UV happened (BMU and BMS) 

- Detailed description how and why the system reached Undervoltage if known. Information when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the Batteries status when the battery was left (on / off / LED). 

- Inverter Model, Serial Number and Inverter Logs 

- Access to Inverter portal (add <u>info@eft-systems.de and tell us the name of the system in the portal)</u> 

### **2.10 Unit Exclusion Method (only when at least 2 LVLs / parallel connection)** 

- Normally a faulty LVL unit can be identified with the Be Connect Plus Program or by the LED Code of the corresponding LVL unit. In this case, remove the suspicious LVL unit with the Event Code from the system, and commission the remaining system (if it still complies with the minimum configuration list) and check if it runs properly. 

- Otherwise, try the each LVL one by one 

**Important: The unit quantity must be adjusted in the app whenever the number of modules has been changed! Don’t forget to perform a proper restart after a new configuration!** 

1. Switch off the Inverter 

2. Switch off the battery (Press button on BMU for 5 seconds until all batteries switch off. All LEDs should be off) 

3. Wait for 2 Minutes 

4. Turn on the Battery (button on battery connected to BMU) and then 

5. Turn on inverter second 



13

<!-- pág. 14 -->
## 3. SERVICE TASKS 

Please go through the general and error specific steps beforehand, see chapter 1 and 2. 

### **3.1 BMU Replacement** 

**Have you detected a faulty BMU?:** 

After replacing the BMU, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.2 BMS Replacement** 

Refer to Manual “ _BMS Drawer Replacement Guide_ ” After replacing the BMS, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.3 BIC Replacement** 

Refer to Manual “ _BIC Board Replacement Guide_ ” 

After replacing the BICs, please do not forget to re-do the configuration and firmware-update with the app or BCP. 





14

<!-- pág. 15 -->
|**BYD Battery-Box Premium LVL Service Checklist - V1.2 EN**|
|---|



|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Box are only<br>i|
|---|
|allowed by professional and qualified electricians. Improper handling can cause danger and damage. This document does<br>fi|
|not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the information.|



|**1.**<br>**GENERAL STEPS**<br>Please carefully check**all**„General Steps“ from page 3 of the Service Guideline and confirm this in the boxes below|
|---|
|1.1 Configuration<br>1.4 Latest Firmware<br>1.7 Switch on procedure|
|1.2 Correct internal cabling<br>1.5 App Configuration<br>1.8 Correct Operation|
|1.3 Correct external cabling<br>1.6 Restart|
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the**error related**Analysis from Chapter 2 of the Service Guideline that you checked, and collect all the<br>information related to those Sections|
|2.1 BMU does not turn on / BMU LED is off or flickering abnormally<br>2.5 SOC & charging logic<br>2.8 Be Connect Plus (BCP)|
|2.2 Problem with the FW Update / App Configuration / WiFi<br>2.6 Unexpected shutdown<br>2.9 Voltage measurement<br>|
|2.3 Incorrect output voltage / No BMS Data / BMU EC102<br>2.7 BMU / BMS LED event<br>d EC<br>and undervoltage<br>210 Uit Eli Mthd|
|24 Citi i ith It / BMU EC106<br>coe ()<br>. n xcuson eo<br>|
|. ommuncaon ssue w nverer<br>(≥ 2 x LVL)|
|**3.**<br>Please fill all available information in below table. Some information like the Serial Number of the BMU is mandatory to receive service.<br>**SERVICE INFORMATION**|
|**•**<br>**Service Ticket Number or System ID:**|
|**•**<br>**Installer / Delivery Address / Contact:**|
|Company<br>ZIP / City|
|Contact Person<br>Phone|
|Street / Nr.<br>Email|
|**•**<br>**System Information**|
|Battery Configuration (X x LVL)<br>BMU Firmware|
|BMU Serial Number<br>BMS Firmware|
|BMU Connected to Internet<br>Inverter Firmware<br>Yes<br>No|
|Inverter Brand + Model<br>System Name on<br>Inverter Portal|
|Inverter Serial Number<br>( Provide access for: info@eft-systems.de )|
|Commissioning Date|
|**•**<br>**Service Information**|
|BMU EventCode (EC)<br>Inverter Error Code|
|BMS EventCode(s) and related LVL Serial Number(s)|
|Was the battery charging / discharging before (was the system working normally before?)<br>Yes<br>No|
|Take pictures of open communication port in the Battery and Inverter clearly showing connection cables|
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see chapter 2.8)|
|Description of<br>the Problem|
|Please provide any additional information that is necessary or could help in the analysis of the service case (e.g. serial number of a<br>wrong module, video of a special behaviour; pictures; app screenshots; module voltages... )|
|By contacting us you confirm, that a qualified person has done the necessary control and collected all available information above.|
|Service Contact:<br>Europe: EFT-Systems GmbH<br>Australia:  Alps Power Pty Ltd<br>www.eft-systems.de<br>www.alpspower.com.au<br>service@eft-sstemsde<br>service@alsowercomau|
|y.<br>pp..<br>+49 9352 8523999<br>+34 9106 02267 ES<br>+61 02 8005 6688|
|<br>()<br> <br>|
|+44 2037 695998 (UK)        +39 0287 368364 (IT)<br>For Europe only: Register Ticket directly in the Online Service Center: https://support.eft-systems.de/|
