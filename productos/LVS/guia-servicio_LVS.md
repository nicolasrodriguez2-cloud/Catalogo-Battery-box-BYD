# Battery-Box Premium LVS — Guía de servicio y checklist

- **Producto:** Battery-Box Premium LVS (LVS)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.1 / 2022-02-13
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/2022-02-13_BYD_Battery-Box_Premium_LVS_Service_Guideline_and_Checklist_EN_V1.1-620b60a73ad9e.pdf
- **SHA-256 del PDF:** e1ff294de3153557afeaf0cbc584de901c97c86acce9b899b47eaeb76436e23c
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/2022-02-13_BYD_Battery-Box_Premium_LVS_Service_Guideline_and_Checklist_EN_V1.1-620b60a73ad9e.pdf
- **Conversión:** pymupdf4llm 1.28.2, 14 págs.

> ⚠ Este documento tiene 1 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium LVS Service Guideline and Checklist** Version 1.1 

Valid for Premium LVS 4.0 / 8.0 / 12.0 / 16.0 / 20.0 / 24.0 



LVS 16.0  (4 Modules + PDU. Max. 64 Modules in 16 Towers per System) 



BMU (1 x per System) 



**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com</u> / <u>www.eft-systems.de</u> / <u>www.alpspower.com.au.</u> Subject to technical modifications; no responsibility is accepted for the accuracy of this information. Attention: Improper handling can cause danger and damage.

<!-- pág. 2 -->
## CONTENT 

|**CONTENT**|**2**|
|---|---|
|**1. GENERAL STEPS**|**3**|
|**2. ERROR ANALYSIS**|**4**|
|2.1 BMU does not turn on / BMU LED is off or flickering abnormally|4|
|2.2 Modules do not show any reaction / No LED on module|4|
|2.3 Problem with the Firmware Update / App Configuration / Battery WiFi|5|
|2.4 Incorrect output voltage / No BMS Data / BMU EC102|6|
|2.5 Communication issue with Inverter / BMU EC106|7|
|2.6 SOC & charging logic|7|
|2.7 Unexpected shutdown|7|
|2.8 BMU/BMS LED Event Code (EC)|8|
|2.9 Be Connect Plus (BCP)|10|
|2.10 Voltage measurement and undervoltage|11|
|2.11 Module Exclusion Method (Identifying a faulty module)|12|
|**3. SERVICE TASKS**|**13**|
|3.1 BMU Replacement|13|
|3.2 PDU Replacement|13|
|3.3 LVS Module Replacement|13|
|**SERVICE CHECKLIST AND CONTACT INFORMATION**|**14**|





2

<!-- pág. 3 -->
## 1. GENERAL STEPS 

**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** Please proceed first with the installation steps by: 

|**No.**|**Name**|**Descript**|**ion**||
|---|---|---|---|---|
|1|Configuration|Check if  i<br>Minimu i<br>Make su    i|the config<br>m Configu<br>re the inv  i|iuration is correct. Refer to latest “BYD Battery-Box Premium LVS<br>iration List” (V1.7 or above) available at: **www.bydbatterybox.com**<br>erter is configured correctly.|
|2|Correct external<br>cabling|1.<br>2.<br>3.<br>4.<br>5.|Commu<br>a.<br>b.<br>c.<br>Groundi<br>a.<br>b.<br>Etherne<br>Correct<br>DC-Port<br>piece re|nication to inverter<br>Depending on the choice of inverter the cable between the BMU port<br>and the inverter must be specially made. Please check the<br>specifications in the installation manual.<br>Recommended CAT5 or higher;<br>Check the cables and replace them if necessary<br>ng<br>Battery-Box connected directly to the ground-bus of the house.<br>The battery must not be earthed via the inverter! Otherwise,<br>communication problems are possible.<br>t-Cable for Internet (**strongly recommended!**)<br>parallel connection cabling if applicable<br>s - Make sure that**+**and**-**are properly connected. (Male DC Connector<br>quired)|
|||Notes ab<br>- DC cab        i<br>a necess<br>the batte<br>- The DC<br>of delive|out DC c<br>le cross s      i<br>ary cable<br>ry and th<br>male con<br>ry. They n|onnection:<br>ection:  depends on the respective configuration. BYD does not specify<br>cross-section herePlease pay attention to the power and current of<br>e inverter, as well as the local rules.<br>nectors (35mm² / 50m² / 70mm²) are not included in the PDU scope<br>eed to be ordered separately from your PV distributor.|





