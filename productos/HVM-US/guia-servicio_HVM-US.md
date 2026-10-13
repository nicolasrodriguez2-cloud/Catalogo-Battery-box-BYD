# Battery-Box Premium HVM-US — Guía de servicio y checklist

- **Producto:** Battery-Box Premium HVM-US (HVM-US)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.0 / 2025-02-20
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/250220_BYD%20Battery-Box%20Premium%20HVM-US_Service%20Guideline%20and%20Checklist_V1.0_EN-67b7cbfcdf27c.pdf
- **SHA-256 del PDF:** 7571221703f4eb3b3da45f74e4b325c6adeb98308789c2fa6041dabbab6532cb
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/250220_BYD Battery-Box Premium HVM-US_Service Guideline and Checklist_V1.0_EN-67b7cbfcdf27c.pdf
- **Conversión:** pymupdf4llm 1.28.2, 16 págs.

> ⚠ Este documento tiene 3 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium HVM-US Service Guideline and Checklist** Version 1.0 

Valid for HVM-US 8.3/ 11.0/ 13.8/ 16.6/ 19.3/ 22.1 





**Make sure to always use the latest version of this service document, available at: www.bydbatterybox.com .** 

**Important: The installation and all other kinds of works or measurements in combination with the Battery-Box Premium are only allowed by professional and qualified electricians.** 

This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on **www.bydbatterybox.com.** Subject to technical modifications; no responsibility is accepted for the accuracy of this information. Attention: High Voltage! Improper handling can cause danger and damage.

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

<!-- pág. 3 -->
## 1. GENERAL STEPS 

**Make sure to always use the latest version of this service document, available at:** first with the installation steps by: 

**www.bydbatterybox.com.** Please proceed 

**No. Name Description** 1 Configuration Check if the configuration is correct. Refer to latest “BYD Battery-Box Premium HVM-US Compatible Inverter List” available at: **www.bydbatterybox.com.** Make sure the inverter is configured correctly. 3 External connections 



   1. Communication to inverter 2. Ports for parallel connection 3. Dip-Switches 4. Ethernet-Cable for Internet ( **strongly recommended!** ) 

   5. DC-Ports 6. Grounding 

- 3 Closed Connection The Connection Area must be closed in order to start the system (else the system switch Area will immediately shut off!) 

- 4 Latest Firmware Always install / update the **newest Firmware** ! (also use the latest App Version!) Note: If not stated otherwise, the Wi-Fi password is BYDB-Box 

5 App Configuration <mark>To complete the commissioning, the conf</mark> i <mark>guration of the battery via  “BYD Be Connect 2</mark> .0 ” <mark>App or “BYD Be Connect Plus” (BCP) Tool for PC is</mark> **<mark>mandatory</mark>** <mark>!</mark> 

- 6 Proper Restart <mark>NOTE: It is important that the battery is switched on before the inverter! Else, the BCU</mark> might <mark>not start and not show any reaction (no LED, no WiFi) Def</mark> i <mark>ned restart (mind the sequence) 1) Switch off Battery (press power button for 5 seconds)* 2) Turn off DC switch of the inverter 3) Turn off AC switch 5) wait 5 minutes 6) Turn on the battery (switch up) 8) Turn on the AC switch 9) Turn on the DC switch on the inverter</mark> 

* **if the battery does not switch off despite pressing the LED for 5 seconds, lift off the BCU to avoid further discharge and contact the service .** 

- 7 Checking the correct The system runs properly if: operation - Inverter displays battery SOC correctly - System charges / discharges Note: **If you can not complete the commissioning, then turn off the battery before you leave the site and make sure all LEDs are off. If this is not possible, remove the BCU. Make sure the system will be set into operation quickly.**

<!-- pág. 4 -->
## 2. ERROR ANALYSIS 

### **2.1 BCU shows no reaction / No LED** 

LEDs do not light up, although the system switch is ON. 

