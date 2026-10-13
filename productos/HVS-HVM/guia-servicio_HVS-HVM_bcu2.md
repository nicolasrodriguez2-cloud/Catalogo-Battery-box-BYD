# Battery-Box Premium HVS/HVM — Guía de servicio y checklist

- **Producto:** Battery-Box Premium HVS/HVM (HVS&HVM BCU2.0)
- **Tipo de documento:** Guía de servicio y checklist
- **Versión/fecha del PDF:** V1.1 / 2025-08-08
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/BCU2.0_250808_BYD%20Battery-Box%20Premium%20HVS&HVM_Service%20Guideline%20and%20Checklist_V1.1_EN-689566346f0c5.pdf
- **SHA-256 del PDF:** 39a5a8b089576806c27e3e327b7a9d05ed431b4e08e1fa7098485f6655f742ee
- **Idioma:** EN
- **Archivo PDF local (no versionado):** _descargas/BCU2.0_250808_BYD Battery-Box Premium HVS&HVM_Service Guideline and Checklist_V1.1_EN-689566346f0c5.pdf
- **Conversión:** pymupdf4llm 1.28.2, 16 págs.

> ⚠ Este documento tiene 3 tabla(s) dudosa(s) y 0 página(s) sin texto. Buscar "⚠ REVISAR".

---
<!-- pág. 1 -->
# **BYD Battery-Box Premium HVS & HVM Service Guideline and Checklist for BCU-V2.0** Version 1. 1 

Valid for HVS 5.1 / 7.7 / 10.2 / 12.8 HVM 8.3 / 11.0 / 13.8 / 16.6 / 19.3 / 22.1 



**Always make sure to use the latest version of this service document, available at: www.bydbatterybox.com** 

**Important: The installation and all other kinds of works or measurements in correlation with the Battery-Box Premium are only allowed by professional and qualified electricians.** This checklist is a shortened assistance for the Battery-Box and does not replace the original manual, which can be found on <u>www.bydbatterybox.com</u> / <u>www.eft-systems.de</u> / <u>www.alpspower.com.au.</u> Subject to technical modifications; no responsibility is accepted for the accuracy of this information. Attention: High Voltage! Improper handling can cause danger and damage.

<!-- pág. 2 -->
## CONTENT 

|**1. GENERAL STEPS**|**3**|
|---|---|
|**2. ERROR ANALYSIS**|**4**|
|2.1 BCU shows no reaction / No LED|4|
|2.2 BCU switch cannot be flipped up / LED remains on|4|
|2.3 Problem with the Firmware Update / App Configuration / Battery Wi-Fi|5|
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

**Always make sure to use the latest version of this service document, available at:** **<u>www.bydbatterybox.com</u>** Please proceed first with the installation steps by: 

|**No.**|**Name**|**Description**|
|---|---|---|
|1|Con<br>figuration|Check<br>if<br>the<br>configuration<br>is<br>correct.<br>Refer<br>to the<br>latest<br>“BYD<br>Battery-Box<br>Premium<br>HVS<br>&<br>HVM<br>Compatible<br>Inverter<br>List”<br>(V2.19<br>or<br>above)<br>available<br>at:<br>**www.bydbatterybox.com**<br>Make<br>sure<br>the<br>inverter<br>is<br>configured<br>correctly.|
|2|Only HVS or HVM|Do not mix up HVS-modules  (“I”) with HVM-modules (“II”).|
|3|External connections||





1. Port for parallel connection 

2. Communication to inverter 

3. Ethernet port ( **strongly recommended** ) 4. Grounding 5. DC-Ports 4 Latest firmware Always install / update the **latest firm ware** (also use the latest app version). Note: If not stated otherwise, the default Wi-Fi password is BYDB-Box. 5 App configuration <mark>To complete the commissioning, the conf</mark> i <mark>guration of the battery via “BYD Be Connect 2</mark> .0 ” <mark>app or “BYD Be Connect Plus” (BCP) tool for PC is</mark> **<mark>mandatory.</mark>** 6 Proper restart <mark>NOTE: It is important that the battery is switched on before the inverter! Else, the BCU might not start and not show any reaction (no LED, no Wi-Fi)</mark> . <mark>Def</mark> i <mark>ned restart (mind the sequence)</mark> 1) Switch off the battery (press LED button for 5 seconds)* <mark>2) Turn off DC switch of the inverter 3) Turn off AC switch</mark> 4) Kostal only: Pull out the PV strings from inverter 5) wait 1 minute <mark>6) Turn on the battery (flip up the</mark> air switch) <mark>7) Kostal only: Connect PV strings back to inverter 8) Turn on the AC switch 9) Turn on the DC switch on the inverter</mark> *if the battery does not switch off despite pressing the LED button for 5 seconds, lift off the BCU to avoid further discharge and contact the service team. 7 Check the correct The system runs properly if: operation - Inverter displays battery SOC correctly - System charges / discharges Note: **If you can not complete the commissioning, then turn off the battery before you leave the site and make sure all the LEDs are off. If this is not possible, remove the BCU. Make sure the system will be set into operation quickly.** 