|3<br>Latest Firmware|Always update the**newest Firmware**! (with using the latest App Version)<br>Note: If not stated otherwise, wifi password is BYDB-Box|
|---|---|
|4<br>App Configuration|To complete the commissioning, the configuration of the battery via  “Be Connect” App<br>or PC tool “Be Connect Plus” (BCP) is**mandatory**! Please restart battery afterwards.|
|5<br>Proper Restart|Switch off:<br>1.<br>Press BMU LED Button for 5 seconds. All modules should be off then. Make<br>sure all LEDs of the battery are completely off. Note: if the modules do not<br>turn off then, something is wrong in the PDU<>BMU connection. Replace<br>comm cable and try again.|
||Switch on (mind the sequence!)<br>1.<br>Switch on the fuse between Inverter and Battery (if there is any)<br>2.<br>Switch on the Battery (press LED Button on the topmost module for 3<br>seconds. All modules should become active then)<br>3.<br>Turn on the inverter|
|6<br>Checking the correct<br>operation|The system runs properly if:<br>- Inverter displays battery SOC correctly<br>- System charges / discharges<br>Note: **If you can not complete the commissioning, then turn off the battery before you**<br>**leave the site and make sure all LEDs are off to avoid a discharge of the battery.**|





3

<!-- pág. 4 -->
## 2. ERROR ANALYSIS 

Please refer to the general steps before proceeding, see chapter 1. 

### **2.1 BMU does not turn on / BMU LED is off or flickering abnormally** 

LEDs of BMU do not light up, although the battery is ON. 

|**No.**|**Name**|**Description**|
|---|---|---|
|7|Check correct cable port|Make sure that the correct data cable port has been used at the BMU (“BMS” port.<br>Do not mix with “inverter” or “Ethernet” port).|
|8|Replace Comm Cable|Try a completely new communication cable between battery and BMU.<br>Note: Sometimes it might be necessary to unplug the communication cable and<br>plug it again while batteries are switched on.|
|9|Voltage measurement on<br>pin 7&8|Measure the voltage of PIN 7 & 8 while the other side of the cable is connected to<br>the IN port of the Battery-Box and while the Battery-Box is powered on. Voltage<br>should be around 50V. If yes: try another BMU (if available). If no: check another<br>cable or try another LVS if multiple batteries are installed in the system.|
|10|Only LED faulty?|In some rare cases, the LED of the BMU is faulty. To check that: check if there is a<br>WIFI access point of the Battery-Box and check if there are internal LEDs inside the<br>BMU. If so, only the external LED is inactive and a commissioning could still work.|
|11|Voltage measurement|Check voltage of battery. See**Section 2.10**|
|12|Module Exclusion Method|Check if system works when removing the suspected module. See**section 2.11**|
|13|BMU exchange|If problem remains:<br>Test another BMU, if available.|



### **2.2 Modules do not show any reaction / No LED on module** 

LEDs of some module do not light up,although button on topmost module is pressed for 3 seconds.. 

|**No.**|**Name**|**Description**|
|---|---|---|
|14|Swap module position|Note: If top modules have active LED but bottom modules don’t, it indicates a<br>connection issue between modules. Example:<br>_LVS16.0 (4 modules). Module 1&2 have LED, module 3&4 don’t have LED._<br>_Issue is in the connection between module 2 &3. Problem likely to be_<br>_module 2 (less likely: module 3)._<br>- Remove the affected module and check whether problem disappears. If not,<br>check the module below.<br>- Rearrange the modules in the tower.<br>Note: The affected module often works without restrictions at the lowest module<br>position of the tower.|





4