> ⚠ REVISAR TABLA — pág. 4: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|8|Module quantity|Check if the module quantity fulfills the minimum requirement (min 3 modules).|
|9|Voltage measurement|See**section 2.10**|
|10|Use correct turn on<br>procedure|NOTE: It is important that the battery is switched on before the inverter!**Else, the**<br>**BCU might not start and not show any reaction (no LED, no WiFi)**|
|||Defined restart (mind the sequence)<br>1) Switch off Battery (press power button for 5 seconds)<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch (inverter should be completely off now!)<br>5) wait 5 minutes<br>6) Turn on the battery (switch up)→LED should light up again<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter|
|11|Only LED off?|Check if there is a wifiaccess point of the Battery-Box. If so, only the external LED<br>is inactive and a commissioning could still work. In that case make sure that the<br>internal cable of the LED is connected properly.|
|12|BCU exchange|Only if cover is closed and voltage look good: Test another BCU, if available.|



### **2.2 BCU switch cannot be pulled up / LED remains on** 

The system switch switches off immediately (within 5 seconds) / LED remains on eventhough system switch is down 

|**No.**|**Name**|**Description**|
|---|---|---|
|13|Close the cover|Make sure the cover for the connection area on the BCU is properly closed.<br>Important: If the panel is open, the battery won’t turn on (for safety reasons)|
|14|Switch was pulled down<br>by hand|If the switch was pulled down manually, then it cannot be pushed up again within<br>10 minutes. (Please refer to the manual for the correct switch off procedure)|
|15|Solid blue LED?<br>EC102? (1xwhite, 2xblue)|Try to properly shut down the BCU (press the LED power button for more than 5<br>Sec.)<br>- If LED goes off: check the installation and restart the system. (battery<br>first, then<br>inverter, second)<br>- If the LED remains on (solid blue or 2xblue blinking): Remove the BCU from the<br>tower to avoid a deep discharge. Measure the voltage of the system (see<br>**section**<br>**2.10**) and contact<br>service. You can use<br>another BCU, if available.|
|16|BCU exchange|Only if the cover is closed and voltage looks good: Test another BCU, if available.|

<!-- pág. 5 -->
### **2.3 Problem with the Firmware Update / App Configuration / Battery WiFi** 

The BCU consists of two components: the BMU and the BMS. The  Firmware Update from the App will update the BMU, which will then update the BMS. **It can take up to 20 Minutes until the firmware is updated on the BMS** . 

|**No**|**Name**|**Description**|
|---|---|---|
|17|Correct App and<br>Firmware|Make sure to have the latest App Version and Battery Firmware (download inside the App)<br>on your mobile device before connecting the app with the battery Wi-Fi.<br>If the App cannot be installed, or other general Problems occur with the App:<br>-<br>try with a different mobile device<br>-<br>Deinstall and reinstall the App<br>-<br>or try with PC Tool BCP (**section 2.8**).|
|18|WiFi cannot be found /<br>WiFi unstable|The Battery WiFi turns off 5 hours after the start of the Battery. To reactivate the WiFi,<br>press the LED button about 1 second or restart the system.<br>To reset the WiFi, press the LED button three times 1 second within 6 seconds.<br>If problem remains:<br>- remove the lan cable during the configuration. Once the Battery has been configured<br>correctly you can connect it again to the Internet.<br>- check whether other mobile devices are connected the same wif<br>- try another mobile device|
|19|BMS Version not<br>updated|The App will only update the BMU. The BMU will update the BMS, Once the BMU is<br>updated and the inverter communication is established correctly or right after the<br>configuration is done, the BMS update can take about 20 Minutes.<br>If the BMS Version is not updated after 20min with stable inverter communication, follow<br>the below Process:|



<mark>1. Update Firmware through the App again 2. Restart the system a. Switch off the Inverter f</mark> i <mark>rst,  then switch off the battery second (Press LED for 5 seconds)</mark> 

<mark>b. Wait for 30 Seconds c. Turn on the Battery f</mark> i <mark>rst, then turn on the inverter second</mark> 

<mark>3. Wait for 20 Minutes 4. Check BMS Firmware Version again with App. If Version is still wrong, do the update process again (if possible with another mobile device).</mark>

<!-- pág. 6 -->
### **2.4 Battery <> inverter communication / no charging or discharging** 

