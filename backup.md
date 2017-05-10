# Backing up your home folder

It's likely that all your important files are in a directory on your SD card called `/home/pi`. This resource assumes this is where you have been keeping your files. If they are elsewhere on your SD card, then you might have to copy them into `/home/pi`.

## Backing up using removable storage

If you have a USB flash drive or a portable hard drive with enough storage, then this is the easiest method to back up your files.

1. Insert your USB drive into one of your Pi's USB ports; it should be recognised straight away.

  ![USB](images/usb1.png)

1. Open the USB drive in **File Manager**.

1. Use File Manager to open a second window and position it alongside the first window.

  ![USB](images/usb2.png)

1. You can now copy the contents of `/home/pi` onto the USB drive.

If you can't copy the files over, it probably means you're using a USB drive that has been formatted to be used with Mac OS X. Try formatting the USB drive with a FAT32 file system, using your Mac's Disk Utility.

## Backing up over a network

You're going to need your Raspberry Pi's IP address to copy files over a network.

1. Boot up your Raspberry Pi, ensure it's connected to the network, and then open a terminal window.

1. In the terminal, type:

  ```bash
  hostname -I
  ```

1. The Raspberry Pi's IP address will be displayed.

### Linux and Mac instructions

1. On your Linux computer or Mac, ensure you're connected to the **same** network as the Raspberry Pi, then open a terminal window.

1. Now type the following into the terminal, replacing the IP address with the one you have taken from the Raspberry Pi:

  ```bash
  rsync -av --exclude".*/" pi@192.168.1.111:/home/pi/ ~/RPi-backup
  ```

1. If you now look in your Mac or Linux machine's home directory, you should see a folder called `RPi-backup`, containing all your files.

### Windows instructions

1. Ensure your Windows machine is connected to the **same** network as the Raspberry Pi.

1. To copy files over the network to a Windows machine, you'll need to install a program called WinSCP.

1. Go to [the WinSCP download page](http://winscp.net/eng/download.php).

1. Download the portable executable:

  ![winscp](images/winscp1.png)

1. If you check in your Downloads folder, you should see the following files. Double-click on the WinSCP **application** (not the MS-DOS application):

  ![winscp](images/winscp2.png)

1. Double-click the file and then click on **Run** if you are asked:

  ![winscp](images/winscp3.png)

1. On the next screen, fill in the IP address of the Pi, and the username and password:

  ![winscp](images/winscp4.png)

1. A warning will pop up, asking whether you trust the computer or not. Click on **Yes**:

  ![winscp](images/winscp5.png)

1. The next screen will allow you to transfer files between the machines by dragging and dropping from one pane to another:

  ![winscp](images/winscp6.png)

## Backing up by accessing the SD card on Linux

If you're using a Linux machine, then you can copy the files directly from the SD card.

1. Shut down the Raspberry Pi, remove the micro SD card, and place it into an SD card adapter. Then insert this into your machine.

1. The screenshot below shows the SD card mounted on a machine running Ubuntu:

  ![SD](images/SD1.png)

1. Your files will be in `home/pi`, so double-click on the `home` directory and copy the entire `pi` directory to your local machine:

  ![SD](images/SD2.png)


## What next?

- Return to the [Raspberry Pi Software Guide](quickstart.md)
- Learn how to [update your SD card](update-sd-card.md)
- Install more [applications](install-apps.md)
- Connect to [WiFi](wifi.md)
