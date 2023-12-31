---
Title: yersinia
Homepage: http://www.yersinia.net/
Repository: 
Architectures: any
Version: 0.8.2-2.1
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### yersinia
 
  Yersinia is a framework for performing layer 2 attacks. It is designed
  to take advantage of some weakeness in different network protocols. It
  pretends to be a solid framework for analyzing and testing the deployed
  networks and systems.
   
  Attacks for the following network protocols are implemented in this
  particular release:
   - Spanning Tree Protocol (STP).
   - Cisco Discovery Protocol (CDP).
   - Dynamic Trunking Protocol (DTP).
   - Dynamic Host Configuration Protocol (DHCP).
   - Hot Standby Router Protocol (HSRP).
   - 802.1q.
   - 802.1x.
   - Inter-Switch Link Protocol (ISL).
   - VLAN Trunking Protocol (VTP).
 
 **Installed size:** `437 KB`  
 **How to install:** `sudo apt install yersinia`  
 
 {{< spoiler "Dependencies:" >}}
 * libatk1.0-0 
 * libc6 
 * libgdk-pixbuf-2.0-0 
 * libglib2.0-0 
 * libgtk2.0-0 
 * libncurses6 
 * libnet1 
 * libpango-1.0-0 
 * libpcap0.8 
 * libtinfo6 
 {{< /spoiler >}}
 
 ##### yersinia
 
 A Framework for layer 2 attacks
 
 ```
 root@kali:~# yersinia --help
     Û²ÛÛ²²Û                                                                    
  
    ²Û°°°²²Û²²                                                                  
  
  Û²²²°ÛÛÛ°²Û²²                                                                 
  
 ²²°²°Û±²±Û²°°²²²Û                                                              
  
 °²°°Û±²±²²±Û²²°²²Û                                                             
  
 ²°²°Û±²±±²²±Û°°²°²²               Yersinia...                                  
  
 ²²°°²Û²²±²²±²±Û°²ÛÛ²²²                                                         
  
 Û²²²°Û±²²²±±²²±ÛÛ°²°ÛÛ²²²         The Black Death for nowadays networks        
  
  ²²²°²ÛÛ±²²²²²²²²±Û°°²²°²²                                                     
  
  ²ÛÛ°°²°Û±²²±±±²²²²²±Û°²²Û²²             by Slay & tomac                       
  
   Û²²Û²°°Û±²²²±±²²²²²²±Û²°°²²Û                                                 
  
      ²²Û²°Û±±²²±±±±±±²²²±Û°²°²Û        http://www.yersinia.net                 
  
       Û²°²²ÛÛ±±±²²±±±±²²²ÛÛÛ²Û²            yersinia@yersinia.net               
  
        Û²²°°²ÛÛ±±±²²²±²²²ÛÛ²°ÛÛ                                                
  
          ²Û²°²²°Û±±±²²²²±Û²°Û²²                                                
  
          ²Û²²Û°²°ÛÛÛÛÛ±ÛÛ°²²²²     Prune your MSTP, RSTP, STP trees!!!!        
  
              ²²Û°°²²²°°²°°Û²²                                                  
  
 
 
 Usage: yersinia [-hVGIDd] [-l logfile] [-c conffile] protocol [protocol_options]
        -V   Program version.
        -h   This help screen.
        -G   Graphical mode (GTK).
        -I   Interactive mode (ncurses).
        -D   Daemon mode.
        -d   Debug.
        -l logfile   Select logfile.
        -c conffile  Select config file.
   protocol   One of the following: cdp, dhcp, dot1q, dot1x, dtp, hsrp, isl, mpls, stp, vtp.
 
 Try 'yersinia protocol -h' to see protocol_options help
 
 Please, see the man page for a full list of options and many examples.
 Send your bugs & suggestions to the Yersinia developers <yersinia@yersinia.net>
 
 
 
 MOTD: Don't do it!! Don't do it!! Don't do it!!
 	(Please DO IT)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
