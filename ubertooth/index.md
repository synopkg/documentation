---
Title: ubertooth
Homepage: https://github.com/greatscottgadgets/ubertooth/
Repository: https://gitlab.com/kalilinux/packages/ubertooth
Architectures: any all
Version: 2020.12.R1-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-802-11 kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libubertooth-dev
 
  Project Ubertooth is an open source wireless development platform suitable for
  Bluetooth experimentation. Ubertooth ships with a capable BLE (Bluetooth Smart)
  sniffer and can sniff some data from Basic Rate (BR) Bluetooth Classic
  connections.
   
  This package provides the development files for using the ubertooth library.
 
 **Installed size:** `52 KB`  
 **How to install:** `sudo apt install libubertooth-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libbluetooth-dev
 * libbtbb-dev
 * libpcap-dev
 * libubertooth1 
 * libusb-1.0-0-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### libubertooth1
 
  Project Ubertooth is an open source wireless development platform suitable for
  Bluetooth experimentation. Ubertooth ships with a capable BLE (Bluetooth Smart)
  sniffer and can sniff some data from Basic Rate (BR) Bluetooth Classic
  connections.
   
  This package provides the shared library needed by Ubertooth.
 
 **Installed size:** `87 KB`  
 **How to install:** `sudo apt install libubertooth1`  
 
 {{< spoiler "Dependencies:" >}}
 * libbtbb1 
 * libc6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### ubertooth
 
  Project Ubertooth is an open source wireless development platform suitable for
  Bluetooth experimentation. This package contains everything necessary to use
  the hardware dongle.
   
  Ubertooth is capable of sniffing BLE (Bluetooth Smart) connections and it also
  has some ability to sniff some data from Basic Rate (BR) Bluetooth Classic
  connections.
   
  In addition to the Bluetooth specific capabilities, there is also a simple
  spectrum analyzer for the 2.4 GHz band included (ubertooth-specan-ui) which
  can be used to also observe other things in this frequency band.
 
 **Installed size:** `336 KB`  
 **How to install:** `sudo apt install ubertooth`  
 
 {{< spoiler "Dependencies:" >}}
 * libbluetooth3 
 * libbtbb1 
 * libc6 
 * libubertooth1 
 * libusb-1.0-0 
 * python3
 * python3-numpy
 {{< /spoiler >}}
 
 ##### ubertooth-afh
 
 Passive detection of AFH channel map
 
 ```
 root@kali:~# ubertooth-afh -h
 ubertooth-afh - passive detection of the AFH channel map
 
 Determine the AFH map for piconet ??:??:22:44:66:88:
     ubertooth-afh -u 22 -l 446688
 
 Main options:
 	-l <LAP> LAP of target piconet (3 bytes / 6 hex digits)
 	-u <UAP> UAP of target piconet (1 byte / 2 hex digits)
 	-m <int> threshold for channel removal (default: 5)
 	-r print AFH channel map once every second (default: print on update)
 
 Other options
 	-t <seconds> timeout for initial AFH map detection (not required)
 	-e maximum access code errors (default: 2, range: 0-4)
 	-V print version information
 	-U <0-7> set ubertooth device to use
 ```
 
 - - -
 
 ##### ubertooth-btbr
 
 
 
 - - -
 
 ##### ubertooth-btle
 
 Bluetooth Low Energy (BLE) sniffing and more
 
 ```
 root@kali:~# ubertooth-btle -h
 ubertooth-btle - passive Bluetooth Low Energy monitoring
 Usage:
 	-h this help
 
     Major modes:
 	-f follow connections
 	-n don't follow, only print advertisements
 	-p promiscuous: sniff active connections
 
 	-a[address] get/set access address (example: -a8e89bed6)
 	-s<address> faux slave mode, using MAC addr (example: -s22:44:66:88:aa:cc)
 	-t<address> set connection following target (example: -t22:44:66:88:aa:cc/48)
 	-tnone unset connection following target
 
     Interference (use with -f or -p):
 	-i interfere with one connection and return to idle
 	-I interfere continuously
 
     Data source:
 	-U<0-7> set ubertooth device to use
 
     Misc:
 	-r<filename> capture packets to PCAPNG file
 	-q<filename> capture packets to PCAP file (DLT_BLUETOOTH_LE_LL_WITH_PHDR)
 	-c<filename> capture packets to PCAP file (DLT_PPI + DLT_BLUETOOTH_LE_LL)
 	-A<index> advertising channel index (default 37)
 	-v[01] verify CRC mode, get status or enable/disable
 	-x<n> allow n access address offenses (default 32)
 
 If an input file is not specified, an Ubertooth device is used for live capture.
 In get/set mode no capture occurs.
 ```
 
 - - -
 
 ##### ubertooth-debug
 
 Classic Bluetooth discovery, sniffing, and decoding
 
 ```
 root@kali:~# ubertooth-debug -h
 ubertooth-debug - command line utility for debugging Ubertooth One
 Usage:
 	-h this message
 	-r <reg>[,<reg>[,...]] read the contents of CC2400 register(s)
 	-r <start>-<end> read a consecutive set of CC2400 register(s)
 	-U<0-7> set ubertooth device to use
 	-v<0-2> verbosity (default=1)
 ```
 
 - - -
 
 ##### ubertooth-dfu
 
 Device firmware update for Ubertooth
 
 ```
 root@kali:~# ubertooth-dfu -h
 ubertooth-dfu - Ubertooth firmware update tool
 
 To update firmware, run:
 	ubertooth-dfu -d bluetooth_rxtx.dfu -r
 
 Usage:
 	-u <filename> upload - read firmware from device
 	-d <filename> download - write DFU file to device
 	-r reset Ubertooth after other operations complete
 
 Miscellaneous:
 	-s <filename> add DFU suffix to binary firmware file
 	-U <0-7> set ubertooth device to use
 ```
 
 - - -
 
 ##### ubertooth-ducky
 
 
 ```
 root@kali:~# ubertooth-ducky -h
 ubertooth-ducky - make an Uberducky quack like a USB Rubber Ducky
 Usage:
 	-q [uuid] quack!
 	-b signal Uberducky to enter bootloader
 
 	-A <index> advertising channel index (default: 38)
 	-a <BD ADDR> Bluetooth address (default: random)
 	-h this help
 
 For more information on Uberducky, visit:
 https://github.com/mikeryan/uberducky
 ```
 
 - - -
 
 ##### ubertooth-dump
 
 Output a continuous stream of received bits
 
 ```
 root@kali:~# ubertooth-dump -h
 ubertooth-dump - output a continuous stream of received bits
 Usage:
 	-h this help
 	-b only dump received bitstream (GnuRadio style)
 	-c classic modulation
 	-l LE modulation
 	-U<0-7> set ubertooth device to use
 	-d filename
 
 This program sends binary data to stdout.  You probably don't want to
 run it from a terminal without redirecting the output.
 ```
 
 - - -
 
 ##### ubertooth-ego
 
 Yuneec E-GO skateboard sniffing
 
 ```
 root@kali:~# ubertooth-ego -h
 ubertooth-ego - Yuneec E-GO skateboard sniffing
 Usage:
 	-h this help
 
     Major modes:
 	-f follow connections
 	-r continuous rx on a single channel
 	-i interfere
 
     Options:
 	-c <2402-2480> set channel in MHz (for continuous rx)
 	-l <1-48> capture length (default: 18)
 	-a <access_code> access code (default: 630f9ffe)
 ```
 
 - - -
 
 ##### ubertooth-follow
 
 CLK discovery and follow for a particular UAP/LAP
 
 ```
 root@kali:~# ubertooth-follow -h
 ubertooth-follow - active(bluez) CLK discovery and follow for a particular UAP/LAP
 Usage:
 	-h this help
 	-l<LAP> (in hexadecimal)
 	-u<UAP> (in hexadecimal)
 	-U<0-7> set ubertooth device to use
 	-r<filename> capture packets to PCAPNG file
 	-q<filename> capture packets to PCAP file
 	-e max_ac_errors
 	-d filename
 	-a Enable AFH
 	-b Bluetooth device (hci0)
 	-w USB delay in 625us timeslots (default:5)
 
 LAP and UAP are both required, if not given they are read from the local device, in some cases this may give the incorrect address.
 ```
 
 - - -
 
 ##### ubertooth-rx
 
 Classic Bluetooth discovery, sniffing, and decoding
 
 ```
 root@kali:~# ubertooth-rx -h
 ubertooth-rx - passive Classic Bluetooth discovery/decode
 
 Example usage:
 	ubertooth-rx -- sniff for all LAPs
 	ubertooth-rx -l <lap> -- calculate UAP for a given LAP
 	ubertooth-rx -l <lap> -u <uap> -- calculate clock and follow piconet
 	ubertooth-rx -z -t 20 -- survey mode: discover all LAPs+UAPs for 20 seconds
 
 Major modes:
 	-l <LAP> to decode (6 hex) - if not specified sniff all LAPs
 	-u <UAP> to decode (2 hex) - if not specified calculate UAP (requires LAP)
 	-z Survey mode - discover and list piconets (implies -s, interrupt with ctrl-C)
 	-i <filename> input file - if not specified use Ubertooth for live capture
 
 Configuration:
 	-c <BT Channel> set a fixed bluetooth channel [Default: 39]
 	-e max_ac_errors (default: 2, range: 0-4)
 	-t <SECONDS> sniff timeout - 0 means no timeout [Default: 0]
 
 Output options:
 	-r<filename> capture packets to PcapNG file
 	-q<filename> capture packets to PCAP file
 	-d<filename> dump packets to binary file
 
 Miscellaneous:
 	-V print version information
 	-U <0-7> set ubertooth device to use
 ```
 
 - - -
 
 ##### ubertooth-scan
 
 Scan frequency band active (Bluez) device scan and inquiry supported by Ubertooth
 
 ```
 root@kali:~# ubertooth-scan -h
 ubertooth-scan - active(Bluez) device scan and inquiry supported by Ubertooth
 
 This tool uses a normal Bluetooth dongle to perform Inquiry Scans and
 Extended Inquiry scans of Bluetooth devices. It uses Ubertooth to
 discover undiscoverable devices and can use BlueZ to scan for
 discoverable devices.
 
 Usage:
     ubertooth-scan
         Use Ubertooth to discover devices and perform Inquiry Scan.
 
     ubertooth-scan -s -x
         Use BlueZ and Ubertooth to discover devices and perform Inquiry Scan
         and Extended Inquiry Scan.
 
 Options:
 	-s hci Scan - use BlueZ to scan for discoverable devices
 	-x eXtended scan - retrieve additional information about target devices
 	-t scan Time (seconds) - length of time to sniff packets. [Default: 20s]
 	-e max_ac_errors (default: 2, range: 0-4)
 	-b Bluetooth device (hci0)
 	-U<0-7> set Ubertooth device to use
 ```
 
 - - -
 
 ##### ubertooth-specan
 
 A spectrum analyzer for Ubertooth
 
 ```
 root@kali:~# ubertooth-specan -h
 ubertooth-specan - output a continuous stream of signal strengths
 
 !!!!!
 NOTE: you probably want ubertooth-specan-ui
 !!!!!
 
 Usage:
 	-h this help
 	-v verbose (print debug information to stderr)
 	-g output suitable for feedgnuplot
 	-G output suitable for 3D feedgnuplot
 	-d <filename> output to file
 	-l lower frequency (default 2402)
 	-u upper frequency (default 2480)
 	-U<0-7> set ubertooth device to use
 ```
 
 - - -
 
 ##### ubertooth-specan-ui
 
 Spectrum analyzer for the 2.4 GHz ISM band
 
 ```
 root@kali:~# man ubertooth-specan-ui
 UBERTOOTH-SPECAN-UI(1)                                  UBERTOOTH-SPECAN-UI(1)
 
 NAME
        ubertooth-specan-ui - spectrum analyzer for the 2.4 GHz ISM band
 
 SYNOPSIS
        ubertooth-specan-ui
 
 DESCRIPTION
        This  shows a GUI window with a spectrum analyzer for the 2.4 GHz band.
        It is very useful to see at what frequencies there are signals.
 
 OPTIONS
        There are no command line options.
 
 SEE ALSO
        ubertooth-specan(1)
 
 AUTHOR
        This manual page was written by Ruben Undheim <ruben.undheim@gmail.com>
        for the Debian project (and may be used by others).
 
                                12 December 2022         UBERTOOTH-SPECAN-UI(1)
 ```
 
 - - -
 
 ##### ubertooth-util
 
 General purpose Ubertooth utility
 
 ```
 root@kali:~# ubertooth-util -h
 ubertooth-util - command line utility for Ubertooth Zero and Ubertooth One
 
 Common options:
 	-v get firmware revision number
 	-V get compile info
 	-I identify ubertooth device by flashing all LEDs
 	-d[0-1] get/set all LEDs
 	-l[0-1] get/set USR LED
 	-S stop current operation
 	-r full reset
 	-U<0-7> set ubertooth device to use
 	-N print total number of Uberteeth and exit
 
 Radio options:
 	-a[0-7] get/set power amplifier level
 	-c[2400-2483] get/set channel in MHz
 	-C[0-78] get/set channel
 	-q[1-225 (RSSI threshold)] start LED spectrum analyzer
 	-t intitiate continuous transmit test
 	-z set squelch level
 
 Range test:
 	-e start repeater mode
 	-m display range test result
 	-n initiate range test
 
 Miscellaneous:
 	-f activate flash programming (DFU) mode
 	-i activate In-System Programming (ISP) mode
 	-b get hardware board id number
 	-p get microcontroller Part ID
 	-s get microcontroller serial number
 	-x xmas lights
 ```
 
 - - -
 
 ### ubertooth-firmware
 
  The Ubertooth hardware needs some firmware to run. The firmware is built with
  arm-none-eabi-gcc. This package contains a number of firmware images that
  may be programmed into the Ubertooth hardware using the 'ubertooth-dfu'
  command.
   
  The firmware images are installed in /usr/share/ubertooth/firmware/
 
 **Installed size:** `89 KB`  
 **How to install:** `sudo apt install ubertooth-firmware`  
 
 
 - - -
 
 ### ubertooth-firmware-source
 
  The Ubertooth hardware needs some firmware to run. The firmware is built with
  arm-none-eabi-gcc. This package contains the source code for the firmware that
  is found in the ubertooth-firmware package.
   
  The firmware source may be found in /usr/src/ubertooth-firmware-source.tar.gz
  after installing this package.
 
 **Installed size:** `251 KB`  
 **How to install:** `sudo apt install ubertooth-firmware-source`  
 
 {{< spoiler "Dependencies:" >}}
 * libubertooth-dev
 * ubertooth
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
