Sources:

https://feodotracker.abuse.ch/downloads/ipblocklist_recommended.txt

https://blocklist.greensnow.co/greensnow.txt

https://pgl.yoyo.org/adservers/iplist.php?ipformat=&showintro=0&mimetype=plaintext

https://raw.githubusercontent.com/HybridNetworks/BlackListBox/main/Mikrotik/HN-BLACKLIST-TALOSINTELLIGENCE.rsc

https://raw.githubusercontent.com/stamparm/ipsum/refs/heads/master/levels/6.txt

ToDo:

https://raw.githubusercontent.com/C24Be/AS_Network_List/main/blacklists/blacklist.txt


Script on Mikrotik:

/tool fetch url="https://raw.githubusercontent.com/ion-lane/IP_blocklist_mikrotik/main/ip_blocklist.rsc" mode=https

/ip firewall address-list remove [find where list="BLOCKLIST"]; /import file-name=ip_blocklist.rsc; /file remove ip_blocklist.rsc
