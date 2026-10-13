# Battery-Box Premium LVS Lite — Guía de servicio y checklist

- **Producto:** Battery-Box Premium LVS Lite (LVS Lite)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.1 / 2022-03-03
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/2022-3-3_BYD_Battery-Box_Premium_LVS%20Lite_Service_Guideline_and_Checklist_EN_V1.1-62393b8c2b0ee.pdf
- **SHA-256 del PDF:** 2383492cfae4d6c47d791de01b76aa989cc9e91a6ff9f25db06d7cc09e4c9dfa
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/2022-3-3_BYD_Battery-Box_Premium_LVS Lite_Service_Guideline_and_Checklist_EN_V1.1-62393b8c2b0ee.pdf
- **Conversión:** pymupdf4llm 1.28.2, 14 págs.

> ⚠ Este documento tiene 1 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium LVS Lite Service Guideline and Checklist** Version 1.1 

Valid for Premium LVS Lite 4.0 / 8.0 / 12.0 / 16.0 



LVS Lite 16.0 (4 Modules + PDU) 



BMU (1 x per System) 



**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** 

This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com</u> / <u>www.alpspower.com.au .</u> 

Subject to technical modifications no responsibility is accepted for the accuracy of this information. Attention: Improper handling can cause danger and damage.

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
|3.3<br>LVS Lite<br>Module<br>Replacement|13|
|**SERVICE CHECKLIST AND CONTACT INFORMATION**|**14**|





2

<!-- pág. 3 -->
## 1. GENERAL STEPS 

**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com** Please proceed first with the installation steps by: 

