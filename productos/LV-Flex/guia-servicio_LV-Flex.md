# Battery-Box LV Flex — Guía de servicio y checklist

- **Producto:** Battery-Box LV Flex (LV Flex)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** 2022-02-08
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/2022-2-8%20BYD%20Battery-Box%20LV%20FLEX%20Service%20Guideline%20and%20Checklist-620b6db6193a9.pdf
- **SHA-256 del PDF:** 9d4307a3441db4249a7e120367067249bc4f25879611ba3f1d9104b1ddd920b1
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/2022-2-8 BYD Battery-Box LV FLEX Service Guideline and Checklist-620b6db6193a9.pdf
- **Conversión:** pymupdf4llm 1.28.2, 19 págs.

> ⚠ Este documento tiene 3 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box LV Flex** 



# **Service Guideline and Checklist** 

# Version 1.0 





Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** 

This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com</u> / <u>www.eft-systems.de</u> / <u>www.alpspower.com.au. Subject to technical modifications; no responsibility is accepted for the</u> accuracy of this information. Attention: Improper handling can cause danger and damage 

1

<!-- pág. 2 -->
## Contents 

|<br>**1. GENERAL STEPS ......................................................................................................................3**|
|---|
|<br>**2. ERROR ANALYSIS.....................................................................................................................4**|
|**3. MEASUREMENT.......................................................................................................................16**|
|**4. SERVICE TASKS........................................................................................................................18**|
|4.1 BMU Replacement .......................................................................................................................18|
|4.2 LV Flex Module Replacement........................................................................................................18|



2

<!-- pág. 3 -->
### **1. GENERAL STEPS** 

Make sure to always use the latest version of this service document, available at: <u>www.bydbatterybox.com</u> 

Please proceed first with the installation steps by: 

> ⚠ REVISAR TABLA — pág. 3: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|1.1|Configuration|Make sure the inverter is configured correctly<br>Check if the configuration is correct. Refer to latest “BYD<br>BATTERY-BOX LV FLEX MINIMUM CONFIGURATION LIST ”<br>(V1.0 or above) available at: www.bydbatterybox.com|
|1.2|Correct external<br>cabling|1. Communication to inverter<br>a. Depending on the choice of inverter the cable between the<br>BMU port and the inverter must be specially made. Please<br>check the specifications in the installation manual.<br>b. Recommended CAT5, CAT5e or higher;<br>c. Check the cables and replace them if necessary<br>2. Grounding<br>a. Battery-Box connected directly to the ground-bus of the<br>house.<br>b. The battery**must not**be earthed via the inverter!<br>Otherwise, communication problems are possible.<br>3. Ethernet-Cable for Internet**(strongly recommended!**)<br>4. DC-Ports - Make sure that**+**and**-**are properly connected.<br>5. Correctparallel connection cabling if applicable<br>**Notes about DC connection:**<br>• Conductor cross-section: 16mm<sup>2</sup>|
|||• Maximum cable length:   20m.|
|1.3|Latest Firmware|Always install / update the newest Firmware!<br>Note: If not stated otherwise, Wi-Fi password is BYDB-Box|
|1.4|App<br>Configuration|To complete the commissioning, the configuration of the battery<br>via mobile device app “Be Connect 2.0” (BC APP) or PC app “Be<br>Connect Plus” (BCP) is**mandatory**!|
|1.5|Restart|After app configuration, please perform a proper restart of the<br>system byswitchingoff the batterycorrectly (press LED Button on|



3

<!-- pág. 4 -->
BMU for 5 sec). Make sure all LEDs of the battery are completely off. 



Figure 1 power off BMU 

Then follow the correct switch on procedure (see step 1.6) 

- 1.6 Switch on Correct switch on procedure is important for a correct operation 

- procedure 1. Turn on the switch between the inverter and battery if there is any; 

      2. Switch on the battery system; (press LED Button on the LV FLEX module address 1 for 3 seconds; LV FLEX module address 1 is the one connecting directly with BMU). 

      3. Switch on the inverter. 

- 1.7 Checking the The system runs properly if: 

   - correct operation 

- -Inverter displays battery SOC correctly 

- -System charges / discharges 