> ⚠ REVISAR TABLA — pág. 6: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|20|Configuration|Check<br>if<br>the<br>configuration<br>is<br>correct.<br>Refer<br>to<br>latest<br>“BYD<br>Battery-Box<br>Premium<br>HVM-US<br>Compatible<br>Inverter<br>List”<br>available<br>at:<br>**www.bydbatterybox.com.**<br>Make<br>sure<br>the<br>inverter<br>is<br>configured<br>correctly.|
|21|App Configuration and<br>Firmware|Please check if the App configuration was successful and the Firmware is the<br>most recent one. If there are problems, please refer to**Section 2.3**|
|22|Check DIP Switch|If only one tower, or two towers parallel connected, all DIP switches should be in<br>position: LEFT<br>If 3 towers HVM-US are in parallel connection, see manual for DIP configuration|
|23|Communication<br>connection|Does the inverter properly detect the battery? Check if the inverter detects the<br>battery parameters (e.g.,SOC, battery temperature) correctly. If not, check cabling:<br>- Confirm PIN / Cable Configuration for the specific inverter model<br>- Replace the communication cable (min. CAT5! - better CAT7)<br>Depending on the Inverter model, one or two of the three options of<br>communication<br>ports shown below can be used (refer to the manual!).<br>Please try the other port and communication option if available for the inverter<br>type.|
|24|Grounding|Connect Battery-Box directly to the ground-bus of the house (do not connect over<br>inverter casing or other devices!). Only with a correct grounding of the battery, a<br>trouble-free and secure data transmission can be guaranteed.|
|25|Battery relay closed? /<br>output voltage available?|Once communication has been established between battery and inverter, the BCU<br>is supposed to close the relay. Only then there will be output voltage. Therefore<br>please check if output voltage is there. You can check either by Be Connect2.0<br>App / Be Connect plus tool or by checking if the inverter correctly shows battery<br>voltage.|
|26|Restart the system|Defined restart (mind the sequence)<br>1) Switch off Battery (press power button for 5 seconds)*<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch<br>5) wait 5 minutes<br>6) Turn on the battery (switch up)<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter<br>*Note: if the battery does not switch off despite pressing the LED for 5 seconds,<br>lift off the BCU to avoid further discharge and contact the service.|

<!-- pág. 7 -->
### **<mark>2.5 SOC & charging logic</mark>** 

|**No**|**Name**|**Description**|
|---|---|---|
|27|SOC<br>at<br>commissioning|New<br>HVM-US<br>modules<br>have<br>30%<br>SOC<br>upon<br>delivery.<br>A<br>new<br>BCU<br>might<br>show<br>a<br>different<br>SOC at<br>the<br>beginning<br>(mostly<br>50%<br>/<br>30%<br>/<br>0%).<br>However,<br>this<br>is<br>only<br>to<br>be<br>understood<br>as<br>a<br>placeholder<br>value,<br>as<br>a<br>new<br>BCU<br>cannot<br>measure<br>the<br>SOC<br>of<br>modules.<br>As<br>soon<br>as<br>the<br>system<br>starts<br>to<br>run<br>(charge/discharge)<br>the<br>SOC<br>detection<br>is<br>corrected<br>gradually.<br>The<br>SOC<br>calibration<br>is<br>completed<br>at<br>the<br>latest<br>after<br>a<br>full<br>cycle.|
|28|SOC jumps|The SOC of an LFP battery cannot be measured. It is a calculated value. In general, the<br>state of charge (SOC) of a battery is calculated using the voltage, but other factors such<br>as temperature, current flow and charging behavior also play a role. The calculation of the<br>state of charge is generally more precise if the battery regularly sees full cycles. Every now<br>and then an SOC correction / calibration might occur. That is normal.|



### **2.6 Unexpected shutdown** 

System has been successfully commissioned in the past and did run for some time. Later on an unexpected shutdown occured. 

|**No**|**Name**|**Description**|
|---|---|---|
|29|Inverter Communication|The battery only works with an compatible external inverter. If for whatever reason the<br>communication between battery and inverter is lost, the battery will shut down itself within<br>30minutes. Therefore, check which one did shut down<br>first (battery or inverter) and check<br>if inverter is properly detecting battery (e.g.showing correct SOC or temperature). If<br>communication problem remains, check according to<br>**section 2.4**.|
|30|Battery Logs / History<br>Data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log<br>files in order to identify the<br>root cause. See<br>**section 2.8**<br>for details.|
|31|Inverter Warning &<br>Monitoring|Unexpected Shutdown can be caused by overall system settings. Therefore, it is necessary<br>to evaluate inverter data as well.<br>-<br>Which error message are shown in inverter portal?<br>-<br>Please provide access to Inverter portal (tell us the name of the system in the<br>portal)|