<!-- pág. 5 -->
|15|Only LED faulty?|In some rare cases, the LED of the module is faulty. To check that: use  PC Tool<br>BCP and check under “diagnosis” if all modules (“BMS”) are detected correctly.|
|---|---|---|
|16|Voltage measurement|Check voltage of battery. See**Section 2.10**|
|17|Module Exclusion Method|- Module Exclusion Method (**see section 2.11)**: Check if the system works when<br>removing the suspected module|



### **2.3 Problem with the Firmware Update / App Configuration / Battery WiFi** 

The Battery Management consists of two components: the BMU and the BMS. The  Firmware Update from the App will update the BMU, which will then update the BMS. **The BMS update can take up to 30 Minutes** . 

|**No.**|**Name**|**Description**|
|---|---|---|
|18|Correct App and<br>Firmware|Make sure to have the latest App version (>1.7.4) and Battery Firmware (download<br>inside the App) on your mobile device before connecting the app with battery WiFi.<br>If the App cannot be installed, or other general Problems occur with the App:<br>-<br>Try with a different mobile device (For Android: min Android version<br>requirement is 4.4. )<br>-<br>Try with PC Tool BCP (**section 2.9**)<br>-<br>Note: If the WiFi connection is not stable you might remove the lan cable<br>during the configuration. Once the battery has been configured correctly<br>you can connect it again to the Internet.|
|19|WiFi cannot be found /<br>WiFi unstable|The Battery WiFi turns off 5 hours after the start of the Battery. To reactivate the WiFi,<br>press the LED button of the BMU about 1 second or restart the system.<br>To reset the WiFi, press the LED button of the BMU three times 1 second within 6<br>seconds.<br>If problem remains:<br>- remove the lan cable during the configuration. Once the Battery has been configured<br>correctly you can connect it again to the Internet.<br>- check whether other mobile devices are connected the same wifi<br>- try another mobile device|
|20|Proper restart|Note: Whenever the configuration via Be Connect app / Be Connect Plus tool is<br>changed, a restart of the battery is necessary to make sure that all changes come<br>into effect (see**step 5 in section 1**)|
|21|Close and restart the App|If the App does not react anymore after some minutes loading during the update<br>process, close (close the program completely) and restart the App. Or try with PC<br>Tool BCP (**section 2.9)**|
|22|BMS Version not updated|The App updates the BMU which updates the BMS,. This**can take up to 30 min.**.<br>If the BMS Version is not updated after 30min with stable inverter communication,<br>follow the below Process:<br>1.<br>Update Firmware through the App again<br>2.<br>Restart the system<br>a.<br>Switch off the Inverter first,  then switch off the battery second<br>(Press the LED of the BMU for 5 seconds)<br>b.<br>Wait for 2 Minutes<br>c.<br>Turn on the Battery first, then turn on the inverter second<br>3.<br>Wait for 30 Minutes<br>4.<br>Check BMS Firmware Version again with App. If Version is still wrong,<br>please do the update process again (if possible with another mobile<br>device).<br>5.<br>Note: if Voltage of Battery is not shown in Be Connect, the update will not<br>be transferred to BMS. Make sure the BMU recognizes BMS properly.|





5

<!-- pág. 6 -->
### **2.4 Incorrect output voltage / No BMS Data / BMU EC102** 

Wrong PDU output voltage (e.g 16V) is normally an indicator for incorrect configuration or  BMU<>BMS communication issue 

