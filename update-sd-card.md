# Updating and upgrading your SD card

Keeping the software on your SD card up to date is a good starting point for any project and is very simple to do. Your Raspberry Pi will need to be connected to the internet via an Ethernet cable or WiFi in order for these steps to work.

## Update

You will need to type a command into a terminal window, or on the command line, once you have logged into your Pi.

1. Open a **Terminal** window by clicking on **Main Menu**, **Accessories** and **Terminal**. Alternatively, you can click on the Terminal icon in the taskbar.
1. Next, type the following:

  ```bash
  sudo apt-get update
  ```
  
1. Then press **Enter** on the keyboard.

 You will see some text appear very quickly. Simply wait for the progress indicator at the bottom to reach 100% and then you will be returned to the command line prompt.

## Upgrade

Once the update process is complete, and any information about new versions of applications are downloaded, you will need to install the upgrades.

1. In a terminal window or on the command line type:

  ```bash
  sudo apt-get upgrade
  ```
  
1. Press **Y** or **Enter** on the keyboard when prompted and your upgrades will be installed.

## Checking space on an SD card

When running `sudo apt-get upgrade`, it will show how much data will be downloaded and how much space it will take up on the SD card. It's worth checking with `df -h` to ensure that you have enough disk space free, as unfortunately `apt` will not do this for you. Also be aware that downloaded package files (.deb files) are kept in `/var/cache/apt/archives`. You can remove these in order to free up space with `sudo apt-get clean`.

## What next?
- Return to [Quick Start Guide](worksheet.md)
- Install more [applications](install-apps.md)
- Connect your Raspberry Pi to [WiFi](wifi.md)
