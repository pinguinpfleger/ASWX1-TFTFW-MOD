# Optimized firmware for the Artillery Sidewinder X1 touch display  
  
The Artillery Sidewinder X1 has an Makerbase MKS-TFT 3.2 Touch-Display build in and is delivered with this Firmware [link](http://www.artillery3d.com/DownLoad/15689.html)   
The Firmware for the MKS-TFT touch display is only available as precompiled firmware [link](https://github.com/makerbase-mks/MKS-TFT/tree/master/MKS-TFT2.8-3.2 ) so adjustments / extensions are limited ...  

## Requirements  
You need the [ASWX1-FW-MOD](https://github.com/pinguinpfleger/ASWX1-FW-MOD) or at least a firmware with the enabled feature that are used with the ASWX1-TFTFW-MOD.  

## RELEASES

##.02.2020 ASWX1-TFTFW-MOD-v1.0 based on MKS TFT28_32_v3.0.3


## Added Features  
  
1. **P.I.D. Autotune**   
   PID Tuning improves your hotend/bed temperatur stability and will positively impact print quality.     
   This command initiates a process of heating and cooling to determine the proper PID values for your hotend.  
   This may take up to 5 minutes.  
   During the tuning process the LED will stay Red.  
   Once the process is finished, the LED will turn Green.   
   Make sure you wait!   
   Default for nozzel is set to 220°C which is the middle of PLA and PETG default nozzel temperatures.  
   Default fur bed is set to 72°C which is the middle of PLA and PETG default bed temperatures.  
   You can edit in [this line in mk_config.txt](/sd-card/mks_config.txt#L187)  
  
2. **Preheat Presets for PLA and PETG**  
   Let you easily preheat to given presets, you can change the temps in the mks_config.txt.  
   Default for [PLA](/sd-card/mks_config.txt#L199) is 205°C Nozzle and 60°C Bed `M104 S205; M140 S60;`  
   Default for [PETG](/sd-card/mks_config.txt#L202) is 235°C Nozzle and 85°C Bed `M104 S235; M140 S85;`  

3. **Manual Bed Leveling**  
   Manual Bed Leveling Homes(G28) and turns off all stepper motors except Z-Motors.  
   Now you can freely move your hotend to the desired positions.  
   I find this helpful for initial bed leveling as you can carefully move your printhead.  
   Do not forget to preheat bed and hotend for accurate leveling.  
   You can use Z+ Z- commands to drive the head up or down overall.  
     
4. **Live Adjust Z / Babystepping Z**  
   During printing the first layer you can still adjust the distance between the nozzle and the print-bed.   
   E.g. if you find  your print is not sticking you can carefully step down the nozzle or correct it up again   
   without the need to relevel all four screws at the same time.  
   However, this assumes the bed is in level overall but maybe just a little too low or too high overall.  
   

## SCREENSHOTS  

### TOOLS
<img src="/README.MD_files/boot.jpg" align="left" width="45%"/>
<img src="/README.MD_files/start.jpg" width="45%"/>
<img src="/README.MD_files/tools.jpg" align="left" width="45%"/>
<img src="/README.MD_files/more.jpg" width="45%"/>  
<img src="/README.MD_files/move.jpg" align="left" width="45%"/>
<img src="/README.MD_files/leveling.jpg"  width="45%"/>  
<img src="/README.MD_files/filament.jpg" align="left" width="45%"/>  
<img src="/README.MD_files/extrude.jpg" width="45%"/>  
<img src="/README.MD_files/heat.jpg" width="45%"/>  

### Settings  
<img src="/README.MD_files/settings_1.jpg" align="left" width="45%"/>
<img src="/README.MD_files/settings_filesys.jpg" width="45%"/>
<img src="/README.MD_files/settings_about.jpg" align="left" width="45%"/>
<img src="/README.MD_files/settings_wifi.jpg" width="45%"/>  


## Individual Adjustments  
Adjustments can be made via the [mks_config.txt](/sd-card/mks_config.txt).  

## Flashing  
Simply copy all files in the [sd-card folder](/sd-card/) to a microSD-Card, insert to your printer and reboot printer, wait until process is finished.  


## TIPPS  
In case your USB Stick does not work anymore after the upgrade, check the following option on your TFT: SET/File/USB.  
That was always there but defaulted back to SD after TFT Upgrade.  

## Credits  
The repository here is the continuation of the TFT-Firmware from [**Robscar's firmware mod** at Thingiverse](https://www.thingiverse.com/thing:3856144) and the remix from [FoodFighter](https://www.thingiverse.com/FoodFighter)  

The modified Marlin firmware for the Artillery Sidewinder X1 has been seperated to an own repository:  
https://github.com/pinguinpfleger/ASWX1-FW-MOD

