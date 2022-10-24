Based on https://www.instructables.com/DIY-1kW-MPPT-Solar-Charge-Controller/
Since I wanted to be able to change the board layout and to test KiCad I decided to give this "conversion" a try.

- I removed the keyboard pullups, they are not needed when activating the internal pullup. And I prefer switching to ground anyway, so I can use 5V for the display and the keyboard.
- I changed the footprint of the screw terminals, since I did not find any other (trustworthy) 50A capable terminal.
- Added possibility of doubling Q1 to Q3. ToDo: Need to check if the spacing is enough.
- Added JTAG interface
- Added a SD card and IIC socket, mainly for a RTC module. Should allow for much better offline logging.
- Switched to 1.27mm pitch smd connector. No need for 2.54mm. Just uses up too much space - on both sides of the board. Also added a few spare IOs and IIC.
- Fan driver transistor. ToDo: Maybe better switch +, and not GND. Although switching ground allows for more flexibility regarding fan voltage.
- Had to divide GND into GND and GND2, so I could add the GND copper bar to the schematics and the layout without getting too hacky... Found no better "KiCad way"
- 3D models are almost complete. SD card is not perfect.

![image](https://user-images.githubusercontent.com/9505718/197556688-87b132a9-91cb-472a-b1fc-604e41f7f647.png)
![image](https://user-images.githubusercontent.com/9505718/197556951-bcc581de-8078-4723-b2d1-d8d0403cc7ca.png)
