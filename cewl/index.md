---
Title: cewl
Homepage: https://github.com/digininja/CeWL
Repository: https://salsa.debian.org/pkg-security-team/cewl
Architectures: all
Version: 5.5.2-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: images/cewl-logo.svg
PackagesInfo: |
 ### cewl
 
  CeWL (Custom Word List generator) is a ruby app which spiders
  a given URL, up to a specified depth, and returns a list of
  words which can then be used for password crackers such as John
  the Ripper. Optionally, CeWL can follow  external links.
   
  CeWL can also create a list of email addresses found in mailto
  links. These email addresses can be used as usernames in brute
  force actions.
   
  Another tool provided by CeWL project is FAB (Files Already
  Bagged). FAB extracts the content of the author/creator fields,
  from metadata of the some files, to create lists of possible
  usernames. These usernames can be used in association with the
  password list generated by CeWL. FAB uses the same metadata
  extraction techniques that CeWL. Currently, FAB process Office
  pre 2007, Office 2007 and PDF formats.
   
  CeWL is useful in security tests and forensics investigations.
  CeWL is pronounced "cool".
 
 **Installed size:** `80 KB`  
 **How to install:** `sudo apt install cewl`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 * ruby-mime
 * ruby-mime-types
 * ruby-mini-exiftool
 * ruby-net-http-digest-auth
 * ruby-nokogiri
 * ruby-spider
 * ruby-zip
 {{< /spoiler >}}
 
 ##### cewl
 
 Custom word list generator
 
 ```
 root@kali:~# cewl -h
 CeWL 5.5.2 (Grouping) Robin Wood (robin@digi.ninja) (https://digi.ninja/)
 Usage: cewl [OPTIONS] ... <url>
 
     OPTIONS:
 	-h, --help: Show help.
 	-k, --keep: Keep the downloaded file.
 	-d <x>,--depth <x>: Depth to spider to, default 2.
 	-m, --min_word_length: Minimum word length, default 3.
 	-o, --offsite: Let the spider visit other sites.
 	--exclude: A file containing a list of paths to exclude
 	--allowed: A regex pattern that path must match to be followed
 	-w, --write: Write the output to the file.
 	-u, --ua <agent>: User agent to send.
 	-n, --no-words: Don't output the wordlist.
 	-g <x>, --groups <x>: Return groups of words as well
 	--lowercase: Lowercase all parsed words
 	--with-numbers: Accept words with numbers in as well as just letters
 	--convert-umlauts: Convert common ISO-8859-1 (Latin-1) umlauts (ä-ae, ö-oe, ü-ue, ß-ss)
 	-a, --meta: include meta data.
 	--meta_file file: Output file for meta data.
 	-e, --email: Include email addresses.
 	--email_file <file>: Output file for email addresses.
 	--meta-temp-dir <dir>: The temporary directory used by exiftool when parsing files, default /tmp.
 	-c, --count: Show the count for each word found.
 	-v, --verbose: Verbose.
 	--debug: Extra debug information.
 
 	Authentication
 	--auth_type: Digest or basic.
 	--auth_user: Authentication username.
 	--auth_pass: Authentication password.
 
 	Proxy Support
 	--proxy_host: Proxy host.
 	--proxy_port: Proxy port, default 8080.
 	--proxy_username: Username for proxy, if required.
 	--proxy_password: Password for proxy, if required.
 
 	Headers
 	--header, -H: In format name:value - can pass multiple.
 
     <url>: The site to spider.
 
 ```
 
 - - -
 
 ##### fab-cewl
 
 Extract metadata from files
 
 ```
 root@kali:~# fab-cewl -h
 fab-cewl
 
 Usage: fab-cewl [OPTION] ... filename/list
 	-h, --help: show help
 	-v: verbose
 	
 	filename/list: the file or list of files to check
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## cewl Usage Example

Scan to a depth of 2 (`-d 2`) and use a minimum word length of 5 (`-m 5`), save the words to a file (`-w docswords.txt`), targeting the given URL (`https://example.com`):

```
root@kali:~# cewl -d 2 -m 5 -w docswords.txt https://example.com
CeWL 5.4.3 (Arkanoid) Robin Wood (robin@digi.ninja) (https://digi.ninja/)
root@kali:~# wc -l docswords.txt
13 docswords.txt
```
