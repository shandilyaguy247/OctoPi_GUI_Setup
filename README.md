# OctoPi GUI Setup

A quick and easy guide to setting up OctoPi for beginners with zero experience. Follow these steps to setup OctoPi OS on your Raspberry Pi in a few basic steps regardless of your machine's operating system.

![Octopi image](https://user-images.githubusercontent.com/64366648/84556016-58e23580-ad20-11ea-9105-232916981913.jpg)

So what exactly is OctoPrint? Here is a list of things OctoPrint allows you to do:

* Wirelessly upload G-code files from a computer to a 3D printer
* Manually control a 3D printer (moving the X-, Y-, and Z-axes as well as forcing extrusion)
* Monitor print temperature and change print settings
* Set up a webcam to view the Print in real time and create time lapse videos
* Slice models using CuraEngine Legacy
* Customize operation with numerous plug-ins

## Installation

### Hardware Prerequisites:

* Raspberry Pi (Model 3B or later, Raspberry Pi Zero/Zero W not recommended)
* 5.1V/2.5 A Micro USB power supply (For the RPi)
* MicroSD card (preferably 16GB or larger)
* MicroSD card reader
* USB Mouse and Keyboard
* HDMI Monitor
* Stable WiFi
* Desktop/Laptop

### Preparing the MicroSD Card:

* Download the latest image of OctoPi from
https://octoprint.org/download/

<img width="1440" alt=" " src="https://user-images.githubusercontent.com/64366648/84555969-11f44000-ad20-11ea-85c6-29e10392f7eb.png">

* Next download an etching tool:
https://www.balena.io/etcher/

<img width="1440" alt=" " src="https://user-images.githubusercontent.com/64366648/84556036-757e6d80-ad20-11ea-99a6-8622c362505d.png">



* Insert the MicroSD card into the MicroSD card reader and connect it to your machine.

* Format the MicroSD card (FAT32 formatting only)

* Using Etcher, flash the disk image of the OctoPi OS onto the MicroSD card

* Once the flashing is complete, insert the MicroSD card into the Raspberry Pi

### Setting up the Raspberry Pi:

* Connect the Raspberry Pi to the monitor, mouse and the keyboard and power it up.

* Your Raspberry Pi will boot up automatically.

* After the boot is complete, you will see the following:

![OctoPi Login](https://user-images.githubusercontent.com/64366648/84556109-ec1b6b00-ad20-11ea-9ee3-7123f930bc2d.png)

* octopi login: pi
* Password : raspberry

You are now sucessfully logged in!

### Enable GUI:

* Enter the following command into the bash terminal:

>> sudo raspi-config

* Re-enter the password.

* Use the arrow keys to navigate to "Network Options"

![ ](https://user-images.githubusercontent.com/64366648/84556137-110fde00-ad21-11ea-8726-bd4332c18117.png)


* Select "N2 Wi-fi"

![ ](https://user-images.githubusercontent.com/64366648/84556209-25ec7180-ad21-11ea-819f-c04b43b368b2.png)


* Enter the SSID (Name of your Wifi network), and click "<Ok>".
* Enter the password of the Wifi (if none, leave blank), and click "<Ok>".

* Click "<Finish>"

You are now back in the bash command line.

Enter:

>> sudo /home/pi/scripts/install-desktop

* Enter the password, press any key to continue.

* You will be asked whether you want the Pi to boot up into a desktop environment by default. Type ‘yes’ and hit Enter. We can disable this functionality later on if we want to.

* The resources for the desktop GUI will now download and install automatically
* When complete, Type: 

>> sudo reboot

The Pi will now reboot to OctoPi Desktop GUI.

* Enter the username and password.

![4](https://user-images.githubusercontent.com/64366648/84556230-57653d00-ad21-11ea-913b-9f830dc7ebf6.png)

Your OctoPi GUI is now ready!

![The OctoPi Desktop GUI](https://user-images.githubusercontent.com/64366648/84556245-7ebc0a00-ad21-11ea-9fbe-6b6a640fc52d.png)

To update your RPi with all the latest packages and releases, type the following:

>> sudo apt update

* Enter the password.

>> sudo apt full-upgrade

* When prompted, enter "Y".

After the processes have finished type:

>> sudo reboot

Your system will reboot with all the changes.

### Your Raspberry Pi - OctoPi is up and ready to use!

## Up Next: How to enable remote access to OctoPi using VNC:

https://github.com/shandilyaguy247/Enable_Remote_Access_to_Raspberry_Pi-OctoPi_Using_VNC

## Meta

**Harshit Shandilya - (https://www.linkedin.com/in/harshitshandilya/ **

Affero General Public License (AGPL)

https://github.com/shandilyaguy247

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b`)
3. Commit your changes (`git commit -am`)
4. Push to the branch (`git push origin`)
5. Create a new Pull Request
6. For major changes, please open an issue first to discuss what you would like to change.
