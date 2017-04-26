# How to install Minix on VirtualBox

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-generate-toc again -->
**Table of Contents**

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
    - [VirtualBox](#virtualbox)
    - [Minix3 source](#minix3-source)
- [Loading Image](#loading-image)
- [Installation](#installation)
- [Post Installation](#post-installation)

<!-- markdown-toc end -->

# Introduction
Minix is a free and open-source operating system based on a microkernel architecture. It was first release in 1987 and made available to university in course and research. Although Minix is not as compilcated as most modern commercial operating systems, it is still hard for beginner to install and configure it properly, due to the lack of graphical user interface. In this article, we will show you how to install Minix3(newest version of Minix) on VirtualBox. The host operating system we used is macOS but the procedure will be similar on Linux and Windows.

# Prerequisites

This section will talk about how to get the required application and source code before you can proceed. If you happened to have the VirtualBox installed and Minix3 downloaded, you can skip this section. 

## VirtualBox 

1. First of all you need to install VirtualBox on your computer. This can be easily done by downloading the application from their websites or using a package manager tool like homebrew. In here we will show you the first way. Visit [VirtualBox website][] and select `OS X hosts` to download the VirtualBox installing application. <br><br>
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/1.png" width='600' height='337'/>  
<br><br>

2. Once the downloading is finished, you should have a dmg format file named VirtualBox-xxxx-OSX.dmg (xxx is version number). Double clicking this file to start the installation. You can change the file destination if you want to, otherwise keep selecting continue until the installation is finished. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/4.png" width='400' height='300'/>
<br><br>

## Minix3 source

Minix3's source file can be downloaded from [Minix3 website][]. In this instruction, we will use version 3.3.0 (stable release) ISO Image. Once the downloading is finished, you should have a file named minix_Rxxx.iso. (xxx is version number).

<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/7.png" width='400' height='200'/>
<br><br>

# Loading Image

1. Now you have all the martials you need. Let's go ahead and load the Minix3 image into the VirtualBox. Open the VirtualBox application. If you can not find it, press F4 to enter the application page. Use the search bar at top to locate VirtualBox.  <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/6.png" width='400' height='300'/> 
<br><br>

2. Click new button on the top left of the window to create a new virtual machine. You can use whatever name you want, in this case we will just name it Minix3. Choose the type to be `Other` and the version to be `Other/Unknown`. Click continue. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/10.png" width='400' height='300'/>    
<br><br> 

3. Virtual Box will keep asking you to select the hardware spec for your virtual machine. You can set up the hardware as you like, but we recommend you not to change the default value too much. The following table can be used as a reference. Be aware that the minimum memory that Minix3 need is 64MB.  <br>

    Hardware | Value
    ------------ | -------------
    Memory size | 128 MB
    Hard disk | Create a virtual hard disk now
    Hard disk file type | VHD (Virtual Hard Disk)
    Storage on physical hard disk | Dynamically allocated
<br><br>    

4. Now you should be able to see your new virtual machine on the left column of the Virtual Box. <br><br>
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/15.png" width='400' height='300'/>   
<br><br>    

5. Select the virtual machine you just created, click `Setting` which is a yellow gear icon on top left of the windows. In the setting page, go to `Storage` section and click little CD icon that follows `Empty`. On the Attributes subsection, click another CD icon and select `Choose Virtual Optical Disk File`. <br>
    
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/16.png" width='420' height='300'/>   
<br><br>

6. On the windows that popped up, find the Minix3 ISO file you downloaded in the previous section and open it. Now you have successfully loaded the Minix3 image into the virtual machine you just created.  <br><br>
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/17.png" width='400' height='300'/>   
<br><br>


# Installation 

1. Go back to the Virtual Box main windows, select the virtual machine you created. You should be able to find the start button on the top left of the windows, click it to start the Minix3. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/18.png" width='400' height='300'/>   
<br><br>

2. VirtualBox will automatically load the image file from disk and give you couple options regarding booting procedure. Let's press `Enter` to start system regularly. <br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/19.png" width='400' height='300'/> <br><br>


3. Minix3 will ask you for the login name. Since you haven't created an account yet, let's use root to enter the root mode. Once you login into the system, type setup to configure the Minix system setup.   <br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/21.png" width='400' height='300'/> <br><br>

4. Minix3 will prompt you more questions about hardware specs and system options you want to use. You can choose the value that best suits your need. However if you are not sure what you want, press `Enter` to choose the default value. There are few tips we want to give in case you run into any unexpected situations.  <br>
	- If screen blanks, press CTRL+F3 to enable "software scrolling"<br>
	- If things go wrong, press CTRL+C to abort and start over.<br>
	<br><br>

5. The installation is going to take a while, you can monitor the progress by looking at the number of remaining files. Once the installation is finished, type shutdown to exit the system.<br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/32.png" width='400' height='300'/><br><br>


6. The last step of installation is removing the installation media. This way Minix3 won't load image on startup every time.  You can do that by following the same procedure as loading the image but select `Remove Disk from Virtual Drive` instead of `Choose Virtual Optical Disk File` <br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/33.png" width='430' height='230'/>   

# Post Installation

Now you have your Minix3 installed on VirtualBox. Beofre you proceed any further, we recommanded you to setup the password for your root account. Start your virtual machine and enter following command once you login into root account.
```sh
# passwd
```
Type the new password in next line. Be aware that no characters or `*` will appear as you type but it is being entered. Reboot you Minix3 and now you will be asked for a password in login. 

[VirtualBox website]: https://www.virtualbox.org/wiki/Downloads
[Minix3 website]: http://wiki.minix3.org/doku.php?id=www:download:start

