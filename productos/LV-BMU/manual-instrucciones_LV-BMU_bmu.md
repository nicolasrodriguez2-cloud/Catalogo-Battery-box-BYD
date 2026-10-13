# Battery-Box Premium LV BMU — Manual de instrucciones

- **Producto:** Battery-Box Premium LV BMU (LV BMU)
- **Tipo de documento:** Manual de instrucciones
- **Versión/fecha del PDF:** V1.2 / 2024-02-20
- **URL de origen:** https://www.bydbatterybox.com/uploads/downloads/240220_BYD%20Battery-Box%20Premium%20LV%20BMU%20Instruction%20Manual%20V1.2-65e181e151fcd.pdf
- **SHA-256 del PDF:** 2770d0e216b35ae0bf7fbf93e21511cae758a2c107f435a79f339b8bc1880660
- **Idioma:** no indicado en el nombre
- **Archivo PDF local (no versionado):** _descargas/240220_BYD Battery-Box Premium LV BMU Instruction Manual V1.2-65e181e151fcd.pdf
- **Conversión:** pymupdf4llm 1.28.2, 4 págs.


---
<!-- pág. 1 -->
# **BYD Battery-Box Premium LV BMU Instruction Manual** 

V1.2 

## **VALIDITY** 

This document is valid for the BYD Battery-Box Premium LV BMU (Battery Management Unit) (“BMU”) from firmware version 1.0. 

## **INTENDED USE** 

BMU is applicable for the BYD Battery-Box Premium LV system(s) (LVS 4.0, LVS 8.0, LVS 12.0, LVS 16.0, LVS 20.0, LVS 20.0 and LVL 15.4) (“Battery-Box”), and works as a control unit for the system(s). 

## **PRODUCT DESCRIPTION** 

BMU is equipped with WLAN.The APP Be Connect 2.0 could communicate with BMU through the WLAN. 









<!-- Start of picture text -->
BMS INVERTER ETHERNET<br>A B C D<br><!-- End of picture text -->

- **A:** RJ45 port for connection with Battery-Box 

- **B:** RJ45 port for connection with an inverter 

- **C:** Ethernet port 

- **D:** LED Button 

The WLAN name and password are on the label of BMU. 

1

<!-- pág. 2 -->
### Assignment of Port B 



|No.|Assignment|
|---|---|
|1|Unused|
|2|Unused|
|3|Unused|
|4|CAN H|
|5|CAN L|
|6|Unused|
|7|Unused|
|8|Unused|



## **SCOPE OF DELIVERY** 

- 1×BMU 

- 1×Instruction Manual 

## **TECHNICAL DATA** 

|Communication|Ethernet/CAN|
|---|---|
|Input voltage*|40-60 V|
|Input current|200 mA|
|Weight|3 kg|
|Dimensions (L×W×H)|250 mm×122 mm×50 mm|
|Ambient temperature in operation|-10°C to 50°C|
|Relative humidity (non-condensing)|5% to 85%|
|Degree of protection (in accordance with IEC 60529)|IP20|



*BMU is powered by Battery-Box through the network cable. No other power supply is needed. 

## **CONNECTION DIAGRAM** 



<!-- Start of picture text -->
BMS INVERTER ETHERNET<br><!-- End of picture text -->



<!-- Start of picture text -->
NOTICE<br>Please don’t ground BMU<br>or Batter-Box at an inverter.<br><!-- End of picture text -->

2

<!-- pág. 3 -->
1. Detailed connection instructions with inverters could be read in the Battery-Box Quick Start Guide. 

2. The communication cable between BMU and an inverter cannot be longer than 10 meters. And the cable should be CAT 5 shield or above. 

3. Please make sure the correct pins are connected between BMU and an inverter. 

4. The connection between BMU and Battery-Box should be the Straight-Through Wired Cable. 

5. Connected to the Internet is highly recommended. 

6. The WLAN of BMU will switch off in 5 hours from turning on. 

Press the LED Button once when BMU is on could activate the WLAN again. 

Press the LED Button three times in six seconds, each time around 1 second could reset the WLAN. 

## **MOUNTING** 