Note: **If you cannot complete the commissioning, then turn off the battery before you leave the site and make sure all LEDs are off to avoid a discharge of the battery.** 

### **2. ERROR ANALYSIS** 

Please refer to the general steps before proceeding, see chapter 1. 

#### **2.1 BMU shows  no reaction / No  LED** 

LED of BMU does not light up, although the battery is ON. 

|**No.**|**Name**|**Description**|
|---|---|---|
|2.1.1|Check correct|Make sure that the correct data cable port has been used at the|
||cable port|BMU (“BMS” port. Do not mix with “inverter” or “Ethernet” port).|
|2.1.2|Replace Comm|Try a completely new communication cable between battery and|
||Cable|BMU.|
|||Note: Sometimes it might be necessary to unplug the|
|||communication cable and plug it again while batteries are<br>switched on.|



4

<!-- pág. 5 -->
|2.1.3|Voltage<br>measurement|Battery voltage should be around 50V, see Section 3.1 for voltage<br>measurement.|
|---|---|---|
|||If yes: try another BMU (if available).<br>If no: check another cable or|
|||Try another LV FLEX if multiple batteries are installed in the<br>system.|
|2.1.4|Only LED faulty?|In some rare cases, the LED of the BMU is faulty. To check that:<br>check if there is a Wi-Fi access point of the Battery-Box. If so, only<br>the external LED is inactive and a commissioning could still work.|
|2.1.5|Module<br>Exclusion<br>Method|Check if system works when bypassing the suspected module.<br>See section 3.2.|
|2.1.6|BMU exchange|If problem remains, try another BMU, if available.|



#### **2.2 Some modules do not show any reaction / No LED on module** 

LEDs of some modules do not light up, although button on topmost module is pressed for 3 seconds. 

|**No.**|**Name**|**Description**|
|---|---|---|
|2.2.1|Comm cable|Try to unplug the comm cable between the first affected LV Flex<br>module and the one above it, and plug it again.<br>Or try a completely new comm cable between the first affected LV<br>Flex module and the one above it|
|2.2.2|Only LED faulty?|In some rare cases, the LED of the module is faulty. To check<br>that: use BC APP or BCP to check whether the BMS information<br>of this module could be detected.|
|2.2.3|Switch on the<br>suspected<br>module|Press the LED button for three seconds to power one the<br>suspected module. If the LED cannot be lighted up, the battery<br>module is faulty.|
|2.2.4|Voltage<br>measurement|Check voltage of the affected module(s). See Section 3.1. Voltage<br>should be around 50V. If voltage is lower than 38V, it might be<br>unable to power on.<br>Try to charge it as soon as possible if a charger is available, or<br>replace it.|



5

<!-- pág. 6 -->
2.2.5 Module Module Exclusion Method (see section 3.2): Check if the system Exclusion works when bypassing the suspected module. Remove it if Method bypassing works. 

#### **2.3 Problem with the Firmware Update / App Configuration** 

The Battery Management consists of two components: the BMU and the BMS. The Firmware Update from BC APP will update the BMU, which will then update the BMS. **The BMS update can take up to 30 minutes until the firmware is updated on the BMS.** 

> ⚠ REVISAR TABLA — pág. 6: 48% de celdas vacías (posibles celdas combinadas)
|**No.**|**Name**|**Description**|
|---|---|---|
|2.3.1|Correct app and<br>Firmware|Make sure to have the latest BC APP (>2.1.0) and Battery<br>Firmware (download inside BC APP) on your mobile device before<br>connecting BC APP with the battery Wi-Fi.|
|||If BC APP cannot be installed, or other general problems occur<br>with BC APP:|
|||- Try with a different mobile device with version|
|||Android:  5.0 or above,|
|||IOS:      11 or above.|
|||- Try with BCP (section 2.9)|



2.3.2 Wi-Fi cannot be For BMU version V1.21 (or above), the Battery Wi-Fi turns off 5 found / hours after the start of the Battery. To reactivate the Wi-Fi, press the LED button about 1 second or restart the system. Wi-Fi unstable To reset the Wi-Fi module, press the LED button three times (each time around one second) within 6 seconds. 

If problem remains: 

