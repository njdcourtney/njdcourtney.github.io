---
layout: blog
title: How to connect a raspberry pi to wifi on first boot.
tags: raspberrypi

---

The Raspberry pi [https://www.raspberrypi.org/] makes a great headless server sitting tucked away in a corner somewhere quietly getting on with its job. However, thanks to SSH being disabled by default in Rasbian and wifi pre-shared keys being a thing, I've often found myself having to break out a network and HDMI cable to get access to my Pis to set them up.

However it turns out to be relatively simple to enable WiFi and get them connected to wifi right from first boot. For this I was using a Raspberry Pi 3B Plus and Rasbian Stretch Lite.

### Step one -  Download latest Raspian

First you'll need a copy of Rasbian from the official downloads page [https://www.raspberrypi.org/downloads/]. The whole point of this article is setting up a headless server, so Im using the Lite version. Don't copy the image to the SD card just yet, we need to make some change first.

### Step two - Enable SSH.

This turns out this is really easy to do. If you mount the disk image (how to do this is OS dependent, on a Mac all you have to do is double-click on the .img file) and add a blank file called 'SSH' That's it, this will enable SSH when the pi boots.

### Step three - Supply WiFi details.

You can add a 'wpa_supplicant.conf' file to the boot image, this will be picked up by the pi at first boot and used to configure the wireless. The format of this file is this:

<pre>
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=GB

network={
        ssid="YourWirelessSSID"
        psk="YouWirelessPassword"
}
</pre>

Tou need to change the country code to match wherever you're using your Pi. For regulatory reasons the Pi won't enable the wireless chip until it knows what country it's in. Obviously you need to supply the correct SSID and passphrase.

### Step four - copy image to SD card and boot.

Unmount the Raspbian image and copy it to your SD card in the normal way [https://www.raspberrypi.org/documentation/installation/installing-images/README.md]

If everything's gone to plan your Pi should boot and connect to your wireless network right from first boot, all you'll need to do is look at your DHCP server to see what IP address it's been allocated and SSH to it. No network cables, HDMI or external monitors required.

### Step five - security!

Don't forget this step.

Leaving your wifi password lying around in plain text isn't a very good idea. Luckily once you've got a working Pi you can use the 'wpa_passphrase' tool to hash your wifi password. There are great instructions on how to do this here: [https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md]. 

Once you've got a properly working wpa_supplicant.conf file, you can copy it off your pi to use it if you ever need to set up another one.

While you're there, don't forget to change the pi user password to something, don't leave it on the default, you will get hacked...