3

<!-- pág. 4 -->
## 2. ERROR ANALYSIS 

### **2.1 BCU shows no reaction / No LED** 

LED does not light up, although the system is switched on. 

> ⚠ REVISAR TABLA — pág. 4: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No.**|**Name**|**Description**|
|---|---|---|
|8|Module quantity|Check if the module quantity ful<br>fills the minimum requirement (HVS: 2, HVM: 3<br>modules) and check the “Compatible Inverter List”<br>for inverter requirements.|
|9|Voltage measurement|See<br>**section 2.10.**<br>(Make sure the voltage of the battery tower is higher than 120V.)|
|10|Follow the sequence<br>correctly|NOTE: It is important that the battery is switched on<br>before<br>the inverter!<br>**Else, the**<br>**BCU might not start and not show any reaction (no LED, no Wi-Fi). See following:**|
|||1) Switch off the battery (press power button for 5 seconds)<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch<br>4) Kostal only: Pull out the PV strings from inverter<br>5) wait 1 minute (inverter should be completely off)<br>6) Turn on the battery (flip up the air switch)<br>→<br>LED should light up again<br>7) Kostal only: Connect PV strings back to inverter<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter|
|11|Only LED off?|Check if there is a Wi-Fi<br>access point of the Battery-Box. If so, only the external<br>LED is inactive, but commissioning could still work. In that case make sure<br>that<br>the internal cable of the LED is connected properly.|
|12|BCU exchange|Only<br>if<br>voltage<br>looks<br>good:<br>Test<br>another<br>BCU,<br>if<br>available.|



### **2.2 BCU switch cannot be flipped up / LED remains on** 

The system switches off immediately (within 5 seconds) / LED remains on even though the system switch is off. 

|**No.**|**Name**|**Description**|
|---|---|---|
|13|Switch was flipped<br>down<br>by hand|If<br>the<br>switch<br>was<br>flipped<br>down<br>manually,<br>then<br>it<br>cannot<br>be<br>flipped<br>up<br>again<br>within<br>10<br>minutes.<br>(Please<br>refer<br>to<br>the<br>manual<br>for<br>the<br>correct<br>switch-off<br>procedure.)|
|14|Steady<br>blue<br>LED?<br>EC102?<br>(1xwhite,<br>2xblue)|Try<br>to<br>properly<br>shut<br>down<br>the<br>BCU<br>(press<br>the<br>LED<br>button<br>for<br>more<br>than<br>5 seconds).<br>-<br>If<br>LED<br>goes<br>off:<br>check<br>the<br>installation<br>and<br>restart<br>the<br>system (battery<br>first,<br>then<br>inverter).<br>-<br>If<br>the<br>LED<br>remains<br>on<br>(steady<br>blue<br>or<br>2x blinking blue):<br>Remove<br>the<br>BCU<br>from<br>the<br>tower<br>to<br>avoid<br>a<br>deep<br>discharge.<br>Measure<br>the<br>voltage<br>of<br>the<br>system<br>(see<br>**section**<br>**2.10**)<br>and<br>contact<br>your<br>service<br>provider.<br>You<br>can<br>use<br>another<br>BCU,<br>if<br>available.|
|15|BCU exchange|Only<br>if<br>the voltage<br>looks<br>good:<br>Test<br>another<br>BCU,<br>if<br>available.|





4

<!-- pág. 5 -->
### **2.3 Problem with the Firmware Update / App Configuration / Battery Wi-Fi** 

The BCU consists of two components: the BMU and the BMS. The  firmware update from the app will update the BMU, which will then update the BMS. **The BMS will only be updated once there is communication between the battery and the inverter or immediately after the app configuration. It can take up to 20 minutes for the firmware to be updated on the BMS** . 