- **remove the LAN cable during the configuration.** Once the 

- Battery has been configured correctly you can connect it again to the Internet. 

- check whether other mobile devices are connected the same WiFi 

- try another mobile device 

- Power on the system, wait for 5 minutes and try again. 

6

<!-- pág. 7 -->
2.3.3 App reports: Battery-Box is busy (e.g. the battery could be updating the “ The battery firmware). Please wait 10 minutes and try again. system may be busy, please try again later ” 

- 2.3.4 Proper restart Note: Whenever the configuration via BC APP / BCP is changed, a restart of the battery is necessary to make sure that all changes come into effect. 

   1. Switch off the battery (Press button on BMU for 5 seconds until all batteries switch off. Note: if the modules do not turn off then, something is wrong in the top LV Flex module<>BMU connection. Replace comm cable and try again.) 

   2. Turn on the Battery (button on topmost battery) 

- 2.3.5 Close and If BC APP does not react anymore after some minutes loading restart BC APP during the update process, close (close the program completely) and restart BC APP. Or try with BCP (section 2.9) 

- 2.3.6 BMS Version not BC APP will only update the BMU. The BMU will update the BMS, updated which can take up to 30 minutes. 

If the BMS Version is not updated after 30min with stable inverter communication, follow the below Process: 

1. Update Firmware through BC APP again 

2. Restart the system 

a. Switch off the Inverter first, then switch off the battery second (Press LED for 5 seconds) 

b. Wait for 2 Minutes 

c. Turn on the Battery first, then turn on the inverter second 

3. Wait for 30 Minutes 

4. Check BMS Firmware Version again with App. If Version is still wrong, do the update process again (if possible with another mobile device). 

5. Note: if Voltage of Battery is not shown in BC APP, the update will not be transferred to BMS. Make sure the BMU recognizes BMS properly. 

7

<!-- pág. 8 -->
#### **2.4 Incorrect output voltage / No BMS Data** 

