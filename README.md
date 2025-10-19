Sources:

https://feodotracker.abuse.ch/downloads/ipblocklist.txt

https://blocklist.greensnow.co/greensnow.txt

https://raw.githubusercontent.com/stamparm/ipsum/refs/heads/master/levels/5.txt

https://rules.emergingthreats.net/blockrules/compromised-ips.txt

https://threatfox.abuse.ch/export/json/ip-port/recent/

https://lists.blocklist.de/lists/strongips.txt

https://threatview.io/Downloads/IP-High-Confidence-Feed.txt


Script on Mikrotik:

``
/tool fetch url="https://raw.githubusercontent.com/ion-lane/IP_blocklist_mikrotik/main/ip_blocklist.rsc" mode=https dst-path=usb1
``

``
/ip firewall address-list remove [find where list="BLOCKLIST"]; /import file-name=usb1/ip_blocklist.rsc; /file remove usb1/ip_blocklist.rsc
``

! I recommend using a USB flash drive ``dst-path=usb1``  to download lists daily.