|**No.**|**Name**|**Description**|
|---|---|---|
|23|Battery correctly<br>configured?|Please check if the App configuration was successful and the Firmware is the<br>most recent one. If there are problems, please refer to**Section 2.3**<br>**Note: It is important to select the correct module quantity. Else, the PDU output**<br>**voltage will be wrong!**The quantity you need to select refers to the overall quantity<br>of LVS4.0 modules and not to the quantity of towers. If you have 2xLVS16.0<br>connected in parallel, you need to select the module quantity of “8” in the Be<br>Connect app / BCP tool.<br>Note: Don’t forget to**properly restart system**after changing configuration!|
|24|Proper restart|Note: Whenever the configuration via Be Connect app / Be Connect Plus tool is<br>changed, a restart of the battery is necessary to make sure that all changes come<br>into effect.  Make sue to follow the correct switch on procedure (see**step 5 in**<br>**section 1**)|
|25|BMU<>BMS<br>communication|make sure that the comm cable is connected to the right port of BMU (the one<br>labeled as "BMS"). Replace comm cable between BMU and battery.|
|26|Check terminal resistor|Make sure that the terminal resistor is connected to the OUT port (Terminal<br>resistor properties: 120 Ω resistor between pin 5 and 6)<br>If it was connected already, then please remove it and try without it to rule out a<br>faulty terminal resistor. Don't forget to properly restart system afterwards.|
|27|Check Base unit|Issue could be caused by faulty base unit: remove base unit from the tower. That<br>means: place the bottom module to the ground directly, without any base. Don't<br>forget to restart battery. If it works then, the base unit is the root cause then and<br>needs replacing|
|28|Module Exclusion Method|Remove all modules from the tower except one. Restart system with that single<br>module. Don't forget to set new module number in the app / BCP tool (another<br>restart will be necessary afterwards). Repeat that for every of the other modules<br>(first only module A; later only module B et) to identify a potentially faulty module.<br>Very important: don't forget to reconfigure  and to restart always when changing<br>the configuration!|
|29|Further checking|If problem remains:<br>- Download all data with BCP**(section 2.9)**<br>- Check the inverter<br>- Test another BMU, if available<br>- Test another PDU, if available|





6

<!-- pág. 7 -->
### **2.5 Communication issue with Inverter / BMU EC106** 

PDU output voltage is normal and you can see BMS (cell) data in BCP, but inverter does not detect battery. _Note: if PDU output voltage is incorrect (eg 16V) or BMS (cell) data cannot be seen in BCP, then go though_ **_section 2.4_** _first_ 

|**No.**|**Name**|**Description**|
|---|---|---|
|30|Configuration|Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium LVS<br>Minimum Configuration List” (V1.7 or above) available at:<br>**www.bydbatterybox.com**<br>Make sure the inverter is configured and working correctly.|
|31|Output voltage incorrect?<br>No BMS Data?|Check according to**section 2.4**. Especially make sure to configure battery via app<br>and to properly restart afterwards.|
|32|Inverter settings|Make sure to configure the battery correctly on the inverter interface. Refer to<br>inverter manual for details.|
|33|Replace comm cable|Replace the communication cable (min. CAT5!). Confirm PIN cable configuration<br>for the specific inverter model (see manual)|
|34|Further checking|If problem remains:<br>- Test another BMU, if available|



### **2.6 SOC & charging logic** 

|**No**|**Name**|**Description**|
|---|---|---|
|35|SOC jumps|The SOC of an LFP battery cannot be measured. It is a calculated value. In general, the<br>state of charge (SOC) of a battery is calculated using the voltage, but other factors such<br>as temperature, current flow and charging behavior also play a role. The calculation of the<br>state of charge is generally more precise if the battery regularly sees full cycles. Every now<br>and then an SOC correction / calibration might occur. That is normal.|



### **2.7 Unexpected shutdown** 

System has been successfully commissioned in the past and did run for some time. Later on an unexpected shutdown occured. 