> ⚠ REVISAR TABLA — pág. 3: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Descript**|**ion**||
|---|---|---|---|---|
|1|Configuration|Check<br>if<br>minimum<br>Make<br>sur|the<br>config<br><br>Configur<br>e<br>the<br>inve|**www.bydbatterybox.com**<br>iuration<br>is<br>correct.<br>Refer<br>to<br>latest<br>“BYD<br>Battery-Box<br>Premium<br>LVS Lite<br>iation<br>List”<br>(V1.0<br>or<br>above)<br>available<br>at:<br>rter<br>is<br>configured<br>correctly.|
|2|Correct external<br>cabling|1.<br>2.<br>3.<br>4.<br>5.<br>Notes<br>ab<br>-<br>DC<br>cab<br>a<br>necess<br>the<br>batte|Commu<br>a.<br>b.<br>c.<br>Groundi<br>a.<br>b.<br>Ethernet<br>Correct<br><br>DC-Port<br>piece<br>re<br>out<br>DC<br>co<br>le<br>cross<br>s<br>ary<br>cable<br>ry<br>and<br>the|nication<br>to<br>inverter<br>Depending<br>on<br>the<br>choice<br>of<br>inverter<br>the<br>cable<br>between<br>the<br>BMU<br>port<br>and<br>the<br>inverter<br>must<br>be<br>specially<br>made.<br>Please<br>check<br>the<br>specifications<br>in<br>the<br>installation<br>manual.<br>Recommended<br>CAT5<br>or<br>higher;<br>Check<br>the<br>cables<br>and<br>replace<br>them<br>if<br>necessary<br>ng<br>Battery-Box<br>connected<br>directly<br>to<br>the<br>ground-bus<br>of<br>the<br>house.<br>The<br>battery<br>must<br>not<br>be<br>earthed<br>via<br>the<br>inverter!<br>Otherwise,<br>communication<br>problems<br>are<br>possible.<br>-Cable<br>for<br>Internet<br>(**strongly**<br>**recommended!**)<br>parallel<br>connection<br>cabling<br>if<br>applicable<br>s<br>-<br>Make<br>sure<br>that<br>**+**<br>and<br>**-**<br>are<br>properly<br>connected.<br>(Male<br>DC<br>Connector<br>quired)<br>nnection:<br>ection:<br>depends<br>on<br>the<br>respective<br>configuration.<br>BYD<br>does<br>not<br>specify<br>cross-section<br>herePlease<br>pay<br>attention<br>to<br>the<br>power<br>and<br>current<br>of<br><br>inverter,<br>as<br>well<br>as<br>the<br>local<br>rules.|
|3|Latest Firmware|Always u<br>Note: If    i|pdate the <br>not stated  i|**newest Firmware**! (with using the latest App Version)<br>otherwise, wifi password is BYDB-Box|
|4|App Configuration|To comp    i<br>or PC to|lete the c  i<br>ol “Be Con|ommissioning, the configuration of the battery via  “Be Connect” App<br>nect Plus” (BCP) is**mandatory**! Please restart battery afterwards.|
|5|Proper Restart|Switch o<br>1.<br>Switch o<br>1.<br>2.<br>3.|ff:<br>Press B<br>sure all<br>turn off<br>comm c<br>n (mind th<br>Switch o<br>Switch o<br>seconds<br>Turn on|MU LED Button for 5 seconds. All modules should be off then. Make<br>LEDs of the battery are completely off. Note: if the modules do not<br>then, something is wrong in the PDU<>BMU connection. Replace<br>able and try again.<br>e sequence!)<br>n the fuse between Inverter and Battery (if there is any)<br>n the Battery (press LED Button on the topmost module for 3<br>. All modules should become active then)<br>the inverter|
|6|Checking the correct<br>operation|The syst<br>- Inverte<br>- System<br>Note: **If**<br>**leave th**|em runs p<br>r displays<br>charges /<br>**you can n**<br>**e site and**|roperly if:<br>battery SOC correctly<br>discharges<br>**ot complete the commissioning, then turn off the battery before you**<br>**make sure all LEDs are off to avoid a discharge of the battery.**|





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
|9|Voltage measurement on<br>pin 7&8|Measure<br>the<br>voltage<br>of<br>PIN<br>7<br>&<br>8<br>while<br>the<br>other<br>side<br>of<br>the<br>cable<br>is<br>connected<br>to<br>the<br>IN<br>port<br>of<br>the<br>Battery-Box<br>and<br>while<br>the<br>Battery-Box<br>is<br>powered<br>on.<br>Voltage<br>should<br>be<br>around<br>50V.<br>If<br>yes:<br>try<br>another<br>BMU<br>(if<br>available).<br>If<br>no:<br>check<br>another<br>cable<br>or<br>try<br>another<br>LVS Lite<br>if<br>multiple<br>batteries<br>are<br>installed<br>in<br>the<br>system.|
|10|Only LED faulty?|In some rare cases, the LED of the BMU is faulty. To check that: check if there is a<br>WIFI access point of the Battery-Box and check if there are internal LEDs inside the<br>BMU. If so, only the external LED is inactive and a commissioning could still work.|
|11|Voltage measurement|Check voltage of battery. See**Section 2.10**|
|12|Module Exclusion Method|Check if system works when removing the suspected module. See**section 2.11**|
|13|BMU exchange|If problem remains:<br>Test another BMU, if available.|



### **2.2 Modules do not show any reaction / No LED on module** 

LEDs of some module do not light up,although button on topmost module is pressed for 3 seconds.. 