> ⚠ REVISAR TABLA — pág. 5: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**No**|**Name**|**Descript**|**ion**|
|---|---|---|---|
|16|Correct app and<br>firmware|Make<br>su<br>the<br>app)<br>If<br>the<br>ap<br>-<br>-<br>-|re<br>to<br>have<br>the<br>latest<br>app<br>version<br>(>2.3.16)<br>and<br>battery<br>firmware<br>(downloadable<br>in<br>on<br>your<br>mobile<br>device<br>before<br>connecting<br>the<br>app<br>with<br>the<br>battery<br>Wi-Fi.<br>p<br>cannot<br>be<br>installed,<br>or if<br>other<br>general<br>problems<br>occur<br>with<br>the<br>app:<br>Try<br>using<br>a<br>different<br>mobile<br>device<br>Uninstall<br>and<br>reinstall<br>the<br>app<br>Or<br>try<br>using the<br>PC<br>tool<br>BCP<br>(see<br>**section**<br>**2.8**)|
|17|Wi-Fi cannot be found /<br>Wi-Fi<br>unstable|The batt<br>press th<br>To reset<br>If the pro<br>-<br>Remov<br>correctly<br>- Check<br>- Try ano|ery Wi-Fi turns off 5 hours after the battery is activated. To reactivate the Wi-Fi,<br>e LED button about 1 second or restart the system.<br>the Wi-Fi, press the LED button three times 1 second within 6 seconds.<br>blem remains:<br>e the LAN cable during the configuration. Once the Battery has been configured<br>, you can connect it again to the Internet.<br>whether other mobile devices are connected to the same Wi-Fi<br>ther mobile device|
|18|BMS version not<br>updated|The app<br>BMU is<br>the conf<br>If the BM<br>follow<br>th|will only update the BMU. The BMU will automatically update the BMS, once the<br>updated and the inverter communication is established correctly or right after<br> iguration is done. The BMS update can take about 20 minutes.<br>S version is not updated after 20 minutes with stable inverter communication,<br>e processbelow:|
|||1.<br>2.<br>3.|Update the firmware through the app again<br>Restart the system<br>a.<br>Switch off the inverter<br>first,  then switch off the battery (press<br>LED<br>button for 5 seconds)<br>b.<br>Wait for 30 Seconds<br>c.<br>Turn on the battery<br>first, then turn on the inverter<br>Wait for 20 minutes|
|||4.|Check the BMS firmware version again with app. If the version is still wrong,<br>repeat the<br>update process(preferably with another mobile device).|





5

<!-- pág. 6 -->
### **2.4 Battery <> inverter communication / no charging or discharging** 



<!-- Start of picture text -->
No. Name Description<br>19 Confguration i Check if the conf i guration is correct. Refer to the latest “BYD Battery-Box Premi um HVS<br>&HVM Compatible Inverter List” (V2. 19 or above) available at: www .bydbatterybox.com<br>Make sure the inverter is configured correctly.<br>20 App confguration i Please check if the app conf i guration has successfully done and the firmware is<br>and firmw are the most recent one. If there are problems, please refer to Section 2.3<br>21 Check t erminal If only one tower is installed, a terminal resistor should be plugged into the " IN " port.<br>resistor If two or three towers are connected in parallel, the “ OUT ” port of the master tower and<br>the " IN " port of the last slave tower should be plugged into a terminal resistor.<br>terminal resistor<br>Min. CAT5e  terminal resistor<br>Max. 20m<br>IN INV P+ IN INV P+<br>OUT ETH P- OUT ETH P-<br>Master Slave<br>terminal resistor<br>Min. CAT5e  Min. CAT5e terminal resistor<br>Max. 20m Max. 20m<br>IN INV P+ IN INV P+ IN INV P+<br>OUT ETH P- OUT ETH P- OUT ETH P-<br><!-- End of picture text -->



<!-- Start of picture text -->
Master Slave 1 Slave 2<br><!-- End of picture text -->



<!-- Start of picture text -->
Note: If there are BCU and BCU-V2 in a system, see Operating Manual or Quick<br>Start Guide for parallel connection.<br>22 Communication Does the inverter properly detect the battery? Check if the inverter detects the battery<br>connection parameters (e.g ., SOC, battery temperature) correctly. If not, check the cabling:<br>- Conf i rm the PIN / cable conf i guration for the specif i c inverter mo del<br>- Replace the communication cable (min. CAT5; better to use C AT7)<br>- For Fronius & SMA: check the enable signal (necessary for battery activation)<br>23 Grounding Connect Battery-Box directly to the ground bus of the house (do not connect it<br>over the inverter casing or other devices). Proper grounding of the battery is<br>essential for trouble-free and secure data transmission.<br>24 Battery relay closed? / Once communication has been established between battery and inverter, the BCU<br>output voltage available? is supposed to close the relay. Only then there will be output voltage. Therefore<br>please check if output voltage is present. You can check this either by Be<br>Connect 2.0 a pp / Be Connect Plus tool or by checking if the inverter correctly<br>shows the battery voltage.<br>25 Restart the system Def i ned restart (mind the sequence)<br>1) Switch off battery (press LED button for 5 seconds)*<br>2) Turn off DC switch of the inverter<br>3) Turn off AC switch<br>4) Kostal only: Pull out the PV strings from inverter<br>5) wait 1 minutes<br>6) Turn on the battery (flip up the  air switch)<br>7) Kostal only: Connect PV strings back to inverter<br>8) Turn on the AC switch<br>9) Turn on the DC switch on the inverter<br>*Note: if the battery does not switch off despite pressing the LED button for 5<br>seconds, lift off the BCU to avoid further discharge, and contact the service team.<br><!-- End of picture text -->