> ⚠ REVISAR TABLA — pág. 7: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No**|**Name**|**Description**|
|---|---|---|
|36|Inverter<br>Communication|The battery only works with an compatible external inverter. If for whatever reason the<br>communication between battery and inverter is lost, the battery will shut down itself within<br>30minutes. Therefore, check which one did shut down first (battery or inverter) and check<br>if inverter is properly detecting battery (e.g showing correct SOC or temperature). If<br>problem remains, check according to**section 2.5**.|
|37|Battery Logs / History<br>Data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log files in order to identify the<br>root cause.  See**section 2.9**for details.|
|38|Inverter Warning &<br>Monitoring|Unexpected Shutdown can be caused by overall system settings. Therefore, it is necessary<br>to evaluate inverter data as well.<br>-<br>Which error message are shown in inverter (portal?<br>-<br>Please provide access to Inverter portal (add info@eft-systems.de and tell us<br>the name of the system in the portal)|





7

<!-- pág. 8 -->
### **2.8 BMU/BMS LED Event Code (EC)** 

A constant white LED refers to standby mode. White blinking means charge or discharge. 

When the battery is initiating, the LED will flash white and blue with an interval time of 0.5 seconds (normal during startup). When the LED flashes blue with an interval time of 1 second it indicates an event code.  Please start to count when the white LED begins to flash, then count how many times the white and blue LED flashes. (also refer to the manual!) **Example:** 1xwhite, 6xblue → EC 106 / 1xwhite, 11xblue → EC 111 / 3xwhite, 3xblue → EC 303 **Note: every LVS Module has its own BMS. The Event Code of the BMS will therefore be shown in the LED of the module.** 



Most errors are caused by a faulty communication line, an incorrect app configuration or the missing restart after the app-configuration. Please go in detail through: **Section 2.3 & 2.4** 

**Note: if the system is not correctly configured with the app, the event code (EC) might be misleading.** 

|**EC**<br>**BMU**|**EC**<br>**BMS**|**Measure**|
|---|---|---|
|No LED|/|See**section 2.1**.|
|/|No LED|See**section 2.2.**|
|Abnormal<br>LED<br>flickering|/|See**section 2.1**<br>Module Exclusion Method (**see section 2.11)**: Check if the system works when removing the<br>suspected module|
|EC 101|/|Initialisation Failure.|
|||- Make sure the app-configuration has been completed correctly (especially module quantity!)<br>- Restart the system properly (see**step 5 in section 1**)|
|||If the problem remains:<br>-<br>Download all data with BCP (especially the historical data)**(section 2.9)**<br>-<br>replace BMU, if available|





8

<!-- pág. 9 -->
EC 102 / Incorrect module quantity / Module not detected. EC 105 - See **section 2.4** . - Make sure the app-configuration has been completed correctly (especially module quantity!). - Check the terminal resistor. The terminal resistor (120 Ω at pin 5+6) is responsible for a clean communication between BMS and BMU. In rare cases it can be damaged and can disturb the signal. In these rare cases it is recommended to remove the terminal resistor. - replace communication cable between Battery and BMU - Restart the system properly (see **step 5 in section 1** ) - Module Exclusion Method ( **see section 2.11)** : Check if the system works when removing the suspected module 

- If problem remains: - Download all data with BCP (especially the historical data) **(section 2.9)** 

- - replace BMU, if available 

EC 103 EC 108 PreCharge Fault. 

- Check the DC cabling and make sure that the Minimum Configuration is met. 

- Check the voltage of the batteries with BCP according to **section 2.9** 

- Restart the system properly (see **step 5 in section 1** ) - Module Exclusion Method ( **see section 2.11)** : Check if the system works when removing the suspected module If problem remains: - Download all data with BCP (especially the historical and the cell data) **(section 2.9)** 

- - provide the serialnumber and voltage of the faulty module (see checklist on last page) 

EC 104 EC 101 Short circuit / DC reverse connection. - Check DC cabling (is there any short circuit? Is the fuse between battery and inverter closed?) - Disconnect the battery system from the inverter and restart the battery system alone (battery isolated), to evaluate if the error is being caused externally (i.e. short circuit in inverter or MPPT). If the Event Code remains, the error might be in the battery. If the Event Code has changed, there might be an error in the inverter side. - Module Exclusion Method ( **see section 2.11)** : Check if the system works when removing the suspected module 

If problem remains: 

- Download all data with BCP (especially the historical and the cell data) **(section 2.9)** - provide the serialnumber and voltage of the faulty module (see checklist on last page) EC 104 EC 102 One of the BMS (modules) reports an event message. up to EC113 - Check the voltage of the batteries according to **section 2.10** (All other If problem remains: than 101) - Download all data with BCP (especially the historical and the cell data) **(section 2.9)** - provide the serialnumber and voltage of the faulty module (see checklist on last page) EC 106 / No communication with Inverter. 

- Make sure the inverter is on, configured and working correctly. 

- Check according to **section 2.5** 



9

<!-- pág. 10 -->
### **2.9 Be Connect Plus (BCP)** 

Be Connect Plus is a Windows-PC tool. With Be Connect Plus (BCP) you can: 

   - read the battery information, 

   - configure the battery system 

   - update BMU & BMS firmware 

- Export / download battery logs (From BMU and all BMS) 

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the Tool on www.bydbatterybox.com / www.eft-systems.de / www.alpspower.com.au** . 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual inside of program ZIP archive). 