|**No.**|**Name**|**Description**|
|---|---|---|
|14|Swap module position|Note: If top modules have active LED but bottom modules don’t, it indicates a<br>connection issue between modules. Example:<br>_LVS Lite16.0_<br>_(4_<br>_modules)._<br>_Module_<br>_1&2_<br>_have_<br>_LED,_<br>_module_<br>_3&4_<br>_don’t_<br>_have_<br>_LED.Issue_<br>_is_<br>_in_<br>_the_<br>_connection_<br>_between_<br>_module_<br>_2_<br>_&3._<br>_Problem_<br>_likely_<br>_to_<br>_be module_<br>_2_<br>_(less_<br>_likely:_<br>_module_<br>_3)._<br>-<br>Remove<br>the<br>affected<br>module<br>and<br>check<br>whether<br>problem<br>disappears.<br>If<br>not,<br>check<br>the<br>module<br>below.<br>-<br>Rearrange<br>the<br>modules<br>in<br>the<br>tower.<br>Note:<br>The<br>affected<br>module<br>often<br>works<br>without<br>restrictions<br>at<br>the<br>lowest<br>module<br>position<br>of<br>the<br>tower.|





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
|18|Correct App and<br>Firmware|Make<br>sure<br>to<br>have<br>the<br>latest<br>App<br>version<br>(>2.1.0)<br>and<br>Battery<br>Firmware<br>(download<br>inside<br>the<br>App)<br>on<br>your<br>mobile<br>device<br>before<br>connecting<br>the<br>app<br>with<br>battery<br>WiFi.<br>If<br>the<br>App<br>cannot<br>be<br>installed,<br>or<br>other<br>general<br>Problems<br>occur<br>with<br>the<br>App:<br>-<br>Try<br>with<br>a<br>different<br>mobile<br>device<br>(For<br>Android:<br>min<br>Android<br>version<br>requirement<br>is<br>4.4.<br>)<br>-<br>Try<br>with<br>PC<br>Tool<br>BCP<br>(**section**<br>**2.9**)<br>-<br>Note:<br>If<br>the<br>WiFi<br>connection<br>is<br>not<br>stable<br>you<br>might<br>remove<br>the<br>lan<br>cable<br>during<br>the<br>configuration.<br>Once<br>the<br>battery<br>has<br>been<br>configured<br>correctly<br>you<br>can<br>connect<br>it<br>again<br>to<br>the<br>Internet.|
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
|23|Battery correctly<br>configured?|Please<br>check<br>if<br>the<br>App<br>configuration<br>was<br>successful<br>and<br>the<br>Firmware<br>is<br>the<br>most<br>recent<br>one.<br>If<br>there<br>are<br>problems,<br>please<br>refer<br>to<br>**Section**<br>**2.3**<br>**Note:**<br>**It**<br>**is**<br>**important**<br>**to**<br>**select**<br>**the**<br>**correct**<br>**module**<br>**quantity.**<br>**Else,**<br>**the**<br>**PDU**<br>**output**<br>**voltage**<br>**will**<br>**be**<br>**wrong!**<br>The<br>quantity<br>you<br>need<br>to<br>select<br>refers<br>to<br>the<br>overall<br>quantity<br>of<br>LVS Lite 4.0<br>modules<br>and<br>not<br>to<br>the<br>quantity<br>of<br>towers.<br>Note:<br>Don’t<br>forget<br>to<br>**properly**<br>**restart**<br>**system**<br>after<br>changing<br>configuration!|
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
|30|Configuration|Check<br>if<br>the<br>configuration<br>is<br>correct.<br>Refer<br>to<br>latest<br>“BYD<br>Battery-Box<br>Premium<br>**www.bydbatterybox.com**<br>LVS Lite<br>Minimum<br>Configuration<br>List”<br>(V1.0<br>or<br>above)<br>available<br>at:<br>Make<br>sure<br>the<br>inverter<br>is<br>configured<br>and<br>working<br>correctly.|
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

|**No**|**Name**|**Description**|
|---|---|---|
|36|Inverter<br>Communication|The battery only works with an compatible external inverter. If for whatever reason the<br>communication between battery and inverter is lost, the battery will shut down itself within<br>30minutes. Therefore, check which one did shut down first (battery or inverter) and check<br>if inverter is properly detecting battery (e.g showing correct SOC or temperature). If<br>problem remains, check according to**section 2.5**.|
|37|Battery Logs / History<br>Data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log files in order to identify the<br>root cause.  See**section 2.9**for details.|
|38|Inverter Warning &<br>Monitoring|Unexpected<br>Shutdown<br>can<br>be<br>caused<br>by<br>overall<br>system<br>settings.<br>Therefore,<br>it<br>is<br>necessary<br>to<br>evaluate<br>inverter<br>data<br>as<br>well.<br>-<br>Which<br>error<br>message<br>are<br>shown<br>in<br>inverter<br>-<br>Please<br>provide<br>access<br>to<br>Inverter<br>portal|





