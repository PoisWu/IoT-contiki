riotp35
tsyY5#tisdx

iotlab-auth -u riotp35

# LEDS
    leds_on(LEDS_RED) / 
    leds_off(LEDS_RED)
    leds_toggle(LEDS_GREEN)
    leds_on(LEDS_ALL)
    leds_get() // %X format 

# IPv6 lab(12-oct)
m3-100 bourder router `2001:660:4403:4cc::9989` 
m3-101 http server ipv6 address 

lille prefix 2001:660:4403:0480

# Final Project
Date line 18 novembre 2022
Défi votre imagination de concevoir une application IoT. 

créez votre banc d'essai simple de l'IoT, servers et clients HTTP/CoAP
Informations de détection et automatisation 


Imaginez une application IoT simple et définissez ses exigences

3 fonctions d'automatisation de cette application. 


# TP2 Note

http-server.{c/iotlab-m3} HTTP server with sending only pressure data
Border-router.iotlab-m3 

er-example-server.{c/iotlab-m3} CoAP server file
sensors-collecting.c for reference to access other sensing information 


Site grenoble
sudo tunslip6.py -v2 -L -a m3-<??> -p 20000 2001:660:5307:3122::1/64


Border-router
iotlab-node --flash border-router.iotlab-m3 -l grenoble,m3,X



HTTP server 
iotlab-node --flash http-server.iotlab-m3 -l grenoble,m3,Y

CoAP server 
iotlab-node --flash er-example-server.iotlab-m3 -l grenoble,m3,Y


For border and HTTP server 
lynx -dump http://[2001:660:5307:3122:: .... ] 


For CoAP server
aiocoap-client coap://[2001:660:5307:3122:: <>]:5683/sensors/pressure



Capteur light   -               Alarme 


Utilisateur sur le front-end: 
Capteur et LED, l'ordinateur 
