# RPI-IMG-ppp
rpi-ppp



// zoznam portov
dmesg | grep "tty"
ls -l /dev|grep serial
ls -l /dev/ttyS0 /dev/ttyAMA0

// config 
sudo nano /boot/config.txt

sudo pppd  /dev/ttyS0 115200 call gprs
sudo pppd  /dev/ttyS0 921600 call gprs

sudo pppd call gprs

tail -f /var/log/syslog
tail -f /var/log/syslog | grep -Ei 'pppd|chat'

sudo killall pppd

sudo systemctl stop serial-getty@ttyAMA0.service
sudo systemctl disable serial-getty@ttyAMA0.servic

sudo systemctl start serial-getty@ttyAMA0.service
sudo systemctl enable serial-getty@ttyAMA0.servic
       
AT+CFUN?
AT+CFUN=0


AT+CFUN=0,0
+-----------------
AT+CMNB=? 
AT+CMNB?
AT+CMNB=1
+--------------------
AT+CNMP=?
AT+CNMP?
//2-Automatic,13-GSM Only,38-LTE Only,51-GSM And LTE Only
AT+CNMP=13     // GSM Only
+-------------------
AT+CPSI=?
AT+CPSI?


AT+CFUN=1
AT+CFUN=0


RDY

+CFUN: 1

+CPIN: READY

SMS Ready

Sending AT query..
AT

OK
Successfull response for AT query..

Enabling echo and verbose mode
ATE1V1

OK
AT+CGMM

SIMCOM_SIM7000E

OK
Model Number : SIMCOM_SIM7000E
AT+CGMI

SIMCOM_Ltd

OK
Manufacturer : SIMCOM_Ltd


