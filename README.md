AdhocToUSB Guide for Windows 7/8/10
====================================

# Requirements

- Any PSP model *except* the Street (E1000)
- Memory Stick PRO Duo or compatible adapter
- 6.60/6.61 ME (Recommended) or 6.60/6.61 PRO-C2 CFW
- USB A to Mini B Cable
- Xlink Kai [[here](https://www.teamxlink.co.uk/)]
- Zadig [[here](https://https://zadig.akeo.ie/)]
- Administrator privileges

# Part A: Setting Up the PC

## Step 1 - Microsoft Loopback Adapter
First install the Loopback Adapter used by adhoctousb's Bridge program.

  1. Press the Windows button and R at the same time or search for `run` in the start menu.
  
  2. The Run window will open, type `hdwwiz`. 
 
  3. Click next and then select `Install the hardware that I manually select from a list (Advanced)`.

  4. This will bring up a list of hardware types, scroll and find `Network Adapters` and click Next.

  5. On the left will be a list of Manufacturers, click on Microsoft then on the right select the `Microsoft KM-TEST Loopback Adapter`. Click next again and it should install.

## Step 2 - Configuring Xlink Kai

Now open your start menu and search for `Configure Kai`.
  
In the configuration tool look for Network Adapter change this to `MS NDIS 6.0 LoopBack Driver`. *(If you don't see this you may have to reinstall WinPcap from their [website](https://www.winpcap.org/install/default.htm).)*  

Click Save and restart Kai to be sure that it has applied.

To test this check the Metrics tabs at the top of the Web UI, and look for Ethernet Adapter it should say `MS NDIS 6.0 LoopBack Driver`, also while in this menu make sure Reachable says Yes. *(You may have to look up a tutorial for port forwarding Kai or Enabling UPNP in your router)*

# Part B: Setting Up the PSP

## Step 3 - Installing the AdhocToUSB Plugin

Connect your PSP to the computer in USB Mode.

In the included AdhocToUSB folder transfer `AdhocToUSB.prx` to the `seplugins` folder, if it doesnt exist create it at the root of your PSP's Memory Stick. *(not in any folders)*  

Afterwards open `GAME.txt` in the `seplugins` folder. *(if it doesnt exist create it.)*  

Now add on a new line:  

`ms0:/seplugins/AdhocToUSB.prx 1` (for PSP 1000/2000/3000)  
or  
`ef0:/seplugins/AdhocToUSB.prx 1` (for PSP GO N1000)

*Note: Only one plugin can use the USB port at a time, do not try to use this and for example RemoteJoyLite at the same time.*

# Part C: Setting Up the Drivers

## Step 4 - Installing the PSP Type B Drivers

Connect the PSP to your computer via USB, start a game with AdhocToUSB enabled.

Back on PC, open Zadig, if you have your PSP in game you should see `PSP Type B`, if not go to Options on the top bar and select `List All Devices`, on the right click the small arrows until you see `libusb-win32`, then Install Driver, it should install successfully.

# Part D: Profit

To go online from now

1. Open Xlink Kai then go to the associated game lobby for your game

2. On PSP activate Adhoc multiplayer while connected to your PC 

3. Start the Bridge.exe in the AdhocToUSB folder, *(you may want to make a shortcut to this file)* 

4. Select the Loopback Adapter *(if you get any timeout error notice thats simply lag and can be ignored.)*

Have fun using your PSP Online.