<!-- pág. 8 -->
### **2.7 Module Extension / Parallel connection** 

|**No**|**Name**|**Description**|
|---|---|---|
|33|Extension|Note: It is important that all modules of a storage tower have a similar state of charge<br>(tolerance 5%). New modules have about 30%. Therefore, please only add the new module<br>to the battery when the state of charge (SOC) is between 25% and 35% charge. Don't forget<br>to adjust the number of modules in the configuration if it is necessary.<br>If the 30% SOC rule has not been followed, temporary capacity loss and SOC jumps might<br>occur. In this case a charger may be required to align the module SOCs. Contact your local<br>service provider.|
|34|Parallel connection|Cabling<br>/<br>installation<br>(including<br>parallel<br>connection)<br>is<br>described<br>in<br>the<br>short<br>installation<br>guide.<br>Some<br>notes:<br>-<br>DC<br>bus<br>bar<br>needed<br>to<br>collect<br>DC<br>cables.<br>-<br>Towers<br>need<br>to<br>be<br>the<br>same<br>type<br>(module<br>type<br>&<br>quantity)<br>-<br>Communication<br>established<br>via<br>master/slave.<br>Only<br>master<br>unit<br>needs<br>to<br>be<br>configured<br>and<br>updated.<br>No<br>configuration<br>of<br>the<br>slave<br>BCUs<br>necessary<br>-<br>Check<br>DIP<br>switches:<br>If<br>only<br>one<br>tower,<br>or<br>two<br>towers<br>parallel<br>connected,<br>all<br>DIP<br>switches<br>should<br>be<br>in<br>position:<br>LEFT.<br>If<br>3<br>towers<br>HVM-US<br>are<br>in<br>parallel<br>connection,<br>see<br>manual<br>for<br>DIP<br>configuration.|





- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

<!-- pág. 9 -->
### **2.8 Be Connect Plus (BCP)** 

Be Connect Plus is a PC tool. With Be Connect Plus (BCP) you can: 

- read the battery information, 

- - configure the battery system 

- update BMU & BMS firmware 

- Export / download battery logs 

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the Tool on www.bydbatterybox.com .** 

For the service analysis, please download and provide the data / logs as described in the program instructions (see PDF manual included). 

Note: You need a computer with Windows that can be connected to the battery WiFi. Login as Installer to Be Connect Plus, the password is the same as for the WiFi: BYDB-Box .

<!-- pág. 10 -->
### **2.9 LED event code (EC)** 

A constant white LED refers to the standby mode. White blinking LED means charge or discharge. 

When the battery is initiating, the LED will blink white and blue with an interval time of 0.5 seconds (normal during startup). When the LED blink s blue with an interval time of 1 second it indicates an event code. Please start to count when the white LED begins to blink , then count how many times white and blue LED blink s. (also refer to the manual!) Examples: 

1xwhite, 3xblue → EC 103 

1xwhite, 11xblue → EC 111 

3xwhite, 3xblue → EC 303 

Most Errors are caused by faulty communication, incorrect app configuration or missing restart after the app or BCP configuration. Please go in detail through: **Section 2.3 & 2.4** 

