# Ender 3 V2 Config
Marlin configuration for my Ender 3 V2 based on these repositories by @mriscoc

- https://github.com/mriscoc/Ender3V2S1/tree/Ender3V2S1-Released
- https://github.com/mriscoc/Special_Configurations

My additions (new for V1.1):
- **New:** Changed default max Z and Extruder speeds from 10 to 20 and 45 to 100 mm/s respectively
- **New:** Changed default max accelerations from 500, 500, 100 and 1000 to 2500, 2500, 200 and 3000 (X, Y, Z, E)
- **New:** Changed default accelerations from 500 to 750 (axes), 800 to 1000 (retractions) and 1000 to 1500 (travel)
- **New:** Changed default BLTouch probe offset to this link's recommendations: https://www.thingiverse.com/thing:4462870
- **New:** Reduced max Z height to 220 due to physical constraints on my machine
- **New:** Changed default ESteps from 93 to 139, since I have a dual drive full-metal extruder
- **New:** Mildly optimised defaults for firmware retractions (shorter lengths, slightly faster)
- **New:** Enabled power-loss recovery by default
- Changed version, printer name and other parameters because it looks cool to have my name on my printer firmware
- 300 degree hotend config since I installed a bimetallic heatbreak
- Added more preheat profiles

Download from releases page:
https://github.com/Pelochus/Ender3-V2-Config/releases/latest

![Minimal config](https://github.com/Pelochus/Ender3-V2-Config/blob/main/images/Minimal-Config.png)

## Procedure
Follow the guide in the [Special_Configurations](https://github.com/mriscoc/Special_Configurations) repo by @mriscoc. In short:
- Clone this repo after syncing it to the original fork (or clone the original)
- With pythonw, execute ```Configurator.pyw```: ```pythonw Configurator.pyw```
- Press Set config and Generate
- Use the config in the photo above
- Now add extra config to the ```Configuration.h```, ```Configuration_adv.h``` and ```Version.h``` files. See example in this repo
- In ```platformio.ini``` file, use ```STM32F103RE_creality```, since I checked that I have the 512 kB STM (the RC is the 256 kB flash). This step is also mentioned in the original README in Special_Configurations repo
- Clone this [repo](https://github.com/mriscoc/Ender3V2S1/tree/Ender3V2S1-Released) and change the previous files (Configurations, version and platformio.ini)
- Compile using PlatformIO and Auto Build for Marlin extensions for VSCode
- For this step, you can check any guide for compiling Marlin online
- Flash to the printer: Turn off printer and insert SD card with only .bin file with a specific name (cannot be something already used before for updating)
- ???
- Profit

## Credits
To the Marlin team and [@mriscoc](https://github.com/mriscoc)
