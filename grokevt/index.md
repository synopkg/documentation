---
Title: grokevt
Homepage: http://projects.sentinelchicken.org/grokevt/
Repository: https://salsa.debian.org/pkg-security-team/grokevt
Architectures: all
Version: 0.5.0-5
Metapackages: kali-linux-everything kali-tools-detect kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### grokevt
 
  GrokEVT is a collection of scripts built for reading Microsoft Windows
  NT/2000/XP/2003 event log files.
   
  Currently the scripts work together on one or more mounted Microsoft Windows
  partitions to extract all information needed (registry entries, message
  templates, and log files) to convert the logs to a human-readable format.
   
  This program is useful in forensics investigations.
 
 **Installed size:** `121 KB`  
 **How to install:** `sudo apt install grokevt`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-pyregfi
 * reglookup
 {{< /spoiler >}}
 
 ##### grokevt-addlog
 
 A tool for adding a raw event log to an existing GrokEVT database.
 
 ```
 root@kali:~# grokevt-addlog -h
 USAGE:
   /usr/bin/grokevt-addlog <DATABASE_DIR> <EVT_FILE> <NEW_TYPE> <BASE_TYPE>
 
 This script takes a raw Windows event log and adds it to a
 previously built database generated by grokevt-builddb.
 See the man page for more details.
 ```
 
 - - -
 
 ##### grokevt-builddb
 
 Builds a database tree based on a single windows system for the purpose of event log conversion.
 
 ```
 root@kali:~# grokevt-builddb -h
 USAGE:
   grokevt-builddb [-v] [-c CSID] <CONFIG_PROFILE> <OUTPUT_DIR>
 
 grokevt-builddb builds a database tree based on a
 single windows system for the purpose of event log
 conversion.  Please see the man page for more
 information.
 ERROR: Requires at least 2 arguments.
 ```
 
 - - -
 
 ##### grokevt-dumpmsgs
 
 A tool for dumping the contents of message databases built previously by grokevt-ripdll(1).
 
 ```
 root@kali:~# man grokevt-dumpmsgs
 grokevt-dumpmsgs(1)                                        grokevt-dumpmsgs(1)
 
 NAME
        grokevt-dumpmsgs - A tool for dumping the contents of message databases
        built previously by grokevt-ripdll(1).
 
 SYNOPSIS
        grokevt-dumpmsgs message-db1 [message-db2 ...]
 
 DESCRIPTION
        grokevt-dumpmsgs takes one or more message databases  previously  built
        with  grokevt-ripdll(1)  and  prints out all entries to stdout. This is
        mainly a debugging tool, but may be useful for  analyzing  the  message
        contents of PE files while developing other applications.
 
 ARGUMENTS
        grokevt-dumpmsgs uses the following arguments:
 
        message-dbN
               If multiple message databases are supplied, entries of all data-
               bases are printed to stdout in the order they are provided.
 
 OUTOUT
        grokevt-dumpmsgs prints each database entry out on a  single  line,  in
        two  comma-separated columns. The first column is the message ID, which
        is in the format:
 
                  XXXX-YYYYYYYY
 
        Here, XXXX represents the message's language  code,  and  the  YYYYYYYY
        represents the message's relative virtual address (RVA) within the mes-
        sage block of the PE file.  The second column contains the message  it-
        self.  Messages containing special characters (such as newlines or com-
        mas) are encoded in the same manner  that  grokevt-parselog(1)  encodes
        them ("%XX" where XX is the hexadecimal value of the character).
 
 BUGS
        Probably  several.  This  particular  script  has  not been extensively
        tested.
 
 CREDITS
        Written by Timothy D. Morgan.
 
 LICENSE
        Please see the file "LICENSE" included with this software distribution.
 
        This program is distributed in the hope that it  will  be  useful,  but
        WITHOUT  ANY  WARRANTY;  without  even  the  implied  warranty  of MER-
        CHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the  GNU  General
        Public License version 3 for more details.
 
 SEE ALSO
        grokevt(7)   grokevt-addlog(1)  grokevt-builddb(1)  grokevt-findlogs(1)
        grokevt-parselog(1) grokevt-ripdll(1)
 
 File Conversion Utilities        20 June 2011              grokevt-dumpmsgs(1)
 ```
 
 - - -
 
 ##### grokevt-findlogs
 
 Attempts to find log file fragments in raw binary files, such as memory dumps and disk images.
 
 ```
 root@kali:~# grokevt-findlogs --help
 USAGE:
   grokevt-findlogs -?
   grokevt-findlogs [-v] [-h] [-H] [-o <OFFSET>] <RAW_FILE>
 
 grokevt-findlogs attempts to find log file fragments in raw
 binary files, such as memory dumps and disk images.
 Please see the man page for more information.
 ```
 
 - - -
 
 ##### grokevt-parselog
 
 Parse a windows event log and generate human-readable output based on message resources stored in a database.
 
 ```
 root@kali:~# grokevt-parselog -h
 USAGE:
   grokevt-parselog -?|--help
   grokevt-parselog -l <DATABASE_DIR>
   grokevt-parselog -m <DATABASE_DIR> <LOG_TYPE>
   grokevt-parselog [-v] [-H] [-h] <DATABASE_DIR> <LOG_TYPE>
 
 This program parses a windows event log and prints a
 CSV version of the log to stdout.  Please see the man
 page for more information.
 ```
 
 - - -
 
 ##### grokevt-ripdll
 
 A tool for extracting message resources from a PE-formatted file.
 
 ```
 root@kali:~# grokevt-ripdll -h
 USAGE:
   grokevt-ripdll <INPUT_DLL> <OUTPUT_DB>
 
 grokevt-ripdll is a tool for extracting message resources from a PE-formatted file.
 Please see the man page for more information.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
