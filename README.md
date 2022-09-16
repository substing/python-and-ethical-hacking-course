# python-and-ethical-hacking-course
This is a repository of completed projects from [Learn Python and Ethical Hacking From Scratch](https://www.udemy.com/course/learn-python-and-ethical-hacking-from-scratch/) by zSecurity.

I will be updating this as I complete the course. 

## mac_changer.py
This requires sudo privilege. It is a command line application. It uses `optparse` to get arguments, and then `subprocess` to run the required commands in the Linux Shell. It then uses `re` to check if the MAC address has been changed correctly. 

## network_scanner.py
This is a simple script which uses `scapy` in order to find the MAC addresses of either a single target or a whole range of targets. It does not accept arguments, and needs to be edited manually. 

## assignment1.py
This is a variation of the network scanner which uses `optparse` to get arguments for target IP addresses or target IP ranges. There is also a help menu, and a `header()` function to make it a bit prettier. 

##  network_scanner_python3.py 
This file is another variation on the network scanner. This version uses the `argparse` library instead of `optparse`. If you are curious why we would want to do this, you can [read more](https://stackoverflow.com/questions/3217673/why-use-argparse-rather-than-optparse). The function should still be the same. 

## arp_spoof.py
This is an ARP spoofer. It will send packets to the gateway and the target using `scapy` and run until a keyboard interrupt. At this point, it will restore the ARP table.
