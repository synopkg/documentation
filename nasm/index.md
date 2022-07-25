---
Title: nasm
Homepage: http://www.nasm.us/
Repository: https://salsa.debian.org/debian/nasm
Architectures: any
Version: 2.15.05-1
Metapackages: kali-linux-arm kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-exploitation kali-tools-forensics kali-tools-post-exploitation kali-tools-reverse-engineering kali-tools-social-engineering kali-tools-top10 kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### nasm
 
  Netwide Assembler.  NASM will currently output flat-form binary files,
  a.out, COFF and ELF Unix object files, and Microsoft 16-bit DOS and
  Win32 object files.
   
  Also included is NDISASM, a prototype x86 binary-file disassembler
  which uses the same instruction table as NASM.
   
  NASM is released under the GNU Lesser General Public License (LGPL).
 
 **Installed size:** `3.22 MB`  
 **How to install:** `sudo apt install nasm`  
 
 {{< spoiler "Dependencies:" >}}
 * dpkg  | install-info
 * libc6 
 {{< /spoiler >}}
 
 ##### ldrdf
 
 Link RDOFF objects and libraries produced by rdflib(1)
 
 ```
 root@kali:~# ldrdf -h
 usage:
    ldrdf [options] object modules ... [-llibrary ...]
    ldrdf -r
 options:
    -v[=n]          increase verbosity by 1, or set it to n
    -a nn           set segment alignment value (default 16)
    -s              strip public symbols
    -dy             Unix-style dynamic linking
    -o name         write output in file 'name'
    -j path         specify objects search path
    -L path         specify libraries search path
    -g file         embed 'file' as a first header record with type 'generic'
    -mn name        add module name record at the beginning of output file
 ```
 
 - - -
 
 ##### nasm
 
 The Netwide Assembler, a portable 80x86 assembler
 
 ```
 root@kali:~# nasm -h
 Usage: nasm [-@ response_file] [options...] [--] filename
        nasm -v (or --v)
 
 Options (values in brackets indicate defaults):
 
     -h            show this text and exit (also --help)
     -v (or --v)   print the NASM version number and exit
     -@ file       response file; one command line option per line
 
     -o outfile    write output to outfile
     --keep-all    output files will not be removed even if an error happens
 
     -Xformat      specifiy error reporting format (gnu or vc)
     -s            redirect error messages to stdout
     -Zfile        redirect error messages to file
 
     -M            generate Makefile dependencies on stdout
     -MG           d:o, missing files assumed generated
     -MF file      set Makefile dependency file
     -MD file      assemble and generate dependencies
     -MT file      dependency target name
     -MQ file      dependency target name (quoted)
     -MP           emit phony targets
 
     -f format     select output file format
        bin                  Flat raw binary (MS-DOS, embedded, ...) [default]
        ith                  Intel Hex encoded flat binary
        srec                 Motorola S-records encoded flat binary
        aout                 Linux a.out
        aoutb                NetBSD/FreeBSD a.out
        coff                 COFF (i386) (DJGPP, some Unix variants)
        elf32                ELF32 (i386) (Linux, most Unix variants)
        elf64                ELF64 (x86-64) (Linux, most Unix variants)
        elfx32               ELFx32 (ELF32 for x86-64) (Linux)
        as86                 as86 (bin86/dev86 toolchain)
        obj                  Intel/Microsoft OMF (MS-DOS, OS/2, Win16)
        win32                Microsoft extended COFF for Win32 (i386)
        win64                Microsoft extended COFF for Win64 (x86-64)
        ieee                 IEEE-695 (LADsoft variant) object file format
        macho32              Mach-O i386 (Mach, including MacOS X and variants)
        macho64              Mach-O x86-64 (Mach, including MacOS X and variants)
        dbg                  Trace of all info passed to output stage
        elf                  Legacy alias for "elf32"
        macho                Legacy alias for "macho32"
        win                  Legacy alias for "win32"
 
     -g            generate debugging information
     -F format     select a debugging format (output format dependent)
     -gformat      same as -g -F format
        elf32:     dwarf     ELF32 (i386) dwarf (newer) [default]
                   stabs     ELF32 (i386) stabs (older)
        elf64:     dwarf     ELF64 (x86-64) dwarf (newer) [default]
                   stabs     ELF64 (x86-64) stabs (older)
        elfx32:    dwarf     ELFx32 (x86-64) dwarf (newer) [default]
                   stabs     ELFx32 (x86-64) stabs (older)
        obj:       borland   Borland Debug Records [default]
        win32:     cv8       Codeview 8+ [default]
        win64:     cv8       Codeview 8+ [default]
        ieee:      ladsoft   LADsoft Debug Records [default]
        macho32:   dwarf     Mach-O i386 dwarf for Darwin/MacOS [default]
        macho64:   dwarf     Mach-O x86-64 dwarf for Darwin/MacOS [default]
        dbg:       debug     Trace of all info passed to debug stage [default]
 
     -l listfile   write listing to a list file
     -Lflags...    add optional information to the list file
        -Lb        show builtin macro packages (standard and %use)
        -Ld        show byte and repeat counts in decimal, not hex
        -Le        show the preprocessed output
        -Lf        ignore .nolist (force output)
        -Lm        show multi-line macro calls with expanded parmeters
        -Lp        output a list file every pass, in case of errors
        -Ls        show all single-line macro definitions
        -Lw        flush the output after every line (very slow!)
        -L+        enable all listing options except -Lw (very verbose!)
 
     -Oflags...    optimize opcodes, immediates and branch offsets
        -O0        no optimization
        -O1        minimal optimization
        -Ox        multipass optimization (default)
        -Ov        display the number of passes executed at the end
     -t            assemble in limited SciTech TASM compatible mode
 
     -E (or -e)    preprocess only (writes output to stdout by default)
     -a            don't preprocess (assemble only)
     -Ipath        add a pathname to the include file path
     -Pfile        pre-include a file (also --include)
     -Dmacro[=str] pre-define a macro
     -Umacro       undefine a macro
    --pragma str   pre-executes a specific %%pragma
    --before str   add line (usually a preprocessor statement) before the input
    --no-line      ignore %line directives in input
 
    --prefix str   prepend the given string to the names of all extern,
                   common and global symbols (also --gprefix)
    --suffix str   append the given string to the names of all extern,
                   common and global symbols (also --gprefix)
    --lprefix str  prepend the given string to local symbols
    --lpostfix str append the given string to local symbols
 
    --reproducible attempt to produce run-to-run identical output
 
     -w+x          enable warning x (also -Wx)
     -w-x          disable warning x (also -Wno-x)
     -w[+-]error   promote all warnings to errors (also -Werror)
     -w[+-]error=x promote warning x to errors (also -Werror=x)
        all                  all possible warnings
        bnd                  invalid BND prefixes [on]
        db-empty             no operand for data declaration [on]
        environment          nonexistent environment variable [on]
        float                all warnings prefixed with "float-"
        float-denorm         floating point denormal [off]
        float-overflow       floating point overflow [on]
        float-toolong        too many digits in floating-point number [on]
        float-underflow      floating point underflow [off]
        hle                  invalid HLE prefixes [on]
        label                all warnings prefixed with "label-"
        label-orphan         labels alone on lines without trailing `:' [on]
        label-redef          label redefined to an identical value [off]
        label-redef-late     label (re)defined during code generation [error]
        lock                 LOCK prefix on unlockable instructions [on]
        macro                all warnings prefixed with "macro-"
        macro-def            all warnings prefixed with "macro-def-"
        macro-def-case-single single-line macro defined both case sensitive and insensitive [on]
        macro-def-greedy-single single-line macro [on]
        macro-def-param-single single-line macro defined with and without parameters [error]
        macro-defaults       macros with more default than optional parameters [on]
        macro-params         all warnings prefixed with "macro-params-"
        macro-params-legacy  improperly calling multi-line macro for legacy support [on]
        macro-params-multi   multi-line macro calls with wrong parameter count [on]
        macro-params-single  single-line macro calls with wrong parameter count [on]
        negative-rep         regative %rep count [on]
        number-overflow      numeric constant does not fit [on]
        obsolete             all warnings prefixed with "obsolete-"
        obsolete-nop         instruction obsolete and is a noop on the target CPU [on]
        obsolete-removed     instruction obsolete and removed on the target CPU [on]
        obsolete-valid       instruction obsolete but valid on the target CPU [on]
        phase                phase error during stabilization [off]
        pragma               all warnings prefixed with "pragma-"
        pragma-bad           malformed %pragma [off]
        pragma-empty         empty %pragma directive [off]
        pragma-na            %pragma not applicable to this compilation [off]
        pragma-unknown       unknown %pragma facility or directive [off]
        ptr                  non-NASM keyword used in other assemblers [on]
        regsize              register size specification ignored [on]
        unknown-warning      unknown warning in -W/-w or warning directive [off]
        user                 %warning directives [on]
        warn-stack-empty     warning stack empty [on]
        zeroing              RESx in initialized section becomes zero [on]
        zext-reloc           relocation zero-extended to match output format [on]
        other                any warning not specifially mentioned above [on]
 
    --limit-X val  set execution limit X
        passes               total number of passes [unlimited]
        stalled-passes       number of passes without forward progress [1000]
        macro-levels         levels of macro expansion [10000]
        macro-tokens         tokens processed during single-lime macro expansion [10000000]
        mmacros              multi-line macros before final return [100000]
        rep                  %rep count [1000000]
        eval                 expression evaluation descent [8192]
        lines                total source lines processed [2000000000]
 ```
 
 - - -
 
 ##### ndisasm
 
 The Netwide Disassembler, an 80x86 binary file disassembler
 
 ```
 root@kali:~# ndisasm -h
 usage: ndisasm [-a] [-i] [-h] [-r] [-u] [-b bits] [-o origin] [-s sync...]
                [-e bytes] [-k start,bytes] [-p vendor] file
    -a or -i activates auto (intelligent) sync
    -u same as -b 32
    -b 16, -b 32 or -b 64 sets the processor mode
    -h displays this text
    -r or -v displays the version number
    -e skips <bytes> bytes of header
    -k avoids disassembling <bytes> bytes from position <start>
    -p selects the preferred vendor instruction set (intel, amd, cyrix, idt)
 ```
 
 - - -
 
 ##### rdf2bin
 
 Convert an RDOFF object file to flat binary
 
 ```
 root@kali:~# rdf2bin -h
 Usage: rdf2bin [options] input-file output-file
 Options:
     -o origin       Specify the relocation origin
     -p alignment    Specify minimum segment alignment
     -f format       Select format (bin, com, ith, srec)
     -q              Run quiet
     -v              Run verbose
 ```
 
 - - -
 
 ##### rdf2com
 
 Convert an RDOFF object file to flat binary
 
 ```
 root@kali:~# rdf2com -h
 Usage: rdf2com [options] input-file output-file
 Options:
     -o origin       Specify the relocation origin
     -p alignment    Specify minimum segment alignment
     -f format       Select format (bin, com, ith, srec)
     -q              Run quiet
     -v              Run verbose
 ```
 
 - - -
 
 ##### rdf2ihx
 
 Convert an RDOFF object file to flat binary
 
 ```
 root@kali:~# rdf2ihx -h
 Usage: rdf2ihx [options] input-file output-file
 Options:
     -o origin       Specify the relocation origin
     -p alignment    Specify minimum segment alignment
     -f format       Select format (bin, com, ith, srec)
     -q              Run quiet
     -v              Run verbose
 ```
 
 - - -
 
 ##### rdf2ith
 
 Convert an RDOFF object file to flat binary
 
 ```
 root@kali:~# rdf2ith -h
 Usage: rdf2ith [options] input-file output-file
 Options:
     -o origin       Specify the relocation origin
     -p alignment    Specify minimum segment alignment
     -f format       Select format (bin, com, ith, srec)
     -q              Run quiet
     -v              Run verbose
 ```
 
 - - -
 
 ##### rdf2srec
 
 Convert an RDOFF object file to flat binary
 
 ```
 root@kali:~# rdf2srec -h
 Usage: rdf2srec [options] input-file output-file
 Options:
     -o origin       Specify the relocation origin
     -p alignment    Specify minimum segment alignment
     -f format       Select format (bin, com, ith, srec)
     -q              Run quiet
     -v              Run verbose
 ```
 
 - - -
 
 ##### rdfdump
 
 Dumps an RDOFF object in human-readable form
 
 ```
 root@kali:~# man rdfdump
 RDFDUMP(1)                       Debian Manual                      RDFDUMP(1)
 
 NAME
        rdfdump - dumps an RDOFF object in human-readable form
 
 SYNOPSIS
        rdfdump [-v] <filename>
 
 DESCRIPTION
        rdfdump  prints  a list of the header records in an RDOFF object in hu-
        man-readable form, and optionally prints a hex dump of the contents  of
        the segments.
 
        rdfdump  supports both version 1 and 2 of RDOFF.  It will give warnings
        if the RDOFF2 format is violated (it looks for  incorrect  lengths  for
        header records, and checks the overall length count at the start of the
        file).
 
 OPTIONS
        -v     Print a hex dump of the contents of the segments.
 
 AUTHORS
        Julian Hall <jules@earthcorp.com>.
 
        This manual page was written by Matej Vela <vela@debian.org>.
 
 Debian Project                 September 6, 1999                    RDFDUMP(1)
 ```
 
 - - -
 
 ##### rdflib
 
 Manage a library file for use with ldrdf(1)
 
 ```
 root@kali:~# rdflib -h
 usage:
   rdflib x libname [extra operands]
 
   where x is one of:
     c - create library
     a - add module (operands = filename module-name)
     x - extract               (module-name filename)
     r - replace               (module-name filename)
     d - delete                (module-name)
     t - list
 ```
 
 - - -
 
 ##### rdx
 
 Load and execute an RDOFF object
 
 ```
 root@kali:~# man rdx
 RDX(1)                           Debian Manual                          RDX(1)
 
 NAME
        rdx - load and execute an RDOFF object
 
 SYNOPSIS
        rdx object
 
 DESCRIPTION
        rdx  loads an RDOFF object, and then calls `_main', which it expects to
        be a C-style function, accepting two parameters, argc and argv in  nor-
        mal C style.
 
 AUTHORS
        Julian Hall <jules@earthcorp.com>.
 
        This manual page was written by Matej Vela <vela@debian.org>.
 
 Debian Project                 September 6, 1999                        RDX(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}