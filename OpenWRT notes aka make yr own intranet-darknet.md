# OpenWRT notes aka make yr own intranet/darknet

By the end of this workshop, you will have your very own network that only people who are in the same physical space can connect to. A single webpage will be shown, that has the ability to change the wifi ssid's so that anyone looking at the local wifi will see anything you type in the webpage, like this:

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_vZiWxCD91Wz_p.266581_1414698273355_haiku.jpg)

So lets get started!

1.  Choose a router from [this](http://wiki.openwrt.org/toh/start) list (scroll down!). We chose:

![](http://www.tp-link.com/resources/images/products/Large/TL-WDR3500_1.0-P1.jpg)

2 Downloaded [openWRT](https://openwrt.org/) image file (the system file) for our specific router (a TP-Link WDR3500. we used [this image](http://downloads.openwrt.org/barrier_breaker/14.07/ar71xx/generic/openwrt-ar71xx-generic-tl-wdr3500-v1-squashfs-factory.bin)) onto our computer. Plug an ethernet cable between your computer and the internet (or incoming signal) ethernet port on your router. On our router, it was blue.

3 Flash the image as a firmware update onto the router using the web interface for that specific router, which we find by going to 192.168.0.1 and then choosing to "update" the firmware and selecting our downloaded image file to use for the update. (we chose this IP address by googling TP-Link router default and finding [this](https://router-defaults.com/Router/TP-LINK--TL-WDR3500-ip-password-username) page. More info on default router configuration can be found [here](http://router-defaults.com/Home).)

4 Using our own computer, fire up the terminal and telnet onto the router so that we can log on and set a password.

*   telnet 192.168.1.1
*

5 set a password

*   passwd 

it will prompt you for a password.

Then log out of telnet (CNTRL-D).

6 Open your web browser and go to 192.168.1.1 It will launch a control panel for the router.

Login in with root and the password you set before.

7 Go to Network > Wifi and Enable wifi. You can now work without the ethernet cable.

8 Open your terminal and use ssh to connect to and transfer files to your router.

*   ssh root@192.168.1.1

It will prompt you for your password to connect to the router.

9 Update OPKG, our package manager, and get usb working. 

(For reference, USB Driver documentation is [here](http://wiki.openwrt.org/doc/howto/usb.essentials))

*   opkg update #[ ](/ep/search/?q=%23updates&via=vZiWxCD91Wz)updates the opkg program, our package manager
*   opkg install kmod-usb2
*   insmod ehci-hcd

10 Install USB storage and disk management packages:

(For reference, USB Storage documentation is [here](http://wiki.openwrt.org/doc/howto/usb.storage))

*   opkg install kmod-usb-storage kmod-fs-ext4 block-mount e2fsprogs fdisk
*

11 Plug in the usb stick and mount it. On our router it was this. Might vary on your router.

*   mount /dev/sda1 /mnt/share

12 We need to run extroot, which "extends the root file system" and allows the router to store system files and run them from the usb stick plugged in. (we followed instructions [here](http://wiki.openwrt.org/doc/howto/extroot), without knowing why pivot overlay is better than pivot root)

*   tar -C /overlay -cvf - . | tar -C /mnt/share -xf -
*

13 Install nano (text editor) so you can more easily edit files

*   opkg install nano

14 Configure the file system table

*   nano /etc/config/fstab
*

15 now edit that file

leave the config 'global' section at the top

below that edit the 'config mount' section

*   config mount
*       option target '/overlay'
*       option device '/dev/sda1'
*       option enabled '1'
*       option fstype 'ext4'

Save it and reboot router.

16 update opkg and install python.

*   opkg update
*   opkg install python

A note that should be unnecessary for most ppl: if you remove python with _opkg remove python_, then make sure you also remove _opkg remove python-mini_ or else when you reinstall python it won't create the needed binaries, so it won't load!

17 install python-openssl

*   opkg install python-openssl

18 download [Python setuptools ](https:// https://bootstrap.pypa.io/ez_setup.py)on your own computer and then move it to the router. type this in your own computer's terminal, not the terminal screen where you are logged in via ssh.

*   scp /Volumes/DISK_IMG/ez_setup.py root@192.168.1.1:/root

19 install the setup tools on the router. move to the terminal window where you've ssh'ed into the router.

*   cd /root
*   python ez_setup.py

20 install flask

*   easy_install flask
*

21 Configure your wireless interfaces to create 3 placeholders (the Python web server will be changing these) and (optionally) one that won't change. 

*   nano /etc/config/wireless

You'll want your wifi-ifaces to be like the following:

*   config 'wifi-iface'
*       option 'device' 'radio0'
*       option 'mode' 'ap'
*       option 'encryption' 'none'
*       option 'network' 'lan'
*       option 'ssid' '-1 ...'
**   config 'wifi-iface'
*       option 'device' 'radio0'
*       option 'mode' 'ap'
*       option 'encryption' 'none'
*       option 'network' 'lan'
*       option 'ssid' '-2 ...'
**   config 'wifi-iface'
*       option 'device' 'radio0'
*       option 'mode' 'ap'
*       option 'encryption' 'none'
*       option 'network' 'lan'
*       option 'ssid' '-3 ...'
**   config 'wifi-iface'
*       option 'device' 'radio0'
*       option 'mode' 'ap'
*       option 'encryption' 'none'
*       option 'network' 'lan'
*       option 'ssid' '-4 --- ☁ haiku wifi ☁ ---'
*       

22 Make LuCI (the default web admin tool for Open-WRT) start up on port 81. In/etc/config/uhttpd, change this line

*   list listen_http    0.0.0.0:80
*   list listen_http '[::]:80'

to

*   list listen_http    0.0.0.0:81
*   list listen_http '[::]:81'

23 Put the web app of [](https://github.com/jedahan/haiku-wifi)https://github.com/jedahan/haiku-wifi[ ](https://github.com/jedahan/haiku-wifion)on your own computer

*   git clone [](https://github.com/jedahan/haiku-wifi)https://github.com/jedahan/haiku-wifi

24 on the router make a directory with /root/arthackday. (switch to your other terminal window on the router)

*   mkdir /root/arthackday

Move back to your own computer and scp (send) the file to the router.

*   cd ..

and then send it to the router in the directory /root/arthackday from your own computer's terminal

*   scp -r haiku-wifi/* root@192.168.1.1:/root/arthackday
*

25 Install the initscript to run the python web app when the router starts up

*   cp /root/arthackday/haiku-wifi/init.d/haiku /etc/init.d haiku

26 give yourself execute permission to this file

*   chmod 775 /etc/init.d/haiku

27 enable it

*   ./haiku enable
*

28 Configure dnsmasq to point all domains at 192.168.1.1. 

*   nano /etc/dnsmasq.conf

Add these lines at the bottom

*   address=/apple.com/0.0.0.0
*   address=/#/192.168.1.1
*

29 Reset the router and connect.