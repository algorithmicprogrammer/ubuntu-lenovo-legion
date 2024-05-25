# Ubuntu on Lenovo Legion

## Table of Contents
1. [My System](#my-system)
	- [My Machine](#my-machine)
	- [Operating System](#operating-system)
1. [Installing Ubuntu](#installing-ubuntu)
	- [Creating a Bootable USB Stick](#creating-a-bootable-usb-stick)
	- [Disabling Secure Boot](#disabling-secure-boot)
	- [What Works Out-of-the-Box](#what-works-out-of-the-box)

## My System
### My Machine
<ul>
	<li><b>Model:</b> Lenovo Legion 7i</li>
	<li><b>Model No:</b> 83FD0015US</li>
	<li><b>Generation:</b> 9th</li>
	<li><b>Screen Size:</b> 16 inches</li>
	<li><b>CPU:</b> 14th generation Intel Core i9</li>
	<li><b>GPU:</b> Nvidia GeForce RTX 4070</li>
	<li><b>RAM:</b> 32 GB</li>
	<li><b>Storage:</b> 1 TB SSD</li>
</ul>

### Operating System
<ul>
	<li>Ubuntu 24.04 LTS</li>
</ul>

## Installing Ubuntu
### Creating a Bootable USB Stick
In the installation tutorial on the Ubuntu website, balenaEtcher is used to write the downloaded ISO to the USB stick. However, if you're using a Windows machine to create your bootable USB stick, I recommend using Rufus instead of balenaEtcher. Detailed instructions for creating a bootable USB stick with Rufus are available <a href="https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#1-overview">here</a>, on the Ubuntu website. The reason I don't recommend using balenaEtcher is because it creates partitions in your USB and won't format the disk due to write protection (this isn't an issue that can be resolved with diskpart, regedit, or Properties). You won't run into any of these problems with Rufus. 

### Disabling Secure Boot
Before initiating your Ubuntu installation, it is good practice to disable secure boot on your device. In order to do this, when your laptop is powering on, press down the F2 key. Then, click on "More Settings". Then click on "Security" in the left hand panel. Scroll down until you see "Secure Boot" and click "Disabled" on the right hand dropdown. 

### What Works Out-of-the-Box
<ul>
	<li>Wi-Fi</li>
	<li>power button</li>
	<li>RGB keyboard backlighting</li>
	<li>audio (headphones/speakers)</li>
</ul>

### What Doesn't Work Out-of-the-Box
<ul>
	<li>number keypad</li>
</ul>
  
