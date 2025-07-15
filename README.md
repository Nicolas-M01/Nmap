# Nmap

Il y 65535 ports sur un ordinateurs. Les 1024 premiers sont les ports bien connus.  


### Some common switches :  

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




To run a specific script, we would use ``--script=<script-name>``
