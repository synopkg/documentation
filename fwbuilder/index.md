---
Title: fwbuilder
Homepage: https://github.com/fwbuilder/fwbuilder/
Repository: https://salsa.debian.org/debian/fwbuilder
Architectures: any all
Version: 5.3.7-5
Metapackages: kali-linux-everything kali-tools-protect 
Icon: images/fwbuilder-logo.svg
PackagesInfo: |
 ### fwbuilder
 
  Firewall Builder consists of an object-oriented GUI and a set of policy
  compilers for various firewall platforms. In Firewall Builder, firewall
  policy is a set of rules, each rule consists of abstract objects which
  represent real network objects and services (hosts, routers, firewalls,
  networks, protocols). Firewall Builder helps the user maintain a database
  of objects and allows policy editing using simple drag-and-drop operations.
   
  This is the GUI part of fwbuilder
 
 **Installed size:** `38.52 MB`  
 **How to install:** `sudo apt install fwbuilder`  
 
 {{< spoiler "Dependencies:" >}}
 * fwbuilder-common 
 * libc6 
 * libgcc-s1 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5printsupport5 
 * libqt5widgets5 
 * libsnmp40 
 * libstdc++6 
 * libxml2 
 * libxslt1.1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### fwb_compile_all
 
 Wrapper script that compiles policies for multiple firewall objects
 
 ```
 root@kali:~# man fwb_compile_all
 fwb_compile_all(1)             Firewall Builder             fwb_compile_all(1)
 
 NAME
        fwb_compile_all  -  Wrapper  script that compiles policies for multiple
        firewall objects
 
 SYNOPSIS
        fwb_compile_all -ffile.xml [-dwdir] [-av] [obj[ obj ...]]
 
 DESCRIPTION
        fwb_compile_all is a wrapper script that compiles policies for  several
        firewall objects in one batch job. This script takes a list of firewall
        object names on the command line (or '-a' command line option, see  be-
        low)  and  calls policy compiler for each one. The script correctly de-
        termines which policy compiler is  needed  depending  on  the  firewall
        platform of each object.
 
 OPTIONS
        -a     The  script  processes  all firewall objects in the "/Firewalls"
               subtree.
 
        -d wdir
               Specify working directory.  Compiler creates file with  iptables
               script  in  this  directory.  If this parameter is missing, then
               iptables script will be placed in the current working directory.
 
        -f FILE
               Specify the name of the data file to be processed.
 
        -v     Script passes this option to the compiler, this makes  it  print
               diagnostic messages indicating its progress.
 
 URL
        Firewall   Builder   home   page  is  located  at  the  following  URL:
        http://www.fwbuilder.org/
 
 BUGS
        Please report bugs using bug tracking system on SourceForge:
 
        http://sourceforge.net/tracker/?group_id=5314&atid=105314
 
 SEE ALSO
        fwbuilder(1), fwb_ipt(1) fwb_ipf(1) fwb_pf(1) fwbedit(1), fwblookup(1)
 
 FWB                                                         fwb_compile_all(1)
 ```
 
 - - -
 
 ##### fwb_iosacl
 
 Policy compiler for Cisco IOS ACL
 
 ```
 root@kali:~# man fwb_iosacl
 fwb_pix(1)                     Firewall Builder                     fwb_pix(1)
 
 NAME
        fwb_ipt - Policy compiler for Cisco IOS ACL
 
 SYNOPSIS
        fwb_iosacl [-vV] [-d wdir] [-4] [-6] [-i] -f data_file.xml object_name
 
 DESCRIPTION
        fwb_iosacl  is  firewall  policy compiler component of Firewall Builder
        (see fwbuilder(1)). Compiler reads objects definitions and firewall de-
        scription  from  the data file specified with "-f" option and generates
        resultant Cisco IOS ACL configuration file. The configuration is  writ-
        ten  to the file with the name the same as the name of the firewall ob-
        ject, plus extension ".fw". Compiler generates  extended  access  lists
        for  Cisco routers running IOS v12.x using "ip access-list <name>" syn-
        tax. Compiler also generates "ip access-group" commands to  assign  ac-
        cess  lists  to interfaces. Generated ACL configuration can be uploaded
        to the router manually or using built-in installer in the  fwbuilder(1)
        GUI.
 
        The data file and the name of the firewall objects must be specified on
        the command line. Other command line parameters are optional.
 
 OPTIONS
        -4     Generate iptables script for IPv4 part of  the  policy.  If  any
               rules  of  the  firewall  refer to IPv6 addresses, compiler will
               skip these rules.  Options "-4" and "-6" are exclusive. If  nei-
               ther  option  is  used, compiler tries to generate both parts of
               the script, although generation of the IPv6 part  is  controlled
               by  the  option  "Enable  IPv6 support" in the "IPv6" tab of the
               firewall object advanced settings dialog.  This option is off by
               default.
 
        -6     Generate  iptables  script  for  IPv6 part of the policy. If any
               rules of the firewall refer to  IPv6  addresses,  compiler  will
               skip these rules.
 
        -f FILE
               Specify the name of the data file to be processed.
 
        -d wdir
               Specify  working  directory. Compiler creates file with ACL con-
               figuration in this directory.  If  this  parameter  is  missing,
               then  generated ACL will be placed in the current working direc-
               tory.
 
        -v     Be verbose: compiler prints diagnostic messages when it works.
 
        -V     Print version number and quit.
 
        -i     When this option is present, the last argument  on  the  command
               line is supposed to be firewall object ID rather than its name
 
 URL
        Firewall   Builder   home   page  is  located  at  the  following  URL:
        http://www.fwbuilder.org/
 
 BUGS
        Please report bugs using bug tracking system on SourceForge:
 
        http://sourceforge.net/tracker/?group_id=5314&atid=105314
 
 SEE ALSO
        fwbuilder(1), fwb_pix(1), fwb_ipfw(1), fwb_ipf(1), fwb_ipt(1) fwb_pf(1)
 
 FWB                                                                 fwb_pix(1)
 ```
 
 - - -
 
 ##### fwb_ipf
 
 Policy compiler for ipfilter
 
 ```
 root@kali:~# fwb_ipf -h
 Firewall Builder:  policy compiler for ipfilter
 Version 5.3.7
 Usage: fwb_ipf [-x] [-v] [-V] [-f filename.xml] [-o output.fw] [-d destdir] [-m] firewall_object_name
 ```
 
 - - -
 
 ##### fwb_ipfw
 
 Policy compiler for ipfw
 
 ```
 root@kali:~# fwb_ipfw -h
 Firewall Builder:  policy compiler for ipfw
 Version 5.3.7
 Usage: fwb_ipfw [-x] [-v] [-V] [-f filename.xml] [-o output.fw] [-d destdir] [-m] firewall_object_name
 ```
 
 - - -
 
 ##### fwb_ipt
 
 Policy compiler for iptables
 
 ```
 root@kali:~# fwb_ipt -h
 Firewall Builder:  policy compiler for Linux 2.4.x and 2.6.x iptables
 Version 5.3.7
 Usage: fwb_ipt [-x level] [-v] [-V] [-q] [-f filename.xml] [-d destdir] [-D datadir ] [-m] [-4|-6] firewall_object_name
 ```
 
 - - -
 
 ##### fwb_pf
 
 Policy compiler for OpenBSD packet filter "pf"
 
 ```
 root@kali:~# fwb_pf -h
 Firewall Builder:  policy compiler for OpenBSD PF
 Version 5.3.7
 Usage: fwb_pf [-x] [-v] [-V] [-f filename.xml] [-o output.fw] [-d destdir] [-D datadir] [-m] [-4|-6] firewall_object_name
 ```
 
 - - -
 
 ##### fwb_pix
 
 Policy compiler for Cisco PIX
 
 ```
 root@kali:~# fwb_pix -h
 Firewall Builder:  policy compiler for Cisco PIX firewall (with support for FWSM)
 Copyright 2002-2009 NetCitadel, LLC
 Version 5.3.7
 Usage: fwb_pix [-tvV] [-f filename.xml] [-d destdir] [-o output.fw] firewall_object_name
 ```
 
 - - -
 
 ##### fwb_procurve_acl
 
 
 ```
 root@kali:~# fwb_procurve_acl -h
 Firewall Builder:  policy compiler for HP ProCurve ACL
 Copyright 2010 NetCitadel, LLC
 Version 5.3.7
 Usage: fwb_procurve_acl [-tvV] [-f filename.xml] [-d destdir] [-o output.fw] firewall_object_name
 ```
 
 - - -
 
 ##### fwbedit
 
 General purpose object tree editing tool
 
 ```
 root@kali:~# fwbedit -h
 Firewall Builder:  general purpose object tree editing tool
 Version 5.3.7
 
 Usage: fwbedit command [options]
 
 Command is one of:
       new         create new object
       delete      delete object
       modify      modify object
       list        print object
       add         add object to a group
       remove      remove object from a group
       upgrade     upgrade data file
       checktree   check object tree and repair if necessary
       merge       merge one data file into another
       import      import firewall configuration (iptables, CIsco IOS,
                   Cisco PIX, ASA and FWSM)
 
 Type   'fwbedit command' to get summary of options for the command
 
 ```
 
 - - -
 
 ##### fwbuilder
 
 Multiplatform firewall configuration tool
 
 ```
 root@kali:~# man fwbuilder
 fwbuilder(1)                   Firewall Builder                   fwbuilder(1)
 
 NAME
        fwbuilder - Multiplatform firewall configuration tool
 
 SYNOPSIS
        /usr/bin/fwbuilder [-ffile.fwb] [-d] [-h] [-ofile] [-Pobject_name] [-r]
        [-v]
 
 DESCRIPTION
        fwbuilder is the Graphic User Interface  (GUI)  component  of  Firewall
        Builder.
 
        Firewall Builder consists of a GUI and set of policy compilers for var-
        ious firewall platforms. It helps users maintain a database of  objects
        and  allows  policy  editing using simple drag-and-drop operations. GUI
        generates firewall description in the form of XML file, which compilers
        then  interpret and generate platform-specific code. Several algorithms
        are provided for automated network objects discovery and bulk import of
        data.  The  GUI  and  policy compilers are completely independent, this
        provides for a consistent abstract model and the same GUI for different
        firewall platforms.
 
        Firewall  Builder  supports  firewalls  based on iptables (Linux kernel
        2.4.x and 2.6.x, see fwb_ipt(1)), ipfilter (variety  of  platforms  in-
        cluding  *BSD,  Solaris  and  others,  see fwb_ipf(1)), pf (OpenBSD and
        FreeBSD, see fwb_pf(1)), ipfw (FreeBSD and others), Cisco PIX (v6.x and
        7.x) and Cisco IOS extended access lists.
 
 OPTIONS
        -f FILE
               Specify the name of the file to be loaded when program starts.
 
        -r     When  this  command  line option is given in combination with -f
               file, the program automatically opens RCS head revision  of  the
               file  if file is in RCS. If file is not in RCS, this option does
               nothing and the file is opened as usual.
 
        -d     Turns on debug mode. Note that in this mode the  program  gener-
               ates  lots  of output on standard error. This is used for debug-
               ging.
 
        -h     Prints brief help message
 
        -o file
               Specify the name of the file for the print  output,  see  option
               "-P".
 
        -P object_name
               Print  rules  and  objects for the firewall object "object_name"
               and immediately exit. The program does not go  into  interactive
               mode.  Print  output  will  be placed in the file specified with
               "-o" option.  If file name is not given with option "-o",  print
               output  is  stored in the file "print.pdf" in the current direc-
               tory.
 
 FILES
        $HOME/.qt/firewallbuilder2rc
               Fwbuilder v2.1 stores user preferences in this file.
 
        $HOME/.config/netcitadel.com/Firewall Builder.conf
               Fwbuilder v3.0 stores user preferences in this file.
 
 URL
        Firewall  Builder  home  page  is  located  at   the   following   URL:
        http://www.fwbuilder.org/
 
 BUGS
        Please report bugs using bug tracking system on SourceForge:
 
        http://sourceforge.net/tracker/?group_id=5314&atid=105314
 
 SEE ALSO
        fwblookup(1), fwb_ipt(1), fwb_ipf(1), fwb_pf(1)
 
 FWB                                                               fwbuilder(1)
 ```
 
 - - -
 
 ### fwbuilder-common
 
  Firewall Builder consists of an object-oriented GUI and a set of policy
  compilers for various firewall platforms. In Firewall Builder, firewall
  policy is a set of rules, each rule consists of abstract objects which
  represent real network objects and services (hosts, routers, firewalls,
  networks, protocols). Firewall Builder helps the user maintain a database
  of objects and allows policy editing using simple drag-and-drop operations.
   
  This is the arch independent common parts of fwbuilder
 
 **Installed size:** `1.25 MB`  
 **How to install:** `sudo apt install fwbuilder-common`  
 
 
 - - -
 
 ### fwbuilder-doc
 
  Firewall Builder consists of an object-oriented GUI and a set of policy
  compilers for various firewall platforms. In Firewall Builder, firewall
  policy is a set of rules, each rule consists of abstract objects which
  represent real network objects and services (hosts, routers, firewalls,
  networks, protocols). Firewall Builder helps the user maintain a database
  of objects and allows policy editing using simple drag-and-drop operations.
   
  This is the documentation of fwbuilder
 
 **Installed size:** `1.39 MB`  
 **How to install:** `sudo apt install fwbuilder-doc`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