6

<!-- pág. 7 -->
### **<mark>2.5 SOC & charging logic</mark>** 

|**No**|**Name**|**Description**|
|---|---|---|
|26|SOC at commissioning|New HVS / HVM modules are delivered with a 30% SOC, while a new BCU might show a<br>different<br>SOC at the beginning (mostly 50%<br>/ 30%<br>/ 0%). The latter one should be<br>understood as a<br>placeholder value, since a new BCU cannot measure the SOC of modules.<br>As soon as the system starts to run (charging/discharging)<br>the SOC detection will<br>be gradually corrected. The SOC<br>calibration is completed at the latest after a full cycle.|
|27|SOC jumps|The SOC of an LFP battery cannot be measured; it is a calculated value. In general, the<br>state<br>of charge (SOC) of a battery is calculated using the voltage, but other factors such<br>as<br>temperature, current<br>flow and charging behavior also play a role. The calculation of the<br>SOC is generally more precise when the battery regularly undergoes full cycles. Every now<br>and then an SOC correction / calibration may occur. If there are other questions, please<br>contact the service team.|



### **2.6 Unexpected shutdown** 

The system has been successfully commissioned in the past and has run for some time. Later on an unexpected shutdown occurred. 

|**No**|**Name**|**Description**|
|---|---|---|
|28|Inverter<br>communication|The battery only works with a compatible external inverter. If,<br>for any reason,<br>the<br>communication between the battery and inverter is lost,<br>the battery will shut<br>down<br>automatically within 30 minutes. Therefore,<br>check which one shut down<br>first<br>(battery<br>or inverter)<br>and check<br>if inverter is properly detecting battery (e.g,.<br>showing<br>correct<br>SOC or temperature). If<br>communication problem remains, refer to<br>**section 2.4**.|
|29|Battery logs / History<br>data|Sporadic alarms are hard to detect as they only occur sometimes. Therefore, it is very<br>important to download and provide all the historic battery log<br>files in order to identify the<br>root cause. See<br>**section 2.8**<br>for details.|
|30|Inverter warning &<br>monitoring|An unexpected shutdown can be caused by overall system settings. Therefore, it is<br>necessary<br>to evaluate inverter data as well.<br>-<br>Which error message are shown in inverter (portal?)<br>-<br>Please provide access to the inverter portal (add<br>info@eft-systems.de<br>and<br>include<br>the<br>name of the system in the portal)|





7

<!-- pág. 8 -->
### **2.7 Module Extension / Parallel connection** 

|**No**|**Name**|**Description**|
|---|---|---|
|31|Extension|Note: It is important that all modules of a storage tower have a similar SOC (tolerance: 5%).<br>Within 5 days before extension,<br>it is recommended to fully charge the existing battery<br>system to 100% SOC at least once. New modules have about 30% SOC. Therefore, please<br>ensure that the SOC of the original system is between 25% and 35% before adding a new<br>module. Don't forget to adjust the number of modules in the configuration if necessary.|
|||If the 30%<br>SOC rule is not followed,<br>temporary capacity loss and SOC jumps<br>might<br>occur. In such cases,<br>a charger may be required to align the SOC of the modules.<br>Please contact<br>your local service provider for assistance.|



