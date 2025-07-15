# Nmap

Il y 65535 ports sur un ordinateurs. Les 1024 premiers sont les ports bien connus.  


### :clipboard: Some common switches :  

``-sS`` : Scan TCP SYN  
``-sU`` : Scan UDP  
``-O`` : Get operating System  
``-sV`` : Version du service.  
`-v` : verbose,  `-vv` : verbose+ ...  
`-oA` : Save in the 3 majors formats  
`-oG` : Save results in "grepable" format  
``-A`` : Agressive mode Enable OS detection, version detection, script scanning, and traceroute  
`-T5` : Increase speed (from 1 to 5), be careful : higher speeds are noisier, and can incur errors  
`-p 80` : scan only port 80.  
`-p 1000-1500` : Scan ports 1000 to 15000  
`-p-` : Scan ***All*** ports  
`--script` : Activate a script from nmap library  
`--script=vuln` : Activate all the scripts in the "vuln" category.  

### 3 basics scans  

These are used in most situations  
####  1) TCP Connect Scans (``-sT``)  
If Nmap sends a TCP request with the SYN flag set to a _closed_ port, the target server will respond with a TCP packet with the RST (Reset) flag set and Nmap can establish that the port is closed  
If, however, the request is sent to an _open_ port, the target will respond with a TCP packet with the SYN/ACK flags set. Nmap then marks this port as being open (and completes the handshake by sending back a TCP packet with ACK set).  
If the port is open but hidden behind a firewall, the firewall will _drop_ incomings packets. Nmap sends a TCP SYN request, and receives nothing back. This indicates that the port is being protected by a firewall and thus the port is considered to be filtered.  
If a port is closed, the flag RST is sent back from the target.  

#### 2) SYN "Half-open" Scans (``-sS``)  
As with TCP scans, SYN scans (-sS) are used to scan the TCP port-range of a target or targets; however, the two scan types work slightly differently. SYN scans are sometimes referred to as "Half-open" scans, or "Stealth" scans.  
Where TCP scans perform a full three-way handshake with the target, SYN scans sends back a RST TCP packet after receiving a SYN/ACK from the server (this prevents the server from repeatedly trying to make the request)  




#### 3) UDP Scans (``-sU``)  




### Additional port scan types  

TCP Null Scans (``-sN``)  
TCP FIN Scans (``-sF``)  
TCP Xmas Scans (``-sX``)  

TCP Connect Scan (``
if Nmap sends a TCP request with the SYN flag set to a closed port, the target server will respond with a TCP packet with the RST (Reset) flag set







To run a specific script, we would use ``--script=<script-name>``
