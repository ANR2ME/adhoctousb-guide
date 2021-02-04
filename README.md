AdhocToUSB Guide for Windows 7/8/10
====================================

# Requirements

- Any PSP model *except* the Street (E1000)
- Memory Stick PRO Duo or compatible adapter
- 6.60/6.61 ME (Recommended) or 6.60/6.61 PRO-C2 CFW
- USB A to Mini B Cable
- Xlink Kai [[here](https://www.teamxlink.co.uk/)]
- Zadig [[here](https://zadig.akeo.ie/)]
- CWUSB [[here](https://github.com/codedwrench/CWUSB/releases)]
- Administrator privileges

# Part A: Setting Up the PC

## Step 1 - Configuring Xlink Kai
Check the following installation guides on how to install XLink Kai: [[here](https://www.teamxlink.co.uk/wiki/Main_Page)], pick the one that corresponds to your operating system.

# Part B: Setting Up the PSP

## Step 2 - Installing the AdhocToUSB Plugin

Connect your PSP to the computer in USB Mode.

In the included AdhocToUSB folder transfer `AdhocToUSB.prx` to the `seplugins` folder, if it doesnt exist create it at the root of your PSP's Memory Stick. *(not in any folders)*  

Afterwards open `GAME.txt` in the `seplugins` folder. *(if it doesnt exist create it.)*  

Now add on a new line:  

`ms0:/seplugins/AdhocToUSB.prx 1` (for PSP 1000/2000/3000)  
or  
`ef0:/seplugins/AdhocToUSB.prx 1` (for PSP GO)

*Note: Only one plugin can use the USB port at a time, do not try to use this and for example RemoteJoyLite at the same time.*

# Part C: Setting Up the Drivers

## Step 3 - Installing the PSP Type B Drivers

Connect the PSP to your computer via USB, start a game with AdhocToUSB enabled.

Back on PC, open Zadig, if you have your PSP in game you should see `PSP Type B`, if not go to Options on the top bar and select `List All Devices`, on the right click the small arrows until you see `libusbK`, then Install Driver, it should install successfully.

## Step 4 - Downloading the Bridge application

Download the latest CWUSB application from [[here](https://github.com/codedwrench/CWUSB/releases)].
Unpack the zip and start cwusb.exe, you may have to unblock the application by right clicking on it, going to properties and hitting "Unblock".

# Part D: Profit

To go online from now

1. Open Xlink Kai then go to the associated game lobby for your game

2. On PSP activate Adhoc multiplayer while connected to your PC 

3. Start the cwusb.exe you downloaded before *(you may want to make a shortcut to this file)* 

Have fun using your PSP Online.


## Troubleshooting
- I'm getting an error about: MSVCP140.dll, VCRUNTIME140.dll or VCRUNTIME140_1.dll
   - Install [Microsoft Visual C++ Redistributable for Visual Studio 2015, 2017 and 2019](https://aka.ms/vs/16/release/vc_redist.x64.exe)
   
- I'm getting an error about: "Operation not supported or unimplemented on this platform"
   - The libUSBK driver is not installed correctly, make sure the plugin is enabled and a game is running when installing the driver using Zadig
   
- Receivebuffer got to over 50! or Sendbuffer got to over 50! ?
   - This is a normal warning, there could be some added latency while playing
 
- Could set configuration: Entity not found
   - This usually happens when you installed the wrong driver, reinstall the driver
