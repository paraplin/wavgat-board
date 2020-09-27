# WAVGAT-BOARD
Adding wavgat boards to the Arduino IDE via board manager.

I downloaded the official WAVGAT drivers from https://drive.google.com/open?id=10gwrG9uTDwaEO-7EudsmBkfgdcyrcABI and restructured them for use with the board manager.

This is a test repository:
 - Checked in Arduino IDE on debian 10.6 (buster) 32 and 64 bits.
 - Compilation and upload blinking and empty sketch -> OK.
 - Testing on Arduino IDE V1.8.13 in minor versions it could give an error.

# PREREQUISITES
You must have version 1.8 of the Arduino IDE installed. You can download it from https://www.arduino.cc/en/Main/Software
If you are on Windows, you must download and install the CH340/CH341 driver to communicate with the board via USB from http://www.wch.cn/download/CH341SER_EXE.html

# INSTALLATION
 - Start Arduino IDE and open "Preferences" window from "File" menu.
 - Go to "Additional Board Manager URLs" field add this url https://github.com/paraplin/wavgat-board/raw/master/package_paraplin_wavgat_index.json and press OK.
 - Go to "Tools" menu select "Open Boards Manager". In the new window install wavgat platform.
 - Go to "Tools" menu and select your correct board in the "Board" section.