|**Note:**<br>**if**<br>**the**<br>**battery**|**is**<br>**not**<br>**correctly**<br>**configured**<br>**with**<br>**the**<br>**app,**<br>**the**<br>**event**<br>**code**<br>**(EC)**<br>**might**<br>**be**<br>**misleading.**|
|---|---|
|**Event Code(EC)**|**Measure**|
|EC 102|Abnormal shutdown (open panel) / PreCharge failure / DC reverse connection.|
||- Check the DC-cable connection to the battery, inverter and combiner box (if there is any).<br>-<br>Make sure the cover for the connection area on the BCU is properly closed.<br>**Important: If the panel is open, the battery won**’**t turn on (for safety reasons)**<br>-<br>Try to properly shut down the BCU (press for 5 seconds the LED power button)<br>If LED goes off: check installation and restart (battery<br>first, then inverter second).<br>If LED remains on (solid blue or 2xblue blinking): Remove the BCU from the tower to avoid a<br>deep discharge. Measure the voltage of the system (see<br>**section 2.10**) and contact your<br>service.|
||If problem remains:<br>-<br>Test another BCU, if available.|
|EC 103|Voltage Sensor Failure / BMU<>BMS communication failure.<br>-<br> Make sure all dip switches are in the correct position. For most configurations all on the left<br>side. Refer to Manual!<br>-<br>Remove the topmost module and check whether the event code disappears. Note: A module<br>with communication problems often works without restrictions at the lowest module position,<br>since no communication with the base is necessary.|
||If problem remains:<br>-<br>Test another BCU, if available.|
|EC 104|Faulty temperature sensor.<br>- Check via BCP to identify the root cause module. Alternatively, follow “Module exclusion<br>method” (see**Section 2.11**).|
|EC 105|PackVoltage Sensor Failure.<br>- Check DC-cable connection on battery, inverter and combiner box (if there is any).<br>- Restart system properly (see**step 6, section 1**)|
||If problem remains:<br>-<br>Test another BCU, if available.|

<!-- pág. 11 -->
|EC 203<br>EC 303|Incorrect<br>module<br>quantity<br>/<br>Module<br>not<br>detected.|
|---|---|
|EC 403<br>EC 503<br>EC 603<br>EC 703<br>EC 803|-<br>Make<br>sure<br>app-configuration<br>has<br>been<br>completed<br>correctly<br>(especially<br>module<br>type<br>and<br>quantity!).<br>-<br>EC<br>203<br>to<br>EC<br>803<br>means<br>that<br>a<br>module<br>is<br>not<br>recognized.<br>The<br>first<br>number<br>(=<br>number<br>of<br>white<br>blinks)<br>indicates<br>which<br>module<br>is<br>probably<br>affected.<br>This<br>module,<br>or<br>the<br>module<br>above<br>it,<br>can<br>be<br>responsible<br>for<br>the<br>event<br>code.<br>Example:<br>EC<br>203<br>=<br>second<br>module<br>from<br>the<br>top<br>/<br>EC<br>403<br>=<br>fourth-top<br>module.<br>-<br>Remove<br>the<br>affected<br>module<br>and<br>check<br>whether<br>the<br>event<br>code<br>disappears.<br>If<br>not,<br>check<br>the<br>module<br>above.<br>-<br>Rearrange<br>the<br>modules<br>in<br>the<br>tower.<br>Note:<br>A<br>module<br>with<br>communication<br>problems<br>often<br>works<br>without<br>restrictions<br>at<br>the<br>lowest<br>module<br>position,<br>since<br>no<br>communication<br>with<br>the<br>base<br>is<br>necessary.|
|EC 106|Current Sensor Failure.<br>- Make sure that the latest<br>firmware is installed and that the battery has been properly restarted.<br>If the problem remains:<br>-<br>Test another BCU if available.|
|EC 107|Undervoltage.<br>- Shut down the system quickly to avoid further discharge. Check whether the system can shut<br>down normally (by pressing the LED button for 5s).<br>- If the system cannot shut down normally, lift the BCU<br>- Follow**section 2.10**(Voltage measurement and undervoltage instruction)|
|EC 108|PreCharge Fault.<br>- Check DC-cable connection on battery, inverter and combiner box (if there is any).<br>- Restart system according to manual. (note: to properly shut down you need to press the LED<br>button for 5 seconds. Make sure to start the battery before starting the inverter!)<br>If problem remains:<br>-<br>Test another BCU, if available.|
|EC 109|Make sure that the latest firmware is installed and that the battery has been properly restarted.<br>If the problem remains: it is Probably caused by a module. Follow the “Module exclusion<br>method” (see**Section 2.11**).|
|EC 110|Low voltage.<br>The system needs to charge very soon and should not be<br>further discharged!<br>1.<br>Shut down the system quickly to avoid further discharge. Check whether the system can<br>shut down normally (by pressing the LED button for 5s).<br>- If the system cannot shut down normally, lift the BCU<br>- Follow<br>**section 2.10**<br>(Voltage measurement and undervoltage)<br>2.<br>Avoid further discharge of the battery, by searching the problem while the battery is<br>completely off / BCU is lifted.<br>- Check the other steps in the service guideline and also check the inverter (latest FW /<br>correct/defined restart?) and with the inverter service, why the force charge doesn’t work<br>(e.g.,any fault at the inverter). Do not turn on the battery before making sure the inverter<br>should be able to charge the battery.<br>3.<br>If everything has been checked and the system cannot be charged, make sure to avoid<br>further discharge (e.g remove BCU) and contact the service.|

