# Invoke-VNC payload

* Author: El3ct71k (Nimrod Levy, Scorpiones)
* Version: Version 1.0
* Target: Windows 7, 8, 8.1, 10

## Description

Invoke-Vnc executes a VNC agent in-memory and initiates a reverse connection, or binds to a specified port. Password authentication is supported.

## Configuration

you must edit the payload file and update the following variables:

* ATTACK_TYPE - on this variable you will choose with which type of payload you want execute
1. bind - bind a VNC port on the victim host
2. reverse - connect to attacker VNC server

###for reverse VNC please update the following variables:
1. ATTACKER_IP - your VNC server
2. VNC_PASS - VNC password for authentication
3. PORT - the port of the vnc server that you listen to

###for bind VNC please update the following variables:
1. VNC_PASS - VNC password for authentication
2. PORT - the port of that was binded on your VNC server

## STATUS

1. Purple - Initial to clean the files from previous execution and starts HTTP server
2. Yellow - Starts HID attack and types a staged payload based on powershell
3. Cyan - Starts Ethernet attack and let the powershell payload to execute the full payload from the server
4. Green - Attack Finished