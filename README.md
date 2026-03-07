# Some Flir A20 thermocamera ethernet info

## filesystem

on file A20filesystem.zip there is a full filesystem dump

## Ethernet connection

You must set tcp address with the camera keys and menu.

## Rtp server
The rtp server port is selected on the menu.

It use a proprietary client that start the image transmission owith some Flir socket server comamnd.

I use it with an usb cvbs grabber and obs.

I try to start it and recive video with ffmpeg and vlc without success.


The Flir socket server command that I found with wireshark and packet sender are:

client -> \01.system.rtp.port\00

camera <- \02\2b\48\00 with rtp port 11080

client -> \01.version.product.name\00

camera <- \02\04ThermoVision A20 V\00

client -> \01.version.product.serial\00

camera <- \02\0422700540\00

# Open ports / services

- 21 tcp ftp to images folder
- 23 tcp telnet no password
- 53 udp dns
- 67 udp dhcp
- 80 tcp web server
- 137 udp Netbios name server
- 138 udp Netbios datagram server
- 139 tcp Netbios session service
- 445 tcp SMB
- 1024 tcp unknown
- 22136 Flir socket server

## Telnet usefull comands
on file Flir_E45_Commands.rtf there are all commands

### help show all commands
help command to see command specific help

### palette: Set/read color palette (<palette default> to reset) (opt -e -r)
 palette file names:
- rainHC
- rainbow
- iron
- bw
- bwr

### graphics: graphics [on/off]

### netstat: show network status
netstat -a show all open ports and connectione

### rls: List resources: rls -h for help
rls -lr to see all resources in long format

### store: Store current image
Usage: store [-j] [-p] [-e] [-o] <filename>
(-j=JPEG, -p=PNG compression, -e=JPEG only, -o=Without overlay graphics)

### bt: Send a button command to PEG: bt [-p <press>] [-r <release>] e
buttons are yes no sel frz left right up down
bt e for menu

## Webserver acess

I used a virtualbox windows xp macjìhine with the programs on Utility CD Thermovision A-series.zip file.

The remote rtp proprietary viewer is FLIRRtpPlayer.exe, you must install JRE and JMF from zib file.

