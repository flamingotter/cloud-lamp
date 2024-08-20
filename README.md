# 3D-Models

* Use the the "small-plate" version for build plates under 250x250mm

* All versions have to printed and tested on a Bambulabs P1S using standard PLA filament. 

* White or lighter color filament will diffuse the light best.

* 1 or 2 LED Pixels may need to be trimmed from the far end ->

* Slicer settings - 0.2 Layer height, 15% infill "Grid", 5mm Outer brim for adhesion.


## BOM
* [WLED Controller](https://www.athom.tech/blank-1/wled-2812b-led-strip-controller)
* [Side Emitting LED Strip - 5mm 72LEDs-M - 1m](https://www.aliexpress.us/item/3256804326430015.html)
* [5v Power Supply](https://amzn.to/3uoYYFV)

![Cloud Lamp in action](https://github.com/flamingotter/cloud-lamp/blob/main/images/cloud_lamp.jpg)


## Preset Config for Power on/off and Preset Scroll with physical button
### Power Toggle
1. From WLED App click "Presets"
2. Click "+ Preset"
3. Name preset "Power"
4. Uncheck "Use current state"
5. Paste into "API command" `T=2`
6. "Save to ID" `250`
7. Click "Save"

### Scroll Presets
1. From WLED App click "Presets"
2. Click "+ Preset"
3. Name preset "Scroll Preset"
3. Uncheck "Use current state"
4. Paste into "API command" `win&P1=1&P2=3PL=~` (Replace values of P1 and P2 with the first and last Present IDs that you want to scroll through)
5. "Save to ID" `249`
6. Click "Save"

### Configure Button
1. From WLED App click "Config"
2. Click "Time & Macros"
3. Scroll down to ["Button Actions"](https://github.com/flamingotter/cloud-lamp/blob/main/images/button_config.png)
4. For "Button 0" enter value `249` for "short on->off"
5. For "Button 0" enter value `250` for "long on->off"
6. Click "Save"