|32|Parallel connection|Cabling / installation (including parallel connection) is described in the short installation<br>guide. Here are some notes:|
|---|---|---|



- A DC bus bar is needed to collect DC cables. There is a matching DC combiner box from BYD for the HVS / HVM. Please refer to the corresponding data sheet and manual of the BYD combiner box for details. 

- - Towers need to be the same type (module type & quantity). 

- - Communication is established between master and slave units. Only the master unit needs to be configured and updated; no configuration of the slave BCUs is necessary. 

- - Check terminal resistor: If only one tower is installed, a terminal resistor should be plugged into the " **IN** " port. If two or three towers are connected in parallel, the “ OUT ” port of the master tower and the " **IN** " port of the last slave tower should be plugged into a terminal resistor.. 



<!-- Start of picture text -->
terminal resistor<br>Min. CAT5e  terminal resistor<br>Max. 20m<br>IN INV P+ IN INV P+<br>OUT ETH P- OUT ETH P-<br>Master Slave<br>terminal resistor<br>Min. CAT5e  Min. CAT5e terminal resistor<br>Max. 20m Max. 20m<br>IN INV P+ IN INV P+ IN INV P+<br>OUT ETH P- OUT ETH P- OUT ETH P-<br>Master Slave 1 Slave 2<br><!-- End of picture text -->

**Note: If there are BCU and BCU-V2 in a system, see Operating Manual or Quick Start Guide for parallel connection.** 



8

<!-- pág. 9 -->
### **2.8 Be Connect Plus (BCP)** 

Be Connect Plus is a PC tool. With Be Connect Plus (BCP) you can: 

- Read battery information 

- Configure the battery system 

- Update BMU & BMS firmware 

- Export / download battery logs 

BCP is constantly being improved and updated. **Make sure to use the latest program version. You can download the latest version of the t ool at www.bydbatterybox.com / www.eft-systems.de / www.alpspower.com.au** . 

For analysis, please download and provide the data/logs as described in the program instructions (see PDF manual included). 

Note: You need a computer with Windows that will be connected to the battery Wi-Fi. Log in as Installer to Be Connect Plus. The default password for the battery Wi-Fi is the same: BYDB-Box 





9

<!-- pág. 10 -->
### **2.9 LED event code (EC)** 

A steady white LED indicates standby mode, while a blinking white LED means charging or discharging. 

During battery initialization, the LED will flash white and blue with an interval time of 0.5 seconds (normal during startup). When the LED flashes blue with an interval time of 1 second, it indicates an event code.  Please start to count when the white LED begins to flash, and then record how many times white and blue LED flashes (also refer to the manual for details). Examples: 

1xwhite, 3xblue → EC 103 1xwhite, 11xblue → EC 111 3xwhite, 3xblue → EC 303 

Most errors are caused by faulty communication, incorrect app configuration or a missing battery restart after the app or BCP configuration. Please go through **Section 2.3 & 2.4** in detail. 

**Note: If the battery is not correctly configured with the app, the event code (EC) might be misleading.** 

|**Event Code**<br>**(EC)**|**Measure**|
|---|---|
|EC 101|DC<br>cable<br>reverse connection<br>/ DC short-circuit<br>-<br>Disconnect the DC cable connection between the inverter and the battery, and use a multimeter<br>to measure whether there is a short circuit between P+ and P-. If there is no short circuit, please<br>check whether there is a short circuit at the inverter port. If there is, proceed to the next step.<br>-<br>Replace the BCU, then use Be Connect 2.0 or BCP tool to reconfigure it correctly, and<br>then<br>restart to confirm.|
|EC 102|Abnormal shutdown / PreCharge failure/ Module failure<br>- Check the DC cable connection to the battery, inverter and combiner box (if there is any).<br>-<br>Try to properly shut down the BCU (press the LED button for 5 seconds).<br>If LED goes off: check installation and restart (battery<br>first, then inverter).<br>If LED remains on, remove the BCU from the tower to avoid a deep discharge.<br>Measure the voltage of the system (see**section 2.10**) and contact your service provider.<br>-<br>Use BC/BCP to read the module cell voltage and temperature data, If any cell voltage<br><1.5V or temperature >70°C, remove the abnormal module.<br>If the problem remains:<br>-<br>Test another BCU, if available.|
|EC 103|Voltage Sensor Failure / BIC Communication Failure<br>- Make sure<br>the terminal resistor is plugged in the correct position. Refer to the Manual.<br>-<br>Remove the topmost module and check whether the event code disappears. Note: A module<br>with communication problems often works without restrictions at the lowest module position,<br>since no communication with the base is necessary.<br>Check the cell voltage of all the modules with the BCP tool (see<br>**Section 2.8**). If a module<br>has an abnormal cell voltage, remove it and then reconfigure the system.<br>If the problem disappears:<br>-<br>Exchange the module.<br>If the problem remains:<br>-<br>Test another BCU, if available.|
|EC 104|Faulty temperature sensor<br>- Check via BCP to identify the abnormal module. Alternatively, follow “Module exclusion<br>method” (see<br>**Section 2.11**).|
|EC 105|- Check DC cable connection to the battery, inverter and combiner box (if there is any).<br>- Restart system properly (see<br>**step 7, section 1**)<br>If the problem remains:<br>-<br>Test another BCU, if available.<br>Pack<br>Voltage Sensor Failure|