Install BMU on the wall or a rack. The recommended expansion screw size is M4×12. The minimum distance from the ground is 50 mm. 

## **COMMISSIONING** 



<!-- Start of picture text -->
BMS INVERTER ETHERNET<br>50mm<br><!-- End of picture text -->

1. Make sure an inverter, Battery-Box, and BMU are correctly connected. 

2. Press the LED Button on Battery-Box for 3 seconds. 

3. Refer to Battery-Box Operating Manual for further steps. 

## **Updating FIRMWARE** 

The firmware of BMU could only be updated when it operates with Battery-Box.Please refer to Battery-Box Operating Manual for further information. 

## **LED STATUS** 

|Blinking<br>white<br>and blue<br>alternately|ON<br>OFF<br>ON<br>OFF<br>White<br>Blue|0.5s<br>0.5s|The<br>battery<br>system<br>is<br>initiating.|
|---|---|---|---|
|Solid<br>white|ON<br>OFF<br>ON<br>OFF<br>White<br>Blue||Idle<br>(the<br>battery<br>system<br>is<br>neither<br>charging<br>nor<br>discharging).|
|Blinking<br>white<br>slowly|ON<br>OFF<br>ON<br>OFF<br>White<br>Blue|2s<br>2s|The<br>battery<br>system<br>is<br>charging.|
|Blinking<br>white<br>quickly|ON<br>OFF<br>ON<br>OFF<br>White<br>Blue|1s<br>1s|The<br>battery<br>system<br>is<br>discharging.|
|Blinking<br>white<br>and<br>solid<br>blue|ON<br>OFF<br>ON<br>OFF<br>White<br>Blue|1s<br>1s|The<br>battery<br>system<br>is<br>discharging,and<br>the<br>SOC<br>is<br>below<br>15%.|
|Blinking<br>white<br>and<br>blue|ON<br>OFF<br>ON<br>OFF<br>White<br>Blue|1s<br>1s<br>......<br>N|An<br>error<br>has<br>occurred<br>(refer<br>to the<br>Service<br>Guideline<br>and Checklist<br>for<br>further<br>details)|



**When an error happens, refer to the Operation Manual of the corresponding Battery-Box for the more details. 

3

<!-- pág. 4 -->
## **DISPOSAL** 

Following the applicable regulations for electronic waste to dispose of BMU. 

## **CONTACT** 

|**BYD Global Service**||
|---|---|
|Email|bboxservice@byd.com|
|Telephone|+86 755 89888888-47175|
|Address|No.3009, BYD Road, Pingshan, Shenzhen, 5118118, P. R. China|
|Website|www.bydbatterybox.com|
|Social Media Link|https://www.facebook.com/BatteryBoxBYD<br>https://twitter.com/BYD_BatteryBox|
||https://www.linkedin.com/company/byd-battey-box|
|**Europe**|**EFT-Systems GmbH**|
|Email|service@eft-systems.de|
|Telephone|+49 9352 8523999|
||+44 (0) 2037695998 (UK)<br>+34 91 060 22 67 (ES)<br>+39 02 87368364 (1T)|
|Address|Bruchtannenstr. 28, 63801 Kleinostheim, Germany|
|Website|www.eft-systems.de|
|**Australia**|**Alps Power Pty Ltd**|
|Email|service@alpspower.com.au|
|Telephone|+61 2 8005 6688|
|Address|2/62 Belmore Road, Riverwood, NSW 2210|
|Website|www.alpspower.com.au|
|**South Africa**|**Afriplus Energy Group (Pty) Ltd**|
|Email|support@afriplusenergy.co.za|
|Telephone|+27 21 140 3594|
|Address|The Pavilion, Corner Of Dock & Portswood Road, V&A Waterfront, 8001, Cape Town|
|Website|www.afriplusenergy.co.za|
|**USA**|**BYD US Service**|
|Email|us.homeenergy@byd.com|
|Telephone|626-491-2333|
|Address|888 E Walnut St,Pasadena,CA 91101 United States|



**Copyright © Shenzhen BYD Electronics Co., Ltd. All right is reserved.** 

4
