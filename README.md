# Some Flir A20 thermocamera info

## filesystem

on file A20filesystem.zip there is a full filesystem dump

## Ethernet connection

You must set tcp address with the camera keys and menu.

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