Note: You need a computer with Windows that will be connected to the battery Wifi. Login as Installer to Be Connect Plus, the password is the same as for WiFi: BYDB-Box 





10

<!-- pág. 11 -->
### **2.10 Voltage measurement and undervoltage** 

You can see the voltages (cells and module) in the app or BCP Tool ( **section 2.9** ). Alternatively you can measure the module voltage manually according to the description below. Make sure not to create a short circuit! 

To check the voltage on the PDU, the Modules have to be ON and the BMU has to be connected with the PDU! (LEDs on Modules and BMU have to be ON). Please measure at **P+** and **P-** according to the picture below: 



The voltage measured on the PDU is the average voltage of all modules in the tower and should be around 50V. **NOTE: the PDU output voltage will only be correct if the battery has been configured correctly via app and then restarted. Without correct app configuration, the PDU output voltage will be wrong!** 

If the PDU output voltage is too low despite correct configuration, please measure the voltage of each LVS module individually. To do this, remove the right side panel of the battery module (the side with the LED). Measure the voltage at the points marked "BAT +" and "BAT-" below. The voltage should be about 50 V.  Attention: Be careful not to cause a short circuit! 









11

<!-- pág. 12 -->
#### **Undervoltage** 

A Module in which one of the 16 cells has a voltage of <1.5 V is in undervoltage (check with BCP ( **section 2.9** ) / BC if possible). 

- LVS Modules with >45 V should be fine and you can go on to check other points according to this service guideline. - If the module voltage is <40V but the single cell voltage is >1.5V, the battery needs to be charged quickly while avoiding any further discharge. Therefore, shut down the system and search for the problem according to the guideline, while the battery is completely switched off. Also check on the inverter side why the force charge doesn’t work. Do not turn on the battery before making sure the inverter is able to charge the battery. 

- If only one module is in undervoltage: remove that module and try commissioning without it (if the remaining modules still comply with the Compatible Inverter List). Otherwise, make sure to avoid further overdischarge. (Turn off the system completely) 

- If one, or all modules are in undervoltage: Contact the service as stated below and make sure to avoid any further discharge of the battery (Turn off the system completely) 

When contacting the service, make sure to fill the service checklist completely and add the following information: 

- Serial Numbers (of the BMU and all affected modules) 

- Individual module voltages of all modules (related to Serialnumber) 

- If possible: Logs from the battery using BCP ( **section 2.9** ) and Screenshots showing the cell voltages 

- Initial Firmware (FW) Version of the Battery when the UV happened (BMU and BMS) 

- Detailed description how and why the system reached Undervoltage if known. Information when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the battery status when the battery was left (on / off / LED). 

   - Inverter Model, Serial Number and Inverter Logs 

- Access to Inverter portal (add info@eft-systems.de and tell us the name of the system in the portal) 

### **2.11 Module Exclusion Method (Identifying a faulty module)** 

- Normally a faulty module can be identified with the Be Connect Plus Program or by the LED Code in the Battery Module. In this case, remove the Module with the Event Code from the system, and commission the remaining system (if it still complies with the minimum configuration list) and check if it runs properly. If the problem remains, please also check the module above the one with the Event Code. 

Otherwise, try the LVS Modules one by one, or by adding Modules one by one into the tower and always check if the system can work properly to identify a possibly faulty module. 

**Important: The module quantity must be adjusted in the app whenever the number of modules has been changed! Don’t forget to perform a proper restart after a new configuration!** 

1. Switch off the battery (Press button on BMU for 5 seconds until all batteries switch off. Note: if the modules do not turn off then, something is wrong in the PDU<>BMU connection. Replace comm cable and try again.) 

2. Turn on the Battery (button on topmost battery) 



12

<!-- pág. 13 -->
## 3. SERVICE TASKS 

Please go through the general steps beforehand, see chapter 1. 

### **3.1 BMU Replacement** 

