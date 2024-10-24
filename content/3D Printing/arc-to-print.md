---
title: arc's Printing Ideas
date: 2024-08-14
draft: false
---

## Queue

- [x] [Raspberry Pi B case](https://www.thingiverse.com/thing:4384009)
- [x] Ring stand (Taro filament)
- [x] [Outlet blank cover](https://www.printables.com/model/593140-electrical-wall-plates-outlet-covers-and-light-dim) for bedroom
- [ ] re-print [toothpaste squeezer](https://www.thingiverse.com/thing:1147252) shaft
- [ ] Razer Naga panel stand (truncated to 2-wide grid)
  - [x] bottom
  - [ ] top

## Wishlist

- X2HR accessories
  - microphone mount: [1](https://www.printables.com/model/698366) [2](https://makerworld.com/en/models/392909)
  - [ear pad rings](https://www.thingiverse.com/thing:4887941)
  - [end caps?](https://www.printables.com/model/935338)
- Bedside cup and/or water bottle holder
- Parchment paper roll holder
- Laptop vertical storage stand
- Print/design enclosure for LED strip power supply
- mangetic cable management clip things (ltt style?)

## Printer Improvements

- [ ] [Probe Calibration](https://www.klipper3d.org/Probe_Calibrate.html#repeatability-check)
- [x] try out the `SEARCH_VARS` macro
- [x] calculate difference between toolhead current position, probe last position, etc
- what is `M82` and `M83` sets extruder to relative and `M82` undoes it?
- how does `G92 E0` work?
- [ ] printer should be able to home at back of bed
  - [ ] include as part of the resume print workflow if not homed
  - `M84` stops motors and loses position
    - is `M18` implemented?
- [ ] improved start macro
  - heat roughly to 160 while waiting for bed
  - draw line while heating nozzle to prevent curling
  - retract slightly at end of print (`G1 E-10` for 10mm for example?)
- [ ] babystepping UI via `SET_GCODE_OFFSET MOVE=0 X_ADJUST=+0.005`?
- check why printer bed axis is crunchy sounding when printing sometimes...
  bedslinger(y) accel or jerk may be set too high?