<!-- pág. 12 -->
EC 111 Normal when the battery has just started. 

LED will turn to solid white when: - inverter communication works (--> Check inverter communication, **Section 2.4** ) 

- right after saving / redoing the configuration (Be Connect 2.0 : go through whole wizard // Be Connect Plus: resave the configuration by using the “Setup” button and restart tool to refresh) Please also make sure all dip switches are in the correct position. For most configurations all on the left side. Refer to Manual! 

If EC111 remains even after the inverter detects battery and even after redoing app configuration: Remove the topmost module and check whether the event code disappears. If not,test another BCU if available. 

EC 112 No communication with inverter. Check inverter communication ( **Section 2.4** )

<!-- pág. 13 -->
### **2.10 Voltage measurement and undervoltage** 

**ATTENTION: High voltage! You can see the max. and min. cell voltage in the Be Connect 2.0 App. You can also get the detailed module and cell voltage in the BCP Program (section 2.8) or measure it manually according to the below description:** 

**Measurement of Tower Voltage** 

Take down the BCU and measure the tower voltage on the topmost module as shown below. Note: The nominal voltage should be module quantity times 50V (for HVM-US ). 



If the measured voltage deviates significantly from the nominal value, please check the electrical voltage at the individual modules, as shown in the following section. 

#### **Measurement of Individual Module Voltage** 



<!-- Start of picture text -->
Positive Negative Measurement:<br><!-- End of picture text -->

<!-- pág. 14 -->
**Undervoltage** A HVM-US Module in which one of the 16 cells cells has a voltage of <1.5 V is in over-discharge (check with BCP [ **section 2.8** ] / B e C onnect 2.0 App if possible). HVM-US Modules with >45 V should be fine and you can continue to check other points according to this service guideline. Always **make sure the firmware is the latest!** If the HVM-US module voltage <45V , but the single cell voltage is >1.5V, the battery needs to be charged quickly - follow the instructions of EC110 in **section 2.9** 

- If only one module is in undervoltage: remove that one and try to start the system without it (if the remaining modules still comply with the Compatible Inverter List). Otherwise, make sure to avoid further over- discharge ( e.g., remove BCU) 

- If one, or all modules are in undervoltage: Contact the service as stated below and make sure to avoid any further over- discharge of the battery ( e.g., remove BCU from the system) 

- When contacting the service, make sure to fill the service checklist completely and add the following information: - Serial Numbers (of the BCU and all (affected) modules) - Tower voltage and individual module voltages of all modules (related to Serial number) 

   - What was the status of the system switch on the BCU when the undervoltage (UV) happened? (tripped or not) 

   - - If possible: Logs from the battery using BCP ( **section 2.8** ) and Screenshots showing the cell voltages 

   - Initial Firmware (FW) Version of the Battery when the UV happened (BMU and BMS) 

   - - Inform if the BCU could shut down normally by pressing the LED button (note: if you have updated the FW after UV, write down here whether the battery could be switched off manually before the FW update.) 

   - Detailed description how and why the system reached Undervoltage if known. Information when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the battery's status when the battery was left (on / 

      - off / LED). 

   - Inverter Model, Serial Number and inverter logs. 

   - Access to the inverter portal (tell us the name of the system in the portal) 

### **2.11 Identifying a faulty module / Module exclusion method** 

**The module quantity must be adjusted in the app whenever the number of modules is changed!** 

**1.** Build the Battery-Box with the minimum available number of Modules ( HVM-US : 3 modules). 

**2. Check System. If Okay** , add one module at a time, adjust the module number in the app and check again. 



**3. If not okay** : The faulty module is probably one of the modules in the tower. Take one of the spare modules and exchange each of the remaining modules with the spare module one at a time. Check the battery status after each step. If battery status turns to “OK”, the faulty module is the one that was exchanged.

<!-- pág. 15 -->
## 3. SERVICE TASKS 

Please go through the general steps beforehand, see chapter 1. 

### **3.1 BCU replacement** 

#### **Have you detected a faulty BCU?:** 

After replacing the BCU, please do not forget to re-do the configuration and firmware-update with the app or BCP. 

### **3.2 Module Replacement** 

#### **Have you detected a faulty module?:** 

In the meantime you can use the battery system with the remaining modules and a correspondingly reduced capacity (take into account the minimum number of modules). 

Please note: It is important that all modules of a battery tower have a similar state of charge (SOC) with a tolerance of 5%. New modules have about **30** % SOC. If the remaining modules have not yet been put into operation (not charged / discharged), the new module can easily be added. Otherwise, it is basically a module extension. In this case, please add the new module to the system only when the system has a SOC between 25% and 35% ( **see extension process in the operating manual or quick start guide** ). Make sure to configure correctly after any change in module number. **Note: Within 5 days before extension, it is recommended to fully charge the existing battery system to SOC 100%.**

<!-- pág. 16 -->
> ⚠ REVISAR TABLA — pág. 16: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|<br>**BYD Battery-Box Premium**<br>**HVM-US**<br>**Service Checklist -**<br>**V1.0 EN**||
|---|---|
|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Bo<br>allowed by professional and qualified electricians. Improper handling can cause danger and damage. This docum<br>not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the inform|x are only<br>i          ent does<br>fi              ation.|
|**1.**<br>i<br>**GENERAL STEPS**<br>Please carefully check**all**„General Steps“ from page 3 of the Service Guideline and confirm this in the|i    boxes below|
|1.1 Configuration<br>1.4 Latest Firmware<br>1.7 C|orrect Operation|
|1.2 External Connections<br>1.5 App Configuration||
|1.3 Closed Connection Area<br>1.6 Proper Restart||
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the<br>**error related**<br>Analysis from Chapter 2 (page 4-10) of the Service Guideline that you c<br>information related to those Sections|hecked, and collect all the|
|2.5 SOC & charging logic<br>2.1 BCU shows no reaction / No LED|2.9 LED event code (EC)|
|2.6 Unexpected shutdown<br>2.2 BCU switch cannot be pulled up / LED remains on|2.10 Voltage measurement and<br>|
|2.7 Module Extension<br>2.3 Problem with the FW Update / App Configuration /BatteryWiFi|undervoltage<br>|
|2.8 Be Connect Plus (BCP)<br>2.4 Battery <> inverter communication / no charging or discharging|2.11 Identifying a faulty module<br>/ Module exclusion method|
|**3.**<br>Please fill all available information in below table. Some information like the Serial Number of the BCU<br>**SERVICE INFORMATION**|i                is mandatory to receive service.|
|**•**<br>**Service Ticket Number or System ID:**||
|**•**<br>**Installer / Delivery Address / Contact:**||
|ZIP / City<br>Company||
|Phone<br>Contact Person||
|Email<br>Street / No.||
|**•**<br>**System Information**<br>i||
|BMU Firmware<br>Battery Configuration (HVM-US..)||
|BCU Serial Number<br>BMS Firmware||
|BCU Connected to Internet<br>Inverter Firmware<br>Yes<br>No||
|Inverter Brand + Model<br>System Name on<br>It Ptl||
|Inverter Serial Number<br>nverer ora||
|Commissioning Date||
|**•**<br>**Service Information**||
|BCU Event Code (EC)<br>Inverter Error Code||
|Was the battery charging / discharging before (was the system working normally before?)|Yes<br>No|
|Take pictures of open communication port in the BCU and Inverter clearly showing connection cables||
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Programm (see chapter 2.8)||
|Description of<br>the Problem<br>By contacting us you confirm, that a qualified person has done the necessary control and collected all available in<br>Service Contact:<br>BYDUSService<br>www.bydbatterybox.com<br>us.homeenergy@byd.com<br>626-491-2333<br>Please provide any additional information that is necessary or could help in the analysis of the service<br>a wrong module, video of a special behaviour; pictures; app screenshots; module voltages... )|i   i           formation above.<br>case (e.g., serial number of|