**Have you detected a faulty BMU?:** 

After replacing the BMU, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.2 PDU Replacement** 

After replacing the PDU, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.3 LVS Module Replacement** 

After replacing the module, please do not forget to re-do the configuration and firmware-update with the app or BCP. 



13

<!-- pág. 14 -->
|**BYD Battery-Box Premium LVS Service Checklist - V1.1 EN**|
|---|



|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Box are only<br>allowed by professional and qualified electricians. Improper handling can cause danger and damage. This document does<br>not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the information.<br>.|
|---|
|**1.**<br>**GENERAL STEPS**<br>Please carefully check**all**„General Steps“ from page 3 of the Service Guideline and confirm this in the boxes below|
|1.1 Configuration<br>1.4 App Configuration|
|1.2 Correct external cabling<br>1.5 Proper Restart|
|1.3 Latest Firmware<br>1.6 Correct Operation|
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the**error related**Analysis from Chapter 2 of the Service Guideline that you checked, and collect all the<br>information related to those Sections|
|2.1 BMU does not turn on / LED is off or flickering abnormally<br>2.5 Communication issue with<br>It / BMU EC106<br>2.9 Be Connect Plus (BCP)|
|2.2 Modules do not show any reaction / No LED on module<br>i<br>nverer<br>2.6 SOC & charging logic<br>2.10 Voltage measurement<br>and undervoltage|
|2.3 Problem with the FW Update / App Configuration / WiFi<br>2.7 Unexpected shutdown<br>2.11 Identifying a faulty|
|2.4 Incorrect output voltage / No BMS Data / BMU EC102<br>2.8 BMU/BMS LED Event Code (EC)<br>module / Module<br>Exclusion Method|
|**3.**<br>**SERVICE INFORMATION**|
|Please fill all available information in below table. Some information like the Serial Number of the BCU is mandatory to receive service.|
|**•**<br>**Service Ticket Number or System ID:**|
|**•**<br>**Installer / Delivery Address / Contact:**|
|Company<br>ZIP / City|
|Contact Person<br>Phone|
|Street / Nr.<br>Email|
|**•**<br>**System Information**|
|Battery Configuration (e.g. 2 x LVS 12.0 /...))<br>BMU Firmware|
|BMU Serial Number<br>BMS Firmware|
|BMU Connected to Internet<br>Inverter Firmware<br>Yes<br>No|
|Inverter Brand + Model<br>System Name on<br>Inverter Portal|
|Inverter Serial Number<br>( Provide access for: info@eft-systems.de )|
|Commissioning Date|
|**•**<br>**Service Information**|
|BMU EventCode (EC)<br>Inverter Error Code|
|BMS EventCode(s) and related Module Serial Number(s)|
|Was the battery charging / discharging before (was the system working normally before?)<br>Yes<br>No|
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see chapter 2.9)|
|Description of<br>the Problem<br>Please provide any additional information that is necessary or could help in the analysis of the service case (e.g. serial number of a<br>wrong module, video of a special behaviour; pictures; app screenshots; module voltages... )|
|By contacting us you confirm, that a qualified person has done the necessary control and collected all available information above.<br>Service Contact:<br>Europe: EFT-Systems GmbH<br>Australia:  Alps Power Pty Ltd<br>www.eft-systems.de<br>www.alpspower.com.au|
|<br><br>service@eft-systems.de<br>service@alpspower.com.au<br>+49 9352 8523999<br>+34 9106 02267 (ES)<br>+61 02 8005 6688|



|By contacting us you confirm, that a qualified person has|i   i   done the necessary control and collected all available information above.|
|---|---|
|Service Contact:<br>Europe: EFT-Systems GmbH<br>www.eft-systems.de<br>service@eft-systems.de<br>+49 9352 8523999<br> <br>+44 2037 695998 (UK)|Australia:  Alps Power Pty Ltd<br>www.alpspower.com.au<br>service@alpspower.com.au<br>+34 9106 02267 (ES)<br>+61 02 8005 6688<br>+39 0287 368364 (IT)|
|For Europe only: Register Ticket directly in the Online Serv|ice Center: https://support.eft-systems.de/|
