# Optimized firmware for the Artillery Sidewinder X1 touch display  
  
The Artillery Sidewinder X1 has an Makerbase MKS-TFT 3.2 Touch-Display build in and is delivered with [this Firmware](http://www.artillery3d.com/DownLoad/15689.html)   
The Firmware for the MKS-TFT touch display is only available as [precompiled firmware](https://github.com/makerbase-mks/MKS-TFT/tree/master/MKS-TFT2.8-3.2 ) so adjustments / extensions are limited ...  

## Requirements  
You need the [ASWX1-FW-MOD](https://github.com/pinguinpfleger/ASWX1-FW-MOD) or at least a firmware with enabled eeprom and babystepping.  

## RELEASES

29.02.2020 [ASWX1-TFTFW-MOD-v1.1](https://github.com/pinguinpfleger/ASWX1-TFTFW-MOD/releases/tag/ASWX1-TFTFW-MOD-v1.1) - [ASWX1-TFTFW-MOD-v1.1.zip](https://github.com/pinguinpfleger/ASWX1-TFTFW-MOD/releases/download/ASWX1-TFTFW-MOD-v1.1/ASWX1-TFTFW-MOD-v1.1.zip) based on MKS TFT28_32_v3.0.3  
*Changed some Icons with FoodFighters Version*  
           
29.02.2020 [ASWX1-TFTFW-MOD-v1.0](https://github.com/pinguinpfleger/ASWX1-TFTFW-MOD/releases/tag/ASWX1-TFTFW-MOD-v1.0) - [ASWX1-TFTFW-MOD-v1.0.zip](https://github.com/pinguinpfleger/ASWX1-TFTFW-MOD/releases/download/ASWX1-TFTFW-MOD-v1.0/ASWX1-TFTFW-MOD-v1.0.zip) based on MKS TFT28_32_v3.0.3  
  
## Added Features  
  
1. **P.I.D. Autotune**   
   PID Tuning improves your hotend/bed temperatur stability and will positively impact print quality.     
   This command initiates a process of heating and cooling to determine the proper PID values for your hotend.  
   This may take up to 5-10 minutes.    
   Make sure you wait!   
   Default for nozzel is set to 220°C which is the middle of PLA and PETG default nozzel temperatures.  
   Default fur bed is set to 72°C which is the middle of PLA and PETG default bed temperatures.  
   You can edit this in [this line in mk_config.txt](/sd-card/mks_config.txt#L187).  
  
2. **Preheat Presets for PLA and PETG**  
   Let you easily preheat to given presets, you can change the temps in the mks_config.txt.  
   Default for [PLA](/sd-card/mks_config.txt#L199) is 205°C Nozzle and 60°C Bed `M104 S205; M140 S60;`  
   Default for [PETG](/sd-card/mks_config.txt#L202) is 235°C Nozzle and 85°C Bed `M104 S235; M140 S85;`  

3. **Manual Bed Leveling**  
   Manual Bed Leveling Homes(G28) and turns off all stepper motors except Z-Motors.  
   Now you can freely move your hotend to the desired positions.  
   I find this helpful for initial bed leveling as you can carefully move your printhead.  
   Do not forget to preheat bed and hotend for accurate leveling.  
   You can use Z+ and Z- commands to drive the head up or down overall.  
     
4. **Live Adjust Z / Babystepping Z**  
   During printing the first layer you can still adjust the distance between the nozzle and the print-bed.   
   E.g. if you find  your print is not sticking you can carefully step down the nozzle or correct it up again   
   without the need to relevel all four screws at the same time.  
   However, this assumes the bed is in level overall but maybe just a little too low or too high overall.  
   

## SCREENSHOTS  

### Boot & Startscreen
<img src="/README.MD_files/1_boot.jpg" align="left" width="45%"/>
<img src="/README.MD_files/2_start.jpg" width="45%"/>  

### Tools  
<img src="/README.MD_files/3_tools.jpg" align="left" width="45%"/>
<img src="/README.MD_files/4_tool_heat.jpg" width="45%"/>  
<img src="/README.MD_files/5_tool_extrusion.jpg" align="left" width="45%"/>
<img src="/README.MD_files/6_tool_move.jpg" width="45%"/>  
<img src="/README.MD_files/7_tool_home.jpg" align="left" width="45%"/>
<img src="/README.MD_files/8_tool_leveling.jpg" width="45%"/>  
<img src="/README.MD_files/9_tool_change.jpg" align="left" width="45%"/>
<img src="/README.MD_files/10_tool_more.jpg" width="45%"/>  

### Settings  
<img src="/README.MD_files/11_settings.jpg" align="left" width="45%"/>
<img src="/README.MD_files/12_settings_files.jpg" width="45%"/>  
<img src="/README.MD_files/13_settings_wii.jpg" align="left" width="45%"/>
<img src="/README.MD_files/14_settings_fan.jpg" width="45%"/>   
<img src="/README.MD_files/15_settings_about.jpg" width="45%"/>   

## Individual Adjustments  
Adjustments can be made via the [mks_config.txt](/sd-card/mks_config.txt).  

## Flashing  
Simply copy all files in the [sd-card folder](/sd-card/) to a microSD-Card, insert to your printer and reboot printer, wait until process is finished.  


## TIPPS  
- In case your USB Stick does not work anymore after the upgrade, check the following option on your TFT: SET/File/USB.  
That was always there but defaulted back to SD after TFT Upgrade.
- You can simply upload the modified mks_config.txt to the tft, just copy this file to sd and reboot. You do not need to copy all the other files, its a lot faster.

## Credits  
The repository here is the continuation of the TFT-Firmware from [**Robscar's firmware mod** at Thingiverse](https://www.thingiverse.com/thing:3856144) and the remix from [FoodFighter](https://www.thingiverse.com/FoodFighter).  

The modified Marlin firmware for the Artillery Sidewinder X1 has been seperated to an own repository:  
https://github.com/pinguinpfleger/ASWX1-FW-MOD

