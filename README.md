# python-and-ethical-hacking-course
This is a repository of completed projects from [Learn Python and Ethical Hacking From Scratch](https://www.udemy.com/course/learn-python-and-ethical-hacking-from-scratch/) by zSecurity.

I will be updating this as I complete the course. 

## mac_changer.py
This requires sudo privilege. It is a command line application. It uses `optparse` to get arguments, and then `subprocess` to run the required commands in the Linux Shell. It then uses `re` to check if the MAC address has been changed correctly. 

##  network_scanner.py 
This is a network scanner which works over either individual IPs or ranges. This uses `subprocess` to run the required commands in the Linux Shell. It then uses `re` to check if the MAC address has been changed correctly. This version uses the `argparse` library instead of `optparse`. If you are curious why we would want to do this, you can [read more](https://stackoverflow.com/questions/3217673/why-use-argparse-rather-than-optparse). 

## assignment1.py
This is a variation of the network scanner which uses `optparse` to get arguments for target IP addresses or target IP ranges. There is also a help menu, and a `header()` function to make it a bit prettier. 

## arp_spoof.py
This is an ARP spoofer. It will send packets to the gateway and the target using `scapy` and run until a keyboard interrupt. At this point, it will restore the ARP table. Ideas for future projects include rewriting this program to take user input, likely using `argparse`, and also potentially enable automatic port forwarding. 

## packet_sniffer.py
This is a process that will intercept packets that flow through the host machine. It prints `HTTP`requests and particualarily any traffic that looks like it could be usernames or passwords. This can be run concurrently with the `arp_spoof.py` in order to execute a [man in the middle attack](https://en.wikipedia.org/wiki/Man-in-the-middle_attack). Note that this program seems to only capture `HTTP` traffic and not `HTTPS`. It also only has 6 keywords to look for as potential usernames and passwords. A future project can be to expand the list, as well as to filter out more traffic. 
