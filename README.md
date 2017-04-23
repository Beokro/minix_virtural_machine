# How to install minix on VirtualBox


**Table of Contents**

- [Prerequisites](#Prerequisites)
    - [Virtual Box](#Virtual-Box)
    - [Minix3 source](#Minix3-source)
- [Loading Image](#Loading-Image)
- [Installation][#Installation]

# Prerequisities

This section will talk about how to get the required application and source before you can start. If you happened to have the following applications installed, you can skip this section. 
## Virtual Box

First of all you need to install VirtualBox on your computer. This can be easily done by downloading the application from their websites or using package manager tool like homebrew. 

### Step by step instruction

1. Visit virtual box org [website][] and select `OS X hosts` to download the virtualBox installing application. <br><br>
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/1.png" width='600' height='337'/>  
<br><br>

2. Once the downloading is finsihed, you should have a dmg format file like the picture below. Double clicking this file to start the installation. Keep selecting continue until the installation is finished. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/4.png" width='400' height='300'/>
<br><br>

## Minix3 source

Minix 3 is a free and open-source operating system. Its source file can be download from this [link][]. In this instruction, we will use version 3.3.0 (stable release) Iso Image. Once the downloading is finished, you should have a file named minix_Rxxx.iso. (xxx is the verison number you download).

<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/7.png" width='400' height='200'/>
<br><br>

# Loading Image

1. Now we have all the matrials we need to start the insatllation. Let's go ahead and load the Minix image into the Virtual Box. Open the Virtual Box application. If you can not find it, press F4 to enter the application page and use the serach bar at top to locate Virtual Box. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/6.png" width='400' height='300'/> 
<br><br>

2. Click new button on the top left of the window to create a new virtual machine. You can use whatever name you want, in this case we will just name it minix 3. Choose the type to be `Other` and the version to be `Other/Unknown`. Click continue. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/10.png" width='400' height='300'/>    
<br><br> 

3. Virtual Box will keep asking you to select the hardware spec for your virtual machine. You can setup the hardware as you like but we recommend you not to change the default vaue too much. The following table can be used as a reference. Be aware that minimum memory that minix3 need is 64MB. <br>

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

5. Select the virtual machine you just created, click `Setting` which is a yellow gear icon on top left of the windows. In the setting page, go to `Storage` section and click little CD icon that follow `Empty`. On the Attributes subsection, click another CD icon and select `Choose Virtual Optical Disk File`. <br>
    
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/16.png" width='420' height='300'/>   
<br><br>

6. On the windows that poped up, find the minix3 ISO file you downloaded in previous ste and open it. Now you successfully load the minix image into the virtual machine you just created. <br><br>
    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/17.png" width='400' height='300'/>   
<br><br>


# Installation 

1. Now, It's time for us to start installation. After you loaded the image to virtual box, you will see this window again. And, this time we click start button to run our image file which you loaded at the previous step. <br>

    <img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/18.png" width='400' height='300'/>   
<br><br>

2. Virtual box will automatically loaded the image file and start the Regular Minix3 installation or you can type other number to have other options. For our instrucation, type 1 to install the regular Miix3. <br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/19.png" width='400' height='300'/> <br><br>


3. Once you see the "login" in the window, then type "root" at the login prompt, and hit enter. Then type "setup" and hit enter to start installation process.  <br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/20.png" width='400' height='300'/> <br>
	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/21.png" width='400' height='300'/> <br><br>

4. Then Minix3 will guide you in setting up MINIX on your machine. There are several notes which are important.<br>

	- Note1 : if the screen blanks, hit CTRL+F3	to select "software scrolling"<br>
	- Note2 : if things go wrong, then hit CTRL+C to abort and start over.<br>
	- Note3 : default answers, like [y], can simply be chosen by hitting enter.<br>
	- Note4 : if you see a colon (:) then you should hit ENTER to continue.<br>
	<br><br>

5. After setting up the installation, the virtual box start the installtion. we just wait the loading bar to the end.<br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/31.png" width='400' height='150'/> <br><br>

 
6. Wait until installation finished, you need to type "reboot" to exit the Minix 3.<br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/32.png" width='400' height='300'/><br><br>


# Unloading image 

1. Now we have done with installtion and we need to remove installtion media. Let's go back and reopen virtual box application. <br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/18.png" width='400' height='300'/>   
<br><br>

2. Select the minix3 virtual machine, click `Setting` which is a yellow gear icon on top left of the windows. In the setting page, go to `Storage` section and click little CD icon that follow `Empty`. On the Attributes subsection, click another CD icon and select `Remove Disk form Virtual Drive`.<br>

	<img src="https://github.com/Beokro/minix_virtural_machine/raw/master/screenshots/33.png" width='430' height='230'/>   

[website]: https://www.virtualbox.org/wiki/Downloads
[link]: http://wiki.minix3.org/doku.php?id=www:download:start

