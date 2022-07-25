---
Title: xplico
Homepage: http://www.xplico.org
Repository: https://gitlab.com/kalilinux/packages/xplico
Architectures: amd64 i386
Version: 1.2.2-0kali4
Metapackages: kali-linux-everything kali-tools-forensics 
Icon: images/xplico-logo.svg
PackagesInfo: |
 ### xplico
 
  The goal of Xplico is extract from an internet traffic
  capture the applications data contained. For example,
  from a pcap file Xplico extracts each email (POP, IMAP,
  and SMTP protocols), all HTTP contents, each VoIP call (SIP, MGCP, H323),
  FTP, TFTP, and so on. Xplico is not a network protocol analyzer.
 
 **Installed size:** `10.02 MB`  
 **How to install:** `sudo apt install xplico`  
 
 {{< spoiler "Dependencies:" >}}
 * apache2
 * binfmt-support
 * init-system-helpers 
 * lame
 * libapache2-mod-php
 * libc6 
 * libjson-c5 
 * libmariadb3 
 * libmaxminddb0 
 * libndpi4.2 
 * libpcap0.8 
 * libpq5
 * libsqlite3-0 
 * libssl3 
 * openssl
 * php-cli
 * php-common
 * php-json
 * php-sqlite3
 * python3
 * python3-httplib2
 * python3-psycopg2
 * recode
 * sox
 * sqlite3
 * tshark
 * zlib1g 
 {{< /spoiler >}}
 
 ##### mfbc
 
 
 ```
 root@kali:~# mfbc -h
 mfbc v1.2.2
 Internet Traffic Decoder (NFAT).
 See http://www.xplico.org for more information.
 
 Copyright 2007-2019 Gianluca Costa & Andrea de Franceschi and contributors.
 This is free software; see the source for copying conditions. There is NO
 warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 This product includes GeoLite data created by MaxMind, available from http://www.maxmind.com/.
 
 usage: mfbc [-h] [-s] [-l] [-i] [-c <config_file>] -p <port>
 	-c config file
 	-s silent
 	-p connection port
 	-i info (PEI generated by this manipulator)
 	-l print all log in the screen
 	-h this help
 	NOTE: parameters MUST respect this order!
 
 ```
 
 - - -
 
 ##### mfile
 
 
 ```
 root@kali:~# mfile -h
 mfile v1.2.2
 Internet Traffic Decoder (NFAT).
 See http://www.xplico.org for more information.
 
 Copyright 2007-2019 Gianluca Costa & Andrea de Franceschi and contributors.
 This is free software; see the source for copying conditions. There is NO
 warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 This product includes GeoLite data created by MaxMind, available from http://www.maxmind.com/.
 
 usage: mfile [-h] [-s] [-l] [-i] [-c <config_file>] -p <port>
 	-c config file
 	-s silent
 	-p connection port
 	-i info (PEI generated by this manipulator)
 	-l print all log in the screen
 	-h this help
 	NOTE: parameters MUST respect this order!
 
 ```
 
 - - -
 
 ##### mpaltalk
 
 
 ```
 root@kali:~# mpaltalk -h
 mpaltalk v1.2.2
 Internet Traffic Decoder (NFAT).
 See http://www.xplico.org for more information.
 
 Copyright 2007-2019 Gianluca Costa & Andrea de Franceschi and contributors.
 This is free software; see the source for copying conditions. There is NO
 warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 This product includes GeoLite data created by MaxMind, available from http://www.maxmind.com/.
 
 usage: mpaltalk [-h] [-s] [-l] [-i] [-c <config_file>] -p <port>
 	-c config file
 	-s silent
 	-p connection port
 	-i info (PEI generated by this manipulator)
 	-l print all log in the screen
 	-h this help
 	NOTE: parameters MUST respect this order!
 
 ```
 
 - - -
 
 ##### mwmail
 
 
 ```
 root@kali:~# mwmail -h
 mwmail v1.2.2
 Internet Traffic Decoder (NFAT).
 See http://www.xplico.org for more information.
 
 Copyright 2007-2019 Gianluca Costa & Andrea de Franceschi and contributors.
 This is free software; see the source for copying conditions. There is NO
 warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 This product includes GeoLite data created by MaxMind, available from http://www.maxmind.com/.
 
 usage: mwmail [-h] [-s] [-l] [-i] [-c <config_file>] -p <port>
 	-c config file
 	-s silent
 	-p connection port
 	-i info (PEI generated by this manipulator)
 	-l print all log in the screen
 	-h this help
 	NOTE: parameters MUST respect this order!
 
 ```
 
 - - -
 
 ##### trigcap
 
 
 ```
 root@kali:~# trigcap -h
 
 usage: trigcap [-v] -f <input_file> -t <pkt num> -b <pkt numbers before> -a <pkt numbers after> -o <output_file> [-h]
 	-v version
 	-f input pcap file
 	-t trigger packet number
 	-b packet numbers before trigger packet
 	-a packet numbers after trigger packet
 	-o output pcap file
 	-h this help
 
 ```
 
 - - -
 
 ##### xplico
 
 
 ```
 root@kali:~# xplico -h
 xplico v1.2.2
 Internet Traffic Decoder (NFAT).
 See http://www.xplico.org for more information.
 
 Copyright 2007-2019 Gianluca Costa & Andrea de Franceschi and contributors.
 This is free software; see the source for copying conditions. There is NO
 warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
 
 This product includes GeoLite data created by MaxMind, available from http://www.maxmind.com/.
 
 usage: xplico [-v] [-c <config_file>] [-h] [-s] [-g] [-l] [-i <prot>] -m <capute_module>
 	-v version
 	-c config file
 	-h this help
 	-i info of protocol 'prot' 
 	-g display graph-tree of protocols
 	-l print all log in the screen
 	-s print every second the deconding status
 	-m capture type module
 	NOTE: parameters MUST respect this order!
 
 ```
 
 - - -
 
 ##### xplico-webui
 
 
 ```
 root@kali:~# xplico-webui -h
 [*] Please wait for the Xplico service to start.
 [*]
 [*] You might need to refresh your browser once it opens.
 [*]
 [*]  Web UI: http://127.0.0.1:9876
 
 ```
 
 - - -
 
 ##### xplico-webui-stop
 
 
 ```
 root@kali:~# xplico-webui-stop -h
 * apache2.service - The Apache HTTP Server
      Loaded: loaded (/lib/systemd/system/apache2.service; disabled; vendor preset: disabled)
      Active: inactive (dead)
        Docs: https://httpd.apache.org/docs/2.4/
 
 Jul 22 12:18:26 kali systemd[1]: Starting The Apache HTTP Server...
 Jul 22 12:18:26 kali apachectl[2041919]: AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.1.1. Set the 'ServerName' directive globally to suppress this message
 Jul 22 12:18:26 kali systemd[1]: Started The Apache HTTP Server.
 Jul 22 12:18:36 kali systemd[1]: Stopping The Apache HTTP Server...
 Jul 22 12:18:36 kali apachectl[2057632]: AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.1.1. Set the 'ServerName' directive globally to suppress this message
 Jul 22 12:18:36 kali systemd[1]: apache2.service: Deactivated successfully.
 Jul 22 12:18:36 kali systemd[1]: Stopped The Apache HTTP Server.
 
 * xplico.service - Xplico
      Loaded: loaded (/lib/systemd/system/xplico.service; disabled; vendor preset: disabled)
      Active: inactive (dead)
        Docs: https://www.xplico.org/docs
 
 Jul 22 12:18:26 kali systemd[1]: Starting Xplico...
 Jul 22 12:18:26 kali systemd[1]: xplico.service: Can't open PID file /run/dema.pid (yet?) after start: Operation not permitted
 Jul 22 12:18:26 kali systemd[1]: Started Xplico.
 Jul 22 12:18:36 kali systemd[1]: Stopping Xplico...
 Jul 22 12:18:36 kali systemd[1]: xplico.service: Deactivated successfully.
 Jul 22 12:18:36 kali systemd[1]: Stopped Xplico.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## xplico Usage Examples

Use the rltm module (`-m rltm`) and analyze traffic on interface eth0 (`-i eth0`):

```
root@kali:~# xplico -m rltm -i eth0
xplico v1.0.1
Internet Traffic Decoder (NFAT).
See http://www.xplico.org for more information.

Copyright 2007-2012 Gianluca Costa & Andrea de Franceschi and contributors.
This is free software; see the source for copying conditions. There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

This product includes GeoLite data created by MaxMind, available from http://www.maxmind.com/.
Configuration file (/opt/xplico/cfg/xplico_cli.cfg) found!
GeoLiteCity.dat found!
pcapf: running: 0/0, subflow:0/0, tot pkt:1
pol: running: 0/0, subflow:0/0, tot pkt:0
eth: running: 0/0, subflow:0/0, tot pkt:1
pppoe: running: 0/0, subflow:0/0, tot pkt:0
ppp: running: 0/0, subflow:0/0, tot pkt:0
ip: running: 0/0, subflow:0/0, tot pkt:0
```