|**No.**|**Name**|**Description**|
|---|---|---|
|2.4.1|App<br>Configuration<br>and Firmware|Please check if BC APP configuration was successful and the<br>Firmware is the most recent one. If there are problems, please<br>refer to Section 2.3<br>Note: It is important to select the correct module quantity. The<br>quantity you need to select refers to the overall quantity of LV Flex<br>modules and not to the quantity of towers. For example, if you<br>have 2 towers connected in parallel, and 4 modules in each tower,<br>you need to select the module quantity of“8”in the BC APP /<br>BCP.<br>Note: Don`t forget to properly restart system after changing<br>configuration!|
|2.4.2|Proper restart|Note: Whenever the configuration via BC APP / BCP is changed,<br>a restart of the battery is necessary to make sure that all changes<br>come into effect.<br>1. Turn off the Inverter<br>2. Turn off the battery (Press button on BMU for 5 seconds until all<br>batteries switch off. All LEDs should be off)<br>3. Turn off the switch between battery and inverter(if available )<br>4. Wait for 2 Minutes<br>5. Turn on the switch between battery and inverter(if available )<br>6. Turn on the Battery (button on battery connected to BMU) and<br>then<br>7. Turn on inverter second|
|2.4.3|BMU<>BMS<br>Communication|Make sure that the comm cable is connected to the right port of<br>BMU (the one labeled as "BMS"). Replace comm cable between<br>BMU and battery.|
|2.4.4|Comm cable<br>between<br>modules|Try to unplug the comm cable between the first affected LV Flex<br>module and the one above it, and plug it again.<br>Or try a completely new comm cable between the first affected LV<br>Flex module and the one above it|



8

<!-- pág. 9 -->
|2.4.5|Check terminal<br>resistor|Make sure that the terminal resistor is connected to the OUT port<br>(Terminal resistor properties: 120Ωresistor between pin 5 and 6)|
|---|---|---|
|||If it was connected already, then please remove it and try without<br>it to rule out a faulty terminal resistor. Don't forget to properly<br>restart system afterwards.|
|2.4.6|Module<br>Exclusion<br>Method|Refer to Section 3.2 to identify a potentially faulty module.|
|2.4.7|Further checking|If problem remains:<br>- Upload logs with BC APP (section 2.10) or download all data<br>with BCP ( section 2.9)<br>- Check the inverter|
|||- Test another BMU, if available|



#### **2.5 Communication problem with Inverter** 

|**No.**|**Name**|**Description**|
|---|---|---|
|2.5.1|Configuration|Check if the inverter is correctly selected when configuration.<br>Refer to latest “BYD BATTERY-BOX LV FLEX MINIMUM<br>CONFIGURATION LIST” (V1.0 or above) available at:<br>www.bydbatterybox.com<br>Make sure the inverter is configured correctly|
|2.5.2|Inverter settings|Make sure to configure the battery correctly on the inverter<br>interface. Refer to inverter manual for details.|
|2.5.3|Comm cable|Confirm PIN / Cable Configuration for the specific inverter model<br>(see manual)<br>Replace the communication cable (min. CAT5!)|
|2.5.4|Check inverter<br>status|Check whether the inverter has been successfully powered on by<br>the battery.<br>If the inverter has not been powered on, check whether the battery<br>voltage is within the inverter operating range or not. If the battery<br>voltage is lower than that, refer to section 3.3.|



9

<!-- pág. 10 -->
- 2.5.5 Further If problem remains: checking -  Upload logs with BC APP (section 2.10) or download all data with BCP (section 2.9). -  Check the inverter -  Try by replacing the BMU, if available 

#### **2.6 SOC & charging logic** 

|**No.**|**Name**|**Description**|
|---|---|---|
|2.6.1|SOC jumps|The SOC of an LFP battery cannot be measured. It is a calculated<br>value. In general, the state of charge (SOC) of a battery is<br>calculated using the voltage, but other factors such as<br>temperature, current flow and charging behavior also play a role.<br>The calculation of the state of charge is generally more precise if<br>the battery regularly sees full cycles. Every now and then an SOC<br>correction / calibration might occur. That is normal.|
|2.6.2|Charging &<br>discharging logic|Charging & discharging is generally controlled by the inverter.|
|2.6.3|Battery Logs /<br>History Data|Download and provide all the historic battery log files with BCP in<br>order to identify the root cause. See section 2.9 for details.|
|||You can also upload logs with BC APP. See section 2.10.|



#### **2.7 Unexpected shutdown** 

System has been successfully commissioned in the past and did run for some time. Later on an unexpected shutdown occurred. 

|**No.**|**Name**|**Description**|
|---|---|---|
|2.7.1|Inverter<br>Communication|The battery only works with a compatible external inverter. If for<br>whatever reason the communication between battery and inverter<br>is lost, the battery will shut down itself within 30minutes.<br>Therefore, check which one did shut down first (battery or<br>inverter) and check if inverter is properly detecting battery (e.g.<br>showing correct SOC or temperature).|
|||If problem remains, check according to section 2.5.|
|2.7.2|Battery Logs /|Sporadic alarms are hard to detect as they only occur sometimes.<br>Therefore, it is veryimportant to download andprovide all the|



10

<!-- pág. 11 -->
> ⚠ REVISAR TABLA — pág. 11: 40% de celdas vacías (posibles celdas combinadas)
||History Data|historic battery log files in order to identify the root cause. See|
|---|---|---|
|||section 2.9 for details. You can also upload logs with BC APP. See<br>section 2.10.|
|2.7.3|Inverter Warning|Unexpected Shutdown can be caused by overall system settings.|
||& Monitoring|Therefore, it is necessary to evaluate inverter data as well.|
|||- Which error message are shown in inverter portal?|



#### **2.8 BMU/BMS LED Event Code (EC)** 

A constant white LED refers to standby mode. White blinking means charge or discharge. When the battery is initiating, the LED will flash white and blue with an interval time of 0.5 seconds (normal during startup). When the LED flashes blue with an interval time of 1 second it indicates an event code. We start to count when the white LED begins to flash, then we count how many times white and blue LED flashes. (Also refer to the manual!) 

**Example:** 

- 1 x white, 6 x blue → EC 106 

- 1 x white, 11 x blue → EC 111 3 x white, 3 x blue → EC 303 



<!-- Start of picture text -->
BMU LED Status  BMS LED Status<br>(EC BMU) (EC BMS)<br><!-- End of picture text -->

Figure 2 BMU and BMS LED Status 

#### **Note: every LV Flex Module has its own BMS. The Event Code of the BMS will therefore be shown in the LED of the module.** 

Most Errors come from a faulty communication line, incorrect app configuration or missing restart after app-configuration. Please go in detail through: Section 1, 2.2 & 2.3 

Note: if the system is not correctly configured with app, the event code (EC) might be misleading. 

|**EC BMU**|**EC BMS**|**Measure**|
|---|---|---|
|No LED|/|See section 2.1.|
|/|No LED|See section 2.2|
|Abnormal|/|See section 2.1|
|LED<br>flickering||Module Exclusion Method (see section 3.2): Check if the<br>system works when bypassing the suspected module|



11

<!-- pág. 12 -->
EC 101 / Initialization Failure. - Make sure BC APP-configuration has been completed correctly (especially module quantity!) 

- Restart the system according to the manual. (Note: to properly shut down you need to press the button on the BMU for 5 seconds. Make sure to start the battery before starting the inverter!) 

If the problem remains: 

- Download all data with BCP (especially the historical data) (section 2.9), or upload logs with BC APP (section 2.10). 

- replace BMU, if available 

EC 102 / Incorrect module quantity / Module not detected. 

See section 2.4 

EC 105 -Make sure app-configuration has been completed correctly (especially module quantity). 

-Check terminal resistor. The terminal resistor (120 Ω at pin 5+6) is responsible for a clean communication between BMS and BMU. In rare cases it can be damaged and can disturb the signal. In these rare cases it is recommended to remove the terminal resistor. 

-replace communication cable between Battery and BMU 

-Restart system according to manual. (Note: to properly shut down you need to press the button on BMU for 5 seconds. Make sure to start the battery before starting the inverter!) 

- Module Exclusion Method (see section 3.2): Check if the system works when bypassing the suspected module 

If problem remains: 

- replace BMU, if available 

- Download all data with BCP (especially the historical data) (section 2.9) 

Or upload logs with BC APP. See section 2.10. 

12

<!-- pág. 13 -->
- EC 103 EC 108 PreCharge Fault. - Check DC cabling and make sure that the Minimum Configuration is met. - Restart system properly (see Step 2.4.2, section 2.4; If there is a fuse between battery and inverter, make sure to close the fuse first) - Disconnect the battery system from the inverter and restart the battery system alone (battery isolated), to evaluate if the error is being caused externally (i.e. short circuit in inverter or mppt). If the Event Code remains, the error might be in the battery. If the Event Code has changed, there might be an error in the inverter side or DC cable connection. - Module Exclusion Method (see section 3.2): Check if the system works when bypassing the suspected module. If problem remains: - Download all data with BCP (especially the historical and the cell data) (section 2.9), or upload logs with BC APP. See section 2.10. - provide the SN and voltage of the faulty module (see checklist on last page) 

- EC 104 EC 101 Short circuit / DC reverse connection. - Check DC cabling (is there any short circuit? Fuse between battery and inverter closed?) - Disconnect the battery system from the inverter and restart the battery system alone (battery isolated), to evaluate if the error is being caused externally (i.e. short circuit in inverter or mppt). If the Event Code remains, the error might be in the battery. If the Event Code has changed, there might be an error in the inverter side. - Module Exclusion Method (see section 3.2):Check if the system works when removing the suspected module If problem remains: - Download all data with BCP (especially the historical and cell data) (section 2.9), or upload logs with BC APP (section 2.10). - provide the SN and voltage of all modules with the EC (see checklist at the last ) 

13

<!-- pág. 14 -->
|EC 104|EC 102|One of the BMS (modules) reports an event message.|
|---|---|---|
||up to|- Check the voltage of the batteries according to section 3.1|
||EC113|If problem remains:|
||(All other<br>than 101)|- Download all data with BCP (especially the historical and the<br>cell data) (section 2.9), or upload logs with BC APP (section<br>2.10).<br>- provide the SN and voltage of the faulty module (see<br>checklist at the last )|
|EC 106|/|No communication with Inverter.<br>- Make sure the inverter is on, configured and working<br>correctly.<br>- Check according to section 2.5|
|EC107|/|Model type error. Please check the configuration, make sure<br>to choose the right model type.|



#### **2.9 Be Connect Plus (BCP)** 

Be Connect Plus is a Windows-PC tool. With BCP you can: 

- read the battery information, 

- configure the battery system 

- update BMU & BMS firmware 

- Export / download battery logs (From BMU and all BMS) 

BCP is constantly being improved and updated. Make sure to use the latest program version. You 

can download the latest version of the Tool on www.bydbatterybox.com / www.eft-systems.de / www.alpspower.com.au. 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual inside of program ZIP archive). 

Note: You need a computer with Windows that will be connected to the battery Wi-Fi. 

Login as Installer to Be Connect Plus, the password is the same as for Wi-Fi: BYDB-Box 

14

<!-- pág. 15 -->
Figure 3 BCP screenshot 

#### **2.10 Upload log data with BC APP** 

When you reach the Status interface, press the three dots on the top left corner, and you will see the menu. Choose Upload Logs, and following the instructions, then you can upload the logs to the BYD server. 



Figure 4 BC APP screenshot 

15

<!-- pág. 16 -->
### **3. MEASUREMENT** 

#### **3.1 Voltage measurement on pin 7&8** 

Measure the voltage of pin 7 & 8 while the other side of the cable is connected to the **IN port** of the Battery and while the Battery is powered on. Voltage should be around 50V. 

Note: Pin 7 and pin 8 are very close. It may cause short circuit if they are measured directly! It is better to take a tool as shown in Figure 5. 

Option 1 



Option 2 



Figure 5 voltage measurement on pin 7&8 

#### **3.2 Identifying a faulty module / Module Exclusion Method** 

- Normally a faulty module can be identified with the BCP, BC app or by the LED Code in the battery module. In this case, bypass the module with the Event Code, and commission the remaining system (if it still complies with the minimum configuration list) and check if it runs properly. 

If the problem remains, please also bypass the module above the one with the Event Code. 

- Otherwise, try the LV Flex Modules one by one to identify a possibly faulty module. 

If no LED on a module or more modules, check the one above the affected module first, and then the affected one. For example, in a LV Flex system with 4 modules, If top modules have active LED but bottom modules don`t, it indicates a connection issue between modules. If module 1&2 have LED, module 3&4 don`t have LED. Issue is in the connection between module 2 &3. Problem likely to be module 2 (less likely: module 3). 

- Bypass the affected module and check whether problem disappears. If not, check the module below. To bypass module 2, just connect module 1 directly with module 3 as shown Figure 6. 



<!-- Start of picture text -->
BMU<br><!-- End of picture text -->



Figure 6 bypass module 2 

16

<!-- pág. 17 -->
Note: The affected module often works without restrictions at the lowest module position of the tower. 

**Important: The module quantity must be adjusted in BC APP whenever the number of modules has been changed! Don`t forget to perform a proper restart after a new configuration!** 

