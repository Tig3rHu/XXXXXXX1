# XXXXXXX1
poc.py

Author:TigerOrTiger

###  introduction 

1. In the bifrost binary component of the device, there is a risk of buffer overflow for the Authorization parameter obtained in the check_token function.
2. A buffer overflow vulnerability can become a denial of service vulnerability in the router
3. This vulnerability can be triggered without authentication

### The firmware simulation

#### The first way
First unpack the firmware package using BinWalk
Locate the "Bifrost" binary component in the /bin/ folder
Run the component with "sudo chroot.. /qemu-mipsel-static./bin/bifrost"
Use Firefox to access port 80 to determine successful emulation

#### The second way
Automated emulation of "gf1200-1.10.6.35824_headerless.bin" using fat.py
Use Firefox to access port 80 to determine successful emulation
The simulation integrity is better this way

### Triggering holes

python poc.py -target http://targetip
