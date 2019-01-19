# RFID-Card-Hostel-Entry
First read the documentation before reading this readme.\
You'll need to install Node.js, NodeRED and Mosquitto mqtt broker to make this project work. Get them installed according to your system requirements.\
This project is compatible with Mifare 1k and 4k cards. I've personally only tested Mifare 1k cards.\
You should keep Mosquitto and NodeRED running in your terminals.\
Then open NodeRED in your browser at 127.0.0.1:1880 and import the NodeRED flow.\
If you're running linux and mosquitto fails to start run sudo pkill mosquitto.\
Connect NodeMCU board to the MFRC522 module in the following way:\
NodeMCU     MFRC522\
D1   ---->   RST\
3V3  ---->   3.3V\
D8   ---->   SDA\
D5   ---->   SCK\
D6   ---->   MISO\
D7   ---->   MOSI\
GND  ---->   GND\
# Writing student data to cards
Upload write_student_info sketch to the NodeMCU board and open serial monitor. Then enter the info ending with '#' and press enter.\
# Reading student data from cards
Upload mysketch sketch to the board and set up the rest of the project as mentioned above.
# Error Handling
Press the reset button of the NodeMCU in case anything goes wrong.
