---
Title: theharvester
Homepage: https://github.com/laramies/theHarvester
Repository: https://gitlab.com/kalilinux/packages/theharvester
Architectures: all
Version: 4.0.3-0kali1
Metapackages: kali-linux-arm kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/theharvester-logo.svg
PackagesInfo: |
 ### theharvester
 
  The package contains a tool for gathering subdomain names, e-mail addresses,
  virtual hosts, open ports/ banners, and employee names from different public
  sources (search engines, pgp key servers).
 
 **Installed size:** `1.75 MB`  
 **How to install:** `sudo apt install theharvester`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 * python3-aiodns 
 * python3-aiofiles
 * python3-aiohttp 
 * python3-aiomultiprocess 
 * python3-aiosqlite 
 * python3-bs4 
 * python3-censys
 * python3-certifi
 * python3-dnspython 
 * python3-fastapi 
 * python3-lxml 
 * python3-netaddr 
 * python3-pyppeteer 
 * python3-requests 
 * python3-retrying 
 * python3-shodan 
 * python3-slowapi
 * python3-spyse
 * python3-starlette
 * python3-texttable 
 * python3-ujson
 * python3-uvicorn
 * python3-uvloop 
 * python3-yaml 
 {{< /spoiler >}}
 
 ##### restfulHarvest
 
 
 ```
 root@kali:~# restfulHarvest -h
 usage: restfulHarvest [-h] [-H HOST] [-p PORT] [-l LOG_LEVEL] [-r]
 
 options:
   -h, --help            show this help message and exit
   -H HOST, --host HOST  IP address to listen on default is 127.0.0.1
   -p PORT, --port PORT  Port to bind the web server to, default is 5000
   -l LOG_LEVEL, --log-level LOG_LEVEL
                         Set logging level, default is info but
                         [critical|error|warning|info|debug|trace] can be set
   -r, --reload          Enable automatic reload used during development of the
                         api
 ```
 
 - - -
 
 ##### theHarvester
 
 
 ```
 root@kali:~# theHarvester -h
 
 *******************************************************************
 *  _   _                                            _             *
 * | |_| |__   ___    /\  /\__ _ _ ____   _____  ___| |_ ___ _ __  *
 * | __|  _ \ / _ \  / /_/ / _` | '__\ \ / / _ \/ __| __/ _ \ '__| *
 * | |_| | | |  __/ / __  / (_| | |   \ V /  __/\__ \ ||  __/ |    *
 *  \__|_| |_|\___| \/ /_/ \__,_|_|    \_/ \___||___/\__\___|_|    *
 *                                                                 *
 * theHarvester 4.0.3                                              *
 * Coded by Christian Martorella                                   *
 * Edge-Security Research                                          *
 * cmartorella@edge-security.com                                   *
 *                                                                 *
 ******************************************************************* 
 
 
 usage: theHarvester [-h] -d DOMAIN [-l LIMIT] [-S START] [-g] [-p] [-s]
                     [--screenshot SCREENSHOT] [-v] [-e DNS_SERVER]
                     [-t DNS_TLD] [-r] [-n] [-c] [-f FILENAME] [-b SOURCE]
 
 theHarvester is used to gather open source intelligence (OSINT) on a company
 or domain.
 
 options:
   -h, --help            show this help message and exit
   -d DOMAIN, --domain DOMAIN
                         Company name or domain to search.
   -l LIMIT, --limit LIMIT
                         Limit the number of search results, default=500.
   -S START, --start START
                         Start with result number X, default=0.
   -g, --google-dork     Use Google Dorks for Google search.
   -p, --proxies         Use proxies for requests, enter proxies in
                         proxies.yaml.
   -s, --shodan          Use Shodan to query discovered hosts.
   --screenshot SCREENSHOT
                         Take screenshots of resolved domains specify output
                         directory: --screenshot output_directory
   -v, --virtual-host    Verify host name via DNS resolution and search for
                         virtual hosts.
   -e DNS_SERVER, --dns-server DNS_SERVER
                         DNS server to use for lookup.
   -t DNS_TLD, --dns-tld DNS_TLD
                         Perform a DNS TLD expansion discovery, default False.
   -r, --take-over       Check for takeovers.
   -n, --dns-lookup      Enable DNS server lookup, default False.
   -c, --dns-brute       Perform a DNS brute force on the domain.
   -f FILENAME, --filename FILENAME
                         Save the results to an XML and JSON file.
   -b SOURCE, --source SOURCE
                         anubis, baidu, bing, binaryedge, bingapi,
                         bufferoverun, censys, certspotter, crtsh, dnsdumpster,
                         duckduckgo, fullhunt, github-code, google,
                         hackertarget, hunter, intelx, linkedin,
                         linkedin_links, n45ht, omnisint, otx, pentesttools,
                         projectdiscovery, qwant, rapiddns, rocketreach,
                         securityTrails, spyse, sublist3r, threatcrowd,
                         threatminer, trello, twitter, urlscan, virustotal,
                         yahoo, zoomeye
 ```
 
 - - -
 
 ##### theharvester
 
 
 ```
 root@kali:~# theharvester -h
 ┏━(Message from Kali developers)
 ┃
 ┃ The command theharvester is deprecated. Please use theHarvester instead.
 ┃
 ┗━
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## theharvester Usage Example

Search from email addresses from a domain (`-d kali.org`), limiting the results to 500 (`-l 500`), using Google (`-b google`):

```
root@kali:~# theharvester -d kali.org -l 500 -b google

*******************************************************************
*                                                                 *
* | |_| |__   ___    /\  /\__ _ _ ____   _____  ___| |_ ___ _ __  *
* | __| '_ \ / _ \  / /_/ / _` | '__\ \ / / _ \/ __| __/ _ \ '__| *
* | |_| | | |  __/ / __  / (_| | |   \ V /  __/\__ \ ||  __/ |    *
*  \__|_| |_|\___| \/ /_/ \__,_|_|    \_/ \___||___/\__\___|_|    *
*                                                                 *
* TheHarvester Ver. 3.0.0                                         *
* Coded by Christian Martorella                                   *
* Edge-Security Research                                          *
* cmartorella@edge-security.com                                   *
*******************************************************************


[-] Starting harvesting process for domain: kali.org

[-] Searching in Google:
    Searching 0 results...
    Searching 100 results...
    Searching 200 results...
    Searching 300 results...
    Searching 400 results...
    Searching 500 results...

 Harvesting results
[...]
```