7

<!-- pág. 8 -->
### **2.8 BMU/BMS LED Event Code (EC)** 

A constant white LED refers to standby mode. White blinking means charge or discharge. 

When the battery is initiating, the LED will flash white and blue with an interval time of 0.5 seconds (normal during startup). When the LED flashes blue with an interval time of 1 second it indicates an event code. Please start to count when the white 

LED begins to flash, then count how many times the white and blue LED flashes. (also refer to the manual!) 

**Example:** 1xwhite, 6xblue → EC 106 / 1xwhite, 11xblue → EC 111 / 3xwhite, 3xblue → EC 303 

**Note: every LVS Lite Module has its own BMS. The Event Code of the BMS will therefore be shown in the LED of the module.** 

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

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the Tool on www.bydbatterybox.com / www.alpspower.com.au** . 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual inside of program ZIP archive). 

Note: You need a computer with Windows that will be connected to the battery Wifi. 

Login as Installer to Be Connect Plus, the password is the same as for WiFi: BYDB-Box 





10

<!-- pág. 11 -->
### **2.10 Voltage measurement and undervoltage** 

You can see the voltages (cells and module) in the app or BCP Tool ( **section 2.9** ). Alternatively you can measure the module voltage manually according to the description below. Make sure not to create a short circuit! 

To check the voltage on the PDU, the Modules have to be ON and the BMU has to be connected with the PDU! (LEDs on Modules and BMU have to be ON). Please measure at **P+** and **P-** according to the picture below: 



The voltage measured on the PDU is the average voltage of all modules in the tower and should be around 50V. **NOTE: the PDU output voltage will only be correct if the battery has been configured correctly via app and then restarted. Without correct app configuration, the PDU output voltage will be wrong!** 

If the PDU output voltage is too low despite correct configuration, please measure the voltage of each LVS Lite module individually. To do this, remove the right side panel of the battery module (the side with the LED). Measure the voltage at the points marked "BAT +" and "BAT-" below. The voltage should be about 50 V.  Attention: Be careful not to cause a short circuit! 









11

<!-- pág. 12 -->
#### **Undervoltage** 

A Module in which one of the 16 cells has a voltage of <1.5 V is in undervoltage (check with BCP ( **section 2.9** ) / BC if possible). 

- LVS Lite Modules with >45 V should be fine and you can go on to check other points according to this service guideline. - If the module voltage is <40V but the single cell voltage is >1.5V, the battery needs to be charged quickly while avoiding any further discharge. Therefore, shut down the system and search for the problem according to the guideline, while the battery is completely switched off. Also check on the inverter side why the force charge doesn’t work. Do not turn on the battery before making sure the inverter is able to charge the battery. 

- If only one module is in undervoltage: remove that module and try commissioning without it (if the remaining modules still 

- comply with the Minimum Configuration List). Otherwise, make sure to avoid further overdischarge. (Turn off the system completely) 

- If one, or all modules are in undervoltage: Contact the service as stated below and make sure to avoid any further discharge of 

- the battery (Turn off the system completely) 

- When contacting the service, make sure to fill the service checklist completely and add the following information: 

   - Serial Numbers (of the BMU and all affected modules) 

   - Individual module voltages of all modules (related to Serialnumber) 

   - If possible: Logs from the battery using BCP ( **section 2.9** ) and Screenshots showing the cell voltages 

   - Initial Firmware (FW) Version of the Battery when the UV happened (BMU and BMS) 

   - Detailed description how and why the system reached Undervoltage if known. Information when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the battery status when the battery was left (on / 

      - off / LED). 

      - Inverter Model, Serial Number and Inverter Logs 

      - Access to Inverter portal 

