Based on https://www.instructables.com/DIY-1kW-MPPT-Solar-Charge-Controller/
Since I wanted to be able to change the board layout and to test KiCad I decided to give this "conversion" a try.

- I removed the keyboard pullups, they are not needed when activating the internal pullup. And I prefer switching to ground anyway, so I can use 5V for the display and the keyboard.
- I changed the footprint of the screw terminals, since I did not find any other (trustworthy) 50A capable terminal. https://www.degson.com/content/details_552_880568.html
- Added JTAG interface
- Added a SD card and IIC socket, mainly for a RTC module. Should allow for much better offline logging.
- Switched to 1.27mm pitch smd connector. No need for 2.54mm. Just uses up too much space - on both sides of the board. Also added a few spare IOs and IIC.
- Fan driver transistor. ToDo: Maybe better switch +, and not GND. Although switching ground allows for more flexibility regarding fan voltage.
- Had to divide GND into GND and GND2, so I could add the GND copper bar to the schematics and the layout without getting too hacky... Found no better "KiCad way"
- 3D models are almost complete. SD card is not perfect.
- Switched to USB-C

3D VRML preview: https://marcelmo.github.io/MPPT_Kicad_Schematics/ (Thanks to https://easyw.github.io/vrm360/ )
![MPPT_Charger_top_view](https://github.com/user-attachments/assets/e09eda48-d56c-4336-b77e-5f80a9d9513d)
![MPPT_Charger_bottom_view](https://github.com/user-attachments/assets/4a02248a-1ff3-46b5-9c1f-4f8be075e6c8)

