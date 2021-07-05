###### Why do i need to install this?
The version 1 of TP- Link's TL-WN722N Adapter has Atheros chipset but TL-WN722N version 2,3 has Realtek. This will not enable monitor mode on default and hence we need to install drivers to be able to use monitor mode

### Commands
1. Update and Upgrade your system(I am using Kali linux)
``` 
sudo apt update && sudo apt upgrade
```

2. Install some modules 
```
1> sudo apt install bc 
2> sudo apt install build-essential       
3> sudo apt install libelf-dev 
4> sudo apt install dkms
5> sudo apt install linux-headers-$(uname -r)
```

3. Now reboot your pc
```
sudo reboot
```

4. Removing existing driver
```
sudo rmmod r8188eu.ko
```

5. Cloning new Drivers from Github
```
git clone https://github.com/aircrack-ng/rtl8188eus
```
6. Open the cloned folder and escalate our previllage
```
1. cd rtl8188eus
2. sudo -i
3. echo "blacklist r8188eu.ko" > "/etc/modprobe.d/realtek.conf"
4. exit
```
7. Compiling and installing fies
```
sudo make && make install
```
8. Last command
```
sudo modprobe 8188eu
```

Thats it!! now to verify the drivers 
```
// this will show your wlan0 is in auto or managed mode
1. iwconfig 
2. sudo airmon-ng (here you will see phy0 or phy1 under PHY section, if NULL is shown then you may have missed in the above steps)
// To change that to monito
3. sudo airmon-ng check kill
4. sudo airmon-ng start wlan0 //This will now start monitor mode
5. iwconfig // you will be shown monitor mode here now 
// To verify Packet injection 
6. sudo aireplay-ng --test wlan0
  this will show "injection is working"
  
#### Happy Hacking
