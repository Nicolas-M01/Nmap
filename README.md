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

* TCP Connect Scans (-sT)  
* SYN "Half-open" Scans (-sS)  
* UDP Scans (-sU)  














To run a specific script, we would use ``--script=<script-name>``
