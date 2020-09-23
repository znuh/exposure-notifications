# exposure-notifications
Visualizer for Covid-19 Exposure Notifications

To remake Exposure Notifications you need to get/make four things:
- a BBC micro:bit or Calliope Mini with the [microbit-corona-scanner](https://github.com/znuh/microbit-corona-scanner) installed
- a black 23x23cm RIBBA frame from IKEA
- the printed circuit board for the LEDs - see the leds/ directory of this repository
- the printed circuit board for the LED matrix controller - **either** matrixctl-v1 **OR** matrixctl-v2
  - matrixctl-v2 includes a socket for the micro:bit and a switching voltage regulator
  - matrixctl-v1 comes without a socket for the micro:bit and has no switching voltage regulator
  - v2 is more efficient and keeps the LED matrix driver cooler when more LEDs light up - therefore I recommend using v2

The printed circuit board designs are made with a **Nightly Development Build** of [KiCAD](https://kicad-pcb.org/).
If you want to open/edit them you also need a recent Nightly Development Build. If you just want to use the PCBs unmodified you can also use the gerber-files from the gerber-subdirectories.

## LED matrix board
The LED matrix board uses Würth 150141RV73100 LEDs. These are bicolor-LEDs but only the red LED is used.
The landing pads for the LEDs have been reduced to a minimum to hide the pads underneath the LEDs. All PCB tracks are on the back side of the PCB. 1206 0-Ohms resistors are used instead of vias to cross tracks.
![LED matrix front side](leds/leds.jpg)
![LED matrix back side](leds/leds-bot.jpg)
