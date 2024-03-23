# Ender 3 V2 Config
Marlin configuration for my Ender 3 V2 based on these repositories by @mriscoc

https://github.com/mriscoc/Ender3V2S1/tree/Ender3V2S1-Released
https://github.com/mriscoc/Special_Configurations

My additions:
- Changed version, printer name and other parameters because it looks cool to have my name on my printer firmware
- 300 degree hotend config since I installed a bimetallic heatbreak
- Added more preheat profiles

![Minimal config](https://github.com/Pelochus/Ender3-V2-Config/blob/main/images/Minimal-Config.png)

## Procedure
Follow the guide in the [Special_Configurations](https://github.com/mriscoc/Special_Configurations) repo by @mriscoc. In short:
- Clone this repo after syncing it to the original fork (or clone the original)
- With pythonw, execute ```Configurator.pyw```: ```pythonw Configurator.pyw```
- Press Set config and Generate
- Use the config in the photo above
- Now add extra config to the ```Configuration.h```, ```Configuration_adv.h``` and ```Version.h``` files. See example in this repo
- Clone this [repo](https://github.com/mriscoc/Ender3V2S1/tree/Ender3V2S1-Released) and change the previous file
- Compile using PlatformIO and Auto Build for Marlin extensions for VSCode
- For this step, you can check any guide for compiling Marlin online
- Flash to the printer: Turn off printer and insert SD card with only .bin file with a specific name (cannot be something already used before for updating)
- ???
- Profit
