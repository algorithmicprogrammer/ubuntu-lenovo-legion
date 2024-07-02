# Ubuntu on Lenovo Legion
This is a comprehensive guide for installing, using, and optimizing Ubuntu on a Lenovo Legion device. This guide is geared towards individuals who are new to Ubuntu and/or Linux, coming from a different operating system (MacOS or Windows).

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
	<li>basic keyboard functionality</li>
	<li>RGB keyboard backlighting</li>
	<li>audio (headphones/speakers)</li>
	<li>USB-A ports</li>
</ul>

### What Doesn't Work Out-of-the-Box
<ul>
	<li>brightness keys</li>
	<li>volume keys</li>
</ul>
  
## Troubleshooting Potential Issues 
### Connecting to a WiFi Network
Just to be clear, WiFi does work out-of-the-box with Ubuntu 24.04 LTS. However, you may have trouble connecting to a WiFi network at a hotel or coffee shop which requires you to enter a password, agree to certain terms & conditions, provide your email address, etc. This is because the window which prompts users for a password, email, etc. won't appear automatically upon attempting to connect to a WiFi network. Fortunately, there is an easy workaround for this. Type <code>ip route</code> into your terminal. Copy the default IP address into your browser. That will direct you to the  login page for the network.

### Node.js and npm
<code>sudo apt install nodejs</code> installs Node.js version 18.19.1 as opposed to the latest LTS release (20.13.1). <code>sudo apt install npm</code> installs npm version 9.2.0 when the latest version is 10.8.0.
