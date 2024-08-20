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
- 


# Design constaints

- HUD device needs to be of matte black surface in order to not reflect in windshield
- LEDs reflect well in cybertruck windshield. However LCD and OLED screens (iPhone, iPad) do not reflect well.
- In order to fit neatly behind leather bar on dashboard and not be visible to driver, the HUD projection device needs to be less than 80mm wide and 10mm tall. It can be as long as the whole windshield width.

