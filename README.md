# CyberHUD
Prototyping Heads Up Display for the windshield of Cybertruck

Based on a cybertruck [community discussion](https://www.cybertruckownersclub.com/forum/threads/heads-up-display.20073/post-385728)

# Wish list

Some of the initial list of desirable features shared by cybertruck drivers:
- Improve convenience and danger of running out of battery by showing low battery warning (Below 20%, 10%, 5%). Currently batttery level is shown on main screen on a small icon at the top. It is possible to miss if driver is exclusively focused on the road especially in peak traffic environment.
- Improve safety by showing max speed exceeded warning (maybe with a 10% tolerance). Currently speed and max speed are shown in a relatively small area in the top left of the main screen. In a busy traffic situation, it is possible for the driver to not notice that they are exceeding max legal speed limit. Especially after passing or while following speeding cars in front.
- Improve safety by showing Tires PSI warning. 
- Improve safety by showing a warning for Door, trunk, window, charging port open while moving.
- Improve convenience and safety by showing upcoming turn from navigation a few seconds in advance. Sometimes drivers miss the turn because it requires looking at the main screen when navigation voice is turned off.
- Improve safety and convenience by showing caller id for incoming calls and text messages. Allow driver to decide whether to take call or pull over to respond to important message. Currently driver has to shift focus from road to main screen to see caller id and assess priority.
- Improve convenience and safety by adjusting (increase or dim) LED brightness based on ambient light (day vs night). In bright daylight it may require LED to be in max brightness in order to be clearly seen. Respectively at night, if the LED is too bright, its reflection on the windshield may impair road visibility.
- Improve convenience and safety by showing blind spot warnings. Ideally indication that it may not be safe to change lanes. Especially helpful when driver wants to change lanes. Because of cybertruck's relatively wide body, it takes some effort for driver to check side mirrors, on-screen traffic simulator and rear view on main screen before changing lanes.

Other nice to have features:
- Incoming Email preview
- News headlines
- Stock market trades and major updates

# Design constaints

- HUD device needs to be of matte black surface in order to not reflect in windshield
- LEDs reflect well in cybertruck windshield. However LCD and OLED screens (iPhone, iPad) do not reflect well.
- In order to fit neatly behind leather bar on dashboard and not be visible to driver, the HUD projection device needs to be less than 80mm wide and 10mm tall. It can be as long as the whole windshield width.

# Hardware

- [Pi Zero 2 W](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/). This remarkable tiny PCB released in 2021 is still great in 2024 as it strikes an [outstanding performance/power balance](https://hackaday.com/2021/11/01/the-pi-zero-2-w-is-the-most-efficient-pi/). Almost as fast as a regular RPi 3B+ with the power efficiency of a RPi Zero W.
- [LED Matrix 64x32 3mm pitch](https://www.adafruit.com/product/2279). Bright LEDs that reflect well in windshiled and sufficient resolution to display text and distinguishable images. Yet small enough to tuck behind the dashboard without distracting the driver.
- [RGB LED Matrix Bonnet for RPi](https://www.adafruit.com/product/3211) which simplifies control of the RGB Matrix via Rpi.
- [Unininterruptable Power Supply to power the PCB and LED matrix](https://www.makerfocus.com/products/raspberry-pi-expansion-board-ups-pack-standard-power-supply?srsltid=AfmBOop_X6rdueEz7cvVL0TxZKkDICGbjlEOxtUUtbOpe7TOrR_PExrE)
- [Solar panel to continuously charge the UPS battery](https://www.adafruit.com/product/5367)
- [USB A to 2.1mm Male Barrel Jack Cable - 22AWG & 1 meter](https://www.adafruit.com/product/2697). Supplying power from UPS to RGB LED Matrix Bonnet.
- [USB A to Micro USB B cable](https://www.adafruit.com/product/592). Supplying power from UPS to RPi.

# Software

- [DietPi](https://dietpi.com/blog/?p=1058)
- [RPi RGB LED Matrix](https://github.com/hzeller/rpi-rgb-led-matrix)
- [Tesla Fleet API - Vehicle Data](https://developer.tesla.com/docs/fleet-api/endpoints/vehicle-endpoints#vehicle-data)
