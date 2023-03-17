# Stiffy Toolhead for the Ender 3

This is a complete toolhead for the Ender 3 that incorporates the Sherpa Mini (or Micro), QuickDraw, dual 5015 part cooling fans, and the stock Creality hotend.

![Image of Stiffy](./Images/Stiffy.png)


## Parts Required

**Required**

- [Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder/) with [housing_front_k](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder/blob/master/STLs/FDM_STLs/optional_parts/%5Ba%5D_housing_front_k_x1_rev5.STL)
- 1x 4010 or 4020 axial fan
- 2x 5015 blower fan
- Creality Hotend or Phaetus BMS (7 fin) Hotend
- 4x M3X20mm
- 2x M3x25mm
- 2x M3x16mm
- 2x M3x12mm
- 3x M3x6mm
- 4x M3 nuts
- 5x Heatset Inserts (3x5x4mm)

**Assembly**

- See [Images](./Images)

**Optional**

- 60W or greater heater cartridge (the increased cooling can overwhelm the stock 40W heater when printing at 15mm^3/s, 220C, 100% fan)
- [QuickDraw](https://github.com/Annex-Engineering/Quickdraw_Probe) 
	- Print, assemble, and install Quickdraw, dock, and holder (see [CAD](./CAD/Stiffy.EASM))
		- Set the X position of dock between the X home position and the bed with the opening facing left. There should be 2mm between the bed and the back of the dock using the stock X endstop. Using the optional x_endstop_mount.stl will allow 12mm between bed and dock. 
		- Set the Y position of dock so that Stiffy's magnets are aligned with QuickDraw's magnets when it is docked.
		- Set the Z position of the dock so that Stiffy's and QuickDraw's magnets barely touch after homing Z with the stock Z endstop. There is an optional replacement for the stock Z endstop bracket that can be used to mount the switch next to the dock holder. 
	- [Configure Klipper](./QuickDraw_klipper_config.cfg) to use Dalegaard's XZ dockable probe module
	- Note: The stock endstop locates the dock height then QuickDraw defines Z0 once the homing routine is complete.
	- Homing video: 

[![Homing video](https://img.youtube.com/vi/NMOQogjF0p8/0.jpg)](https://youtu.be/NMOQogjF0p8)
- BLTouch
	- Use [BLTouch_4010_Mount.STL](./STLs/Optional/BLTouch_4010_brace.STL)
	- Remix of [Hairing's fan mounted BLTouch](https://www.thingiverse.com/thing:4617163)



**Neptune 2 version**

For the Elegoo Neptune 2 (and potentially 2D/2S), print [Stiffy_Neptune2.stl](./STLs/Stiffy_Neptune2.stl) instead of [Stiffy_E3V2.stl](./STLs/Stiffy_E3V2.stl). Otherwise all assembly details are the same as the Ender 3 version.