#### **3.3 Undervoltage** 

If the minimum cell voltage is less than 1.5 V, it is in undervoltage (check with BC APP or BCP). 

- LV Flex Modules with >45 V should be fine and you can go on to check other points according to this service guideline. 

- If the module voltage is <40V but the single cell voltage is >1.5V, the battery needs to be charged as soon as possible while avoiding any further discharge. Therefore, shut down the system and search for the problem according to the guideline, while the battery is completely switched off. Also check on the inverter side why the force charge doesn ` t work. Do not turn on the battery before making sure the inverter is able to charge the battery. 

- If only one module is in undervoltage: remove that module and try commissioning without it (if the remaining modules still comply with the Compatible Inverter List). Otherwise, make sure to avoid further over discharge. (Turn off the system completely) 

- If one, or all modules are in undervoltage: Contact BYD local service and make sure to avoid any further discharge of the battery (Turn off the system completely) 

When contacting the service, make sure to fill the service checklist completely and add the following information: 

- Serial Numbers (of the BMU and all affected modules) 

- Individual module voltages of all modules (related to Serial number) 

- If possible: Upload logs with BC APP (section 2.10) or BCP (section 2.9) and screenshots showing the cell voltages 

- Initial Firmware (FW) Version of the Battery when the UV happened (BMU and BMS) 

- Detailed description how and why the system reached Undervoltage if known. Information when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the battery status when the battery was left (on / off / LED). 

- Inverter Model, Serial Number and Inverter Logs 

17

<!-- pág. 18 -->
### **4. SERVICE TASKS** 

Please go through the general steps beforehand, see chapter 1. 

#### **4.1 BMU Replacement** 

Have you detected a faulty BMU? 

After replacing the BMU, please do not forget to re-do the configuration and firmware-update with BC APP or BCP. 

#### **4.2 LV Flex Module Replacement** 

After replacing a Module, please do not forget to re-do the configuration and firmware-update in BC APP. (Every module has its own BMS) 

18

<!-- pág. 19 -->
|**BYD Battery-Box LV Flex Service Checklist - V1.0 EN**|
|---|



|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Box are only<br>i|
|---|
|allowed by professional and qualified electricians. Improper handling can cause danger and damage. This document does<br>fi|
|not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the information.|





|**1.**<br>**GENERAL STEPS**<br>Please carefully check**all**7 „General Steps“ from page 3 and 4 of the Service Guideline and confirm this in the boxes below|
|---|
|1.1 Configuration<br>1.4 App Configuration<br>1.7 Correct Operation|
|1.2 Correct external cabling<br>1.5 Restart|
|1.3 Latest Firmware<br>1.6 Switch on procedure|
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the<br>**error related**<br>Analysis from Chapter 2 and 3  (page 4-17) of the Service Guideline that you checked, and collect<br>all the information related to those Sections|
|2.1 BMU shows no reaction / No LED<br>2.2 Some modules do not show any reaction / No LED on module<br>2.3 Problem with the Firmware Update / App Configuration<br>2.4 Incorrect output voltage / No BMS Data<br>2.5 Communication problem with Inverter<br>2.6 SOC& charging logic<br>2.7 Unexpected shutdown<br>2.8 BMU/BMS LED Event Code (EC)<br>2.9 Be Connect Plus (BCP)<br>2.10 Upload log data with BC APP<br>3.1 Voltage measurement on pin7&8<br>3.2 Identifying a faulty module / Module Exclusion Method<br>3.3 Undervoltage|
|**3.**<br>Please fill all available information in below table. Some information like the Serial Number of the BMU is mandatory to receive service.<br>**SERVICE INFORMATION**|
|**•**<br>**Service Ticket Number or System ID:**|
|**•**<br>**Installer / Delivery Address / Contact:**|
|Company<br>ZIP / City|
|Contact Person<br>Phone|
|Street / Nr.<br>Email|
|**•**<br>**System Information**|
|Battery Configuration (XLV FLex)<br>BMU Firmware|
|BMU Serial Number<br>BMS Firmware|
|BMU Connected to Internet<br>Inverter Firmware<br>Yes<br>No|
|Inverter Brand + Model<br>Inverter Portal Name|
|Inverter Serial Number<br>(State the system name. Provide access)|
|Commissioning Date|
|**•**<br>**Service Information**|
|BMU EventCode (EC)<br>Inverter Error Code|
|BMS EventCode(s) and related Module Serial Number(s)|
|Was the battery charging / discharging before (was the system working normally before?)<br>Yes<br>No|
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see chapter 2.9)|
|Description of<br>the Problem<br>Please provide any additional information that is necessary or could help in the analysis of the service case (e.g. serial number of a<br>wrong module, video of a special behaviour; pictures; app screenshots; module voltages... )|
|By contacting us you confirm, that a qualified person has done the necessary control and collected all available information above.|
|Service Contact:<br>Europe: EFT-Systems GmbH<br>Australia:  Alps Power Pty Ltd<br>wwweft-systemsde<br>wwwalpspowercomau|
|..<br>...<br>service@eft-systems.de<br>service@alpspower.com.au<br> <br>|
|+49 9352 8523999<br>+61 02 8005 6688<br>For Europe only: Register Ticket directly in the Online Service Center: https://support.eft-systems.de/|
