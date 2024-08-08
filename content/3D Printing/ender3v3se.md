---
title: Ender 3 V3 SE
date: 2024-08-03
draft: false
---

# Slicer Configuration

* I've been using [Ultimaker Cura](https://ultimaker.com/software/ultimaker-cura/) as the slicer for this printer, though I've edited the start and end gcode to be `START_GCODE` and `END_GCODE` respectively so that Klipper can handle the start and end automation alongside having changed the bed to the full 230x230mm size.
* I also use [OctoPrint Connection](https://marketplace.ultimaker.com/app/cura/plugins/fieldofview/OctoPrintPlugin) for Cura so that it can hook up to the pretend OctoPrint API running on Moonraker.
	* To generate an API key for the plugin, go to the Fluidd authentication settings and hit API key.

# Equipment

* [Replacement extruder silicone socks](https://www.amazon.ca/gp/product/B0CJTZTZ9S)
  * This should not necessarily need replacing unless it breaks.
* [High speed 0.4mm and 0.6mm nozzles](https://www.amazon.ca/gp/product/B0B5N1C8FB)
  * Please change your slicer settings if you switch to a 0.6mm nozzle.
  * [Creality Nozzle Replacement Video](https://www.youtube.com/watch?v=xTZfIqY6NMY)
* [Dual-sided printing platform, glossy PET and coated PEI](https://www.amazon.ca/gp/product/B0CQNVKWYZ)
  * The PET sticker surface is the patterned surface, which tolerates up to 80C and is good for PLA, PETG and TPU.
  * The coated PEI is the frosted surface and can be used for PLA, PETG, ABS, TPU, ASA, PET, PA, PC, ...
# Failed Upgrades

## LED Strip

[Product Page](https://www.amazon.ca/gp/product/B0CM3KT9CY)

Current status:
* An attempt at performing the install occurred on 2024-08-02.
* The aluminium frame binding against the plastic caused the wires for the power to short 24V to ground and be broken in the process.
* The wires that hook up to the power supply need to be replaced in some fashion.

## Filament Runout Sensor

[Product Page](https://www.amazon.ca/gp/product/B0CP5ZFCGN)

Current status:
* An attempt at performing the install occurred on 2024-08-02.
* The aluminium frame binding against the plastic caused the wires for power and data to be broken in the process.

# Calibration

## Bed Levelling

The tune section of the Fluidd interface is relevant for generating a bed mesh. It uses the CR Touch probe attached to the printer to figure out the discrepancies in bed flatness.

![Bed levelling infographic. If you are quite visually impaired, I think it will be very hard to understand this anyway so possibly don't worry about it. Textural demonstrations of "too close" and "too far" might be better?](bed-levelling.jpeg)

## Z-offset

The ideal distance from the nozzle to the bed is 0.15mm. This is the value you mostly need for this printer. The probe generally takes care of the rest now and has a static offset from the nozzle itself.