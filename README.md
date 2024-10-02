Sources:

https://feodotracker.abuse.ch/downloads/ipblocklist_recommended.txt

https://feodotracker.abuse.ch/downloads/ipblocklist.txt

https://blocklist.greensnow.co/greensnow.txt

https://pgl.yoyo.org/adservers/iplist.php?ipformat=&showintro=0&mimetype=plaintext

https://raw.githubusercontent.com/HybridNetworks/BlackListBox/main/Mikrotik/HN-BLACKLIST-TALOSINTELLIGENCE.rsc

https://raw.githubusercontent.com/stamparm/ipsum/refs/heads/master/levels/6.txt

https://rules.emergingthreats.net/blockrules/compromised-ips.txt

ToDo:

http://www.talosintelligence.com/documents/ip-blacklist

https://raw.githubusercontent.com/C24Be/AS_Network_List/main/blacklists/blacklist.txt


Script on Mikrotik:

``
/tool fetch url="https://raw.githubusercontent.com/ion-lane/IP_blocklist_mikrotik/main/ip_blocklist.rsc" mode=https dst-path=usb1
``

``
/ip firewall address-list remove [find where list="BLOCKLIST"]; /import file-name=usb1/ip_blocklist.rsc; /file remove usb1/ip_blocklist.rsc
``

! I recommend using a USB flash drive ``dst-path=usb1``  to download lists daily.