10

<!-- pág. 11 -->
|EC 203<br>EC 303<br>EC 403<br>EC 503<br>EC 603<br>EC 703<br>EC 803|Incorrect module quantity / Module not detected<br>- Make sure the app configuration has been completed correctly (especially the module type<br>and quantity).<br>- EC 203 to EC 803 means that a module is not recognized. The<br>first number (= number of<br>white<br>LED flashes) indicates which module is probably affected. This module, or the module<br>above it, can be responsible for the event code.<br>Example: EC 203 = second module from the top / EC 403 = fourth-top module.<br>- Remove the affected module and check whether the event code disappears. If not, check the<br>module above.<br>- Rearrange the modules in the tower.<br>Note: A module with communication problems often works without restrictions at the lowest<br>module position, since no communication with the base is necessary.|
|---|---|
|EC 106|Current Sensor Failure<br>- Make sure that the latest<br>firmware is installed and that the battery has been properly<br>restarted.<br>If the problem remains:<br>-<br>Test another BCU if available.|
|EC 107|Cell failure or voltage difference alarm(level 3)<br>- Check whether the<br>cell voltage of each module is normal,<br>and exchange the module if the cell<br>voltage is abnormal.<br>- Follow<br>**section 2.10**<br>(Voltage measurement and undervoltage<br>instruction)|
|EC 108|PreCharge Fault<br>- Check DC cable connection to the battery, inverter and combiner box (if there is any).<br>-<br>Restart system according to the manual. (Note: To properly shut down you need to press<br>the<br>LED<br>button for 5 seconds. Make sure to start the battery before starting the inverter.)<br>If the problem remains:<br>-<br>Test another BCU, if available.|
|EC 109|BIC balancing failed<br>Make sure that the latest<br>firmware is installed and that the battery has been properly restarted.<br>If the problem remains: it is probably caused by a module. Follow the “Module exclusion<br>method” (see<br>**Section 2.11**).|
|EC 110|Low voltage<br>The system needs to be charged very soon and should not be<br>further discharged.<br>1.<br>Shut down the system quickly to avoid further discharge. Check whether the system can<br>shut down normally (by pressing the LED button for 5 seconds).<br>- If the system cannot shut down normally, remove the BCU<br>- Follow<br>**section 2.10**<br>(Voltage measurement and undervoltage)<br>2. Troubleshoot the problem while the battery is completely off / BCU is lifted.<br>-<br>Check the other steps in the service guideline and also check the inverter (latest<br>firmware version/correct and defined restart?)<br>and consult with the inverter service<br>team to determine why the force charge doesn’t work(e.g., any faults at the inverter). Do<br>not turn on the battery before ensuring the inverter<br>is capable of charging the battery.<br>3.<br>If everything has been checked and the system cannot be charged, make sure to avoid<br>further discharge (e.g.,<br>remove BCU) and contact the service team.|





11

<!-- pág. 12 -->
EC 111 Normal when the battery has just started. LED will turn to steady white when: - inverter communication works (--> Check inverter communication, **Section 2.4** ) - right after saving / redoing the configuration (Be Connect 2.0 : go through whole wizard / Be Connect Plus: resave the configuration by using the “Setup” button and restart tool to refresh) Please also make sure the terminal resistor is plugged in a correct position. Refer to the Manual. If EC111 remains even after the inverter detects battery and even after redoing app configuration, test another BCU if available. EC 112 No communication with inverter. Check inverter communication ( **Section 2.4** ) 



