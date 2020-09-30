# WAVGAT-BOARD
Adding WAVGAT boards to the Arduino IDE via board manager:
 - WAVGAT UNO R3
 - WAVGAT NANO 3.0
 - WAVGAT Pro Mini

I downloaded the official WAVGAT drivers from https://drive.google.com/open?id=10gwrG9uTDwaEO-7EudsmBkfgdcyrcABI and restructured them to use it with the board manager, but I had a problem with the Ethernet library. Then I found this repository https://github.com/LGTMCU/Larduino_HSP, I did the same and It works!

I checked this repository:
 - On debian buster (10.6 / 32 and 64 bits).
 - On Arduino IDE V1.8.13 (version lower than V1.6.18 it should give an error).
 - Compilation and upload empty, blinking, servo and some ethernet sketch examples are OK.

# REQUIREMENTS
You must have installed at least Arduino IDE V1.6.18. You can download it from https://www.arduino.cc/en/Main/Software
If you are on Windows, you must download and install the CH340/CH341 driver to communicate with the board via USB from http://www.wch.cn/download/CH341SER_EXE.html

# INSTALLATION
 - Start Arduino IDE and open "Preferences" window from "File" menu.
 - Go to "Additional Board Manager URLs" field add this url https://raw.githubusercontent.com/paraplin/wavgat-board/master/package_paraplin_wavgat_index.json and press OK.
 - Go to "Tools" menu and select "Open Boards Manager". In the new window install wavgat platform.
 - Go to "Tools" menu and go to "board" submenu. Select your correct board in "WAVGAT boards" section.

# ISSUES
 - Compilation errors can be lead because it use some different libraries than Arduino, for example, with MFRC522 access control sketch: 'class EEPROMClass' has no member named 'length' and this happens because the EEPROM library from Arduino is different than the WAVGAT board uses.
 - My english is very poor ;).