### **2.11 Module Exclusion Method (Identifying a faulty module)** 

- Normally a faulty module can be identified with the Be Connect Plus Program or by the LED Code in the Battery Module. In this case, remove the Module with the Event Code from the system, and commission the remaining system (if it still complies with the minimum configuration list) and check if it runs properly. If the problem remains, please also check the module above the one with the Event Code. 

- Otherwise, try the LVS Lite Modules one by one, or by adding Modules one by one into the tower and 

- always check if the system can work properly to identify a possibly faulty module. **Important: The** **<u>module quantity must be adjusted in the app</u> whenever the number of modules has been changed! Don’t forget to perform a** **<u>proper restart</u> after a new configuration!** 

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

### **3.3 LVS Lite Module Replacement** 

After replacing the module, please do not forget to re-do the configuration and firmware-update with the app or BCP. 



13

<!-- pág. 14 -->
|**BYD Battery-Box Premium LVS Lite Service Checklist - V1.1 EN**|
|---|



|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Box are only<br>allowed by professional and qualified electricians. Improper handling can cause danger and damage. This document does<br>not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the information.<br>.|
|---|
|**1.**<br>**GENERAL STEPS**<br>Please carefully check**all**„General Steps“ from page 3 of the Service Guideline and confirm this in the boxes below|
|1.1 Configuration<br>1.4 App Configuration|
|1.2 Correct external cabling<br>1.5 Proper Restart|
|1.3 Latest Firmware<br>1.6 Correct Operation|
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the**error related**Analysis from Chapter 2 of the Service Guideline that you checked, and collect all the<br>information related to those Sections|
|2.1 BMU does not turn on / LED is off or flickering abnormally<br>2.5 Communication issue with<br> <br>2.9 Be Connect Plus (BCP)|
|2.2 Modules do not show any reaction / No LED on module<br>i<br>Inverter / BMU EC106<br>2.6 SOC & charging logic<br>2.10 Voltage measurement<br>and undervoltage|
|2.3 Problem with the FW Update / App Configuration / WiFi<br>2.4 Incorrect output voltage / No BMS Data / BMU EC102<br>2.7 Unexpected shutdown<br>2    d<br>2.11 Identifying a faulty<br>module / Module<br>Eli Mhd|
|.8 BMU/BMS LED Event Coe (EC)<br>xcuson eto|
|**3.**<br>Please fill all available information in below table. Some information like the Serial Number of the BCU is mandatory to receive service.<br>**SERVICE INFORMATION**|
|**•**<br>**Service Ticket Number or System ID:**|
|**•**<br>**Installer / Delivery Address / Contact:**|
|Company<br>ZIP / City|
|Contact Person<br>Phone|
|Street / Nr.<br>Email|
|**•**<br>**System Information**|
|BMU Firmware<br>Battery Configuration (e.g. LVS Lite 12.0 /...))|
|BMU Serial Number<br>BMS Firmware|
|BMU Connected to Internet<br>Inverter Firmware<br>Yes<br>No|
|Inverter Brand + Model<br>System Name on<br>Inverter Portal|
|Inverter Serial Number<br>|
|Commissioning Date|
|**•**<br>**Service Information**|
|BMU EventCode (EC)<br>Inverter Error Code|
|BMS EventCode(s) and related Module Serial Number(s)|
|Was the battery charging / discharging before (was the system working normally before?)<br>Yes<br>No|
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see chapter 2.9)|
|Description of<br>the Problem|
|Please provide any additional information that is necessary or could help in the analysis of the service case (e.g. serial number of a<br>wrong module, video of a special behaviour; pictures; app screenshots; module voltages... )|
|By contacting us you confirm, that a qualified person has done the necessary control and collected all available information above.<br>Service Contact:<br>Alps Power Pty Ltd<br>www.alpspower.com.au<br>service@alpspower.com.au|



|+61 02 8005 6688|
|---|