12

<!-- pág. 13 -->
### **2.10 Voltage measurement and undervoltage** 

**ATTENTION: High voltage! You can see the max. and min. cell voltage in the Be Connect 2.0 a pp. You can also get the detailed module and cell voltage in the BCP Program (section 2.8) or measure it manually according to the description below:** 

#### **Measurement of Tower Voltage** 

Remove the BCU and measure the tower voltage on the topmost module as shown below. Note: The nominal voltage should be the module quantity times 100V (for HVS) or the module quantity times 

- 50V (for HVM). 



If the measured voltage deviates significantly from the nominal value, please check the electrical voltage at the individual modules, as shown in the following section. 

#### **Measurement of Individual Module Voltage** 

**Positive** 

**Negative** 

**Measurement:** 









13

<!-- pág. 14 -->
#### **Undervoltage** 

A module in which one of the 32 (HVS) / 16 (HVM) cells has a voltage of <1.5 V is considered to be in undervoltage (check with BCP [section 2.8] / B e C onnect 2.0 if possible). 

A HVS module with >90 V and a HVM module with >45 V should be fine, and you can continue to check other items according to this service guideline. **Always make sure the firmware is the latest.** If the module voltage is <90V (HVS) / <45V (HVM) but the single cell voltage is >1.5V, the battery needs to be charged quickly(follow the instructions of EC110 in **section 2.9** ). 

- If only one module is in undervoltage: Remove that one and try to start the system without it (if the remaining modules still 

- comply with the minimum quantity requirement). Otherwise, avoid further discharge (e.g., remove the BCU) 

- If one or all modules are in undervoltage: Contact the service team as stated below and make sure to avoid any further 

- discharge of the battery (e.g remove BCU from the system) 

- When contacting the service team, make sure to fill out the service checklist completely and provide the following information: 

   - Serial Numbers (of the BCU and all affected modules) 

   - Tower voltage and individual module voltages of all modules (related to serial number) 

   - What was the status of the system switch on the BCU when the undervoltage (UV) happened? (tripped or not) 

   - If possible: Logs from the battery using BCP ( **section 2.8** ) and screenshots showing the cell voltages 

   - Initial firmware version of the battery when the undervoltage happened (BMU and BMS) 

   - Inform if the BCU could shut down normally by pressing the LED button. (Note: if you have updated the firmware version after undervoltage, write down whether the battery could be switched off manually before the firmware update.) 

   - Detailed description of how and why the system reached undervoltage if known. Include the information of when the system was installed and commissioned and in which circumstance and when the undervoltage happened. If the battery was never running before: Why did it never work before, and what was the battery's status when the battery was left (on / off / LED) 

      - Inverter model, serial number and inverter logs 

   - Access to the inverter portal (add info@eft-systems.de and provide the name of the system in the portal) 

### **2.11 Identifying a faulty module / Module exclusion method** 

#### **The module quantity must be adjusted in the app whenever the number of modules is changed!** 

1. Install the Battery-Box system complying with the minimum quantity requirement (HVS: 2 modules, HVM: 3 modules). 

**2. Check System. If Okay** , add one module at a time, adjust the module number in the app and check again. 



**3. If not okay** : The faulty module is probably one of the modules in the tower. Take one of the spare modules and exchange each of the remaining modules with the spare module one at a time. Check the battery status after each step. If battery status turns to “OK”, the faulty module is the one that was exchanged. 





14

<!-- pág. 15 -->
## 3. SERVICE TASKS 

Please go through the general steps beforehand, see chapter 1. 

### **3.1 BCU replacement** 

**Have you detected a faulty BCU?** 

After replacing the BCU, please remember to redo the configuration and firmware-update with the app or BCP. 

### **3.2 Module Replacement** 

#### **Have you detected a faulty module?** 

In the meantime, you can continue to use the battery system with the remaining modules and a correspondingly reduced capacity (taking into account the minimum number of modules). Please note: It is important that all modules of a battery tower have a similar state of charge (SOC) with a tolerance of 5%. New modules have about **30** % SOC. If the remaining modules have not yet been put into operation (not charged / discharged), the new module can be easily added. Otherwise, it is basically a module extension. In this case, please add the new module to the system only when the SOC of the system is between 25% and 35% (see extension process in the O perating M anual). Make sure to configure correctly after any change to the module quantity. 





15

<!-- pág. 16 -->
|**BYD Battery-Box Premium HVS&HVM Service Checklist - V1.1 EN**|
|---|



|Important: The installation and all other kinds of works or measurements in combination with the BYD Battery-Box are only<br>i|
|---|
|allowed by professional and qualified electricians. Improper handling can cause danger and damage. This document does<br>fi|
|not replace the official BYD manuals and documents. No responsibility is accepted for the accuracy of the information.|



> ⚠ REVISAR TABLA — pág. 16: celda partida (paréntesis sin cerrar; posible celda combinada cortada)
|**1.**<br>**GENERAL STEPS**<br>Please carefully check<br>**all**<br>“General Steps“ from page 3 of the Service Guideline and confirm this in t|i   he boxes below|
|---|---|
|1.1 Configuration<br>1.4Latest Firmware<br>1.7|Correct Operation|
|1.2 Only HVS or HVM<br>1.5App Configuration||
|1.3 External Connections<br>1.6Proper Restart||
|**2.**<br>**ERROR RELATED ANALYSIS**<br>Please mark the**error related**Analysis from Chapter 2 of the Service Guideline that you checked, a<br>information related to those Sections|nd collect all the|
|2.5 SOC & charging logic<br>2.1 BCU shows no reaction / No LED|2.9 BCU LED event code (EC)|
|2.6 Unexpected shutdown<br>2.2 BCU switch cannot be flipped up / LED remains on|2.10 Voltage measurement<br>|
|2.7 Module Extension /<br>Parallel connection<br>2.3 Problem with FW Update / App Configuration / Battery Wi-Fi|and undervoltage<br>211 Identifin a fault|
|<br> <br>2.4 Battery <> Inverter communication / no charging or<br>|. yg  y<br>module / Module<br>|
|2.8 Be Connect Plus (BCP)<br>discharging|exclusion method|
|**3.**<br>Please fill all available information in below table. Some information like the Serial Number of the B<br>**SERVICE INFORMATION**|i               CU is mandatory to receive service.|
|**•**<br>**Service Ticket Number or System ID:**||
|**•**<br>**Installer / Delivery Address / Contact:**||
|Company<br>ZIP / City||
|Contact Person<br>Phone||
|Street / Nr.<br>Email||
|**•**<br>**System Information**||
|BMU Firmware<br>Battery Configuration (e.g., HVS5.1 / 2xHVM11.0 /...)||
|BCU Serial Number<br>BMS Firmware||
|BCU Connected to Internet<br>Inverter Firmware<br>Yes<br>No||
|Inverter Brand + Model<br>System Name on||
|<br> <br>Inverter Portal||
|Inverter Serial Number<br> <br>( Provide access for: i|nfo@eft-systems.de )|
|Commissioning Date<br>||
|**•**<br>**Service Information**||
|BCU EventCode (EC)<br>Inverter Error Code||
|Was the battery charging / discharging before (was the system working normally before?)|Yes<br>No|
|Take pictures of open communication port in the BCU and Inverter clearly showing connection cable|s|
|Get Data of the Battery-Box with the Be Connect Plus (BCP) Program (see chapter 2.8)||
|Description of<br>the Problem<br>Please provide any additional information that is necessary or could help in the analysis of the servic<br>module, video of a special behaviour; pictures; app screenshots; module voltages... )|e case (e.g., serial number of a wron|
|By contacting us you confirm, that a qualified person has done the necessary control and collected all available|i   i           information above.|
|Service Contact:<br>Europe: EFT-Systems GmbH<br>Australia:  Alps Power<br>www.eft-systems.de<br>www.alpsp<br>ri@fttmd<br>ri@l|Pty Ltd<br>ower.com.au<br>rm|
|sevcee-syses.e<br>sevcea<br>+49 9352 8523999<br>+34 9106 02267 (ES)<br>+61 02 800<br>|spowe.co.au<br>5 6688|
|+44 2037 695998 (UK)        +39 0287 368364 (IT)<br>For Europe only: Register Ticket directly in the Online Service Center: https://support.eft-systems.de/|184361|



|Please provide any additional information that is necessary or could help in the analysis of the service case (e.g., serial number of a wrong<br>module, video of a special behaviour; pictures; app screenshots; module voltages... )|
|---|



|18436136-00|
|---|
