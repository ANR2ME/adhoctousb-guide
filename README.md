AdhocToUSB Guide for Windows 10 by plus#3034
============================================

# Requirements

- PSP (any model should work)
- Memory Stick PRO Duo
- USB A to Mini USB Cable
- Xlink Kai [[here](http://www.teamxlink.co.uk/)]
- 6.60/6.61 PRO-C2 (Recommended) or 6.60/6.61 ME CFW
- Administrator privileges

# Part A: Setting Up the PC

## Step 1 - Microsoft Loopback Adapter
First we'll install the Loopback Adapter used by adhoctousb's Bridge program.

  1. Press the Windows button and R at the same time or search for `run` in the start menu in this menu type `hdwwiz`. 
 
  2. Click next and then select `Install the hardware that I manually select from a list (Advanced)`.

  3. This will bring up a list of Hardware types, scroll and find `Network Adapters`. Next.

  4. On the left will be a list of Manufacturers, click on Microsoft then on the right select the `Microsoft KM-TEST Loopback Adapter`. Click next again and it should install.

## Step 2 - Configuring Xlink Kai

Now open your start menu and search for `Configure Kai`.
  
In the configuration tool look for Network Adapter change this to `MS NDIS 6.0 LoopBack Driver`. *(If you don't see this you may have to reinstall WinPcap from their [website](https://www.winpcap.org/install/default.htm).)*  

Just click Save and restart Kai to be sure that its applied.

To test this check the Metrics tabs at the top of the Web UI, and look for Ethernet Adapter it should say `MS NDIS 6.0 LoopBack Driver` while in this menu make sure Reachable says Yes. *(You may have to look up a tutorial for port forwarding Kai or Enabling UPNP in your router)*

# Part B: Setting Up the PSP

## Step 3 - Installing the AdhocToUSB Plugin

Connect your PSP to the computer. *(If you have CFW im assuming you know how to put it into USB Mode.)*

In the included software bundle open the AdhocToUSB folder and transfer `AdhocToUSB.prx` to the `seplugins` folder, if it doesnt exist create it at the root of your PSP directory *(not in any subfolders)*  

Afterwards open `GAME.txt` in the `seplugins` folder, once again if it doesnt exist create it.  

Now type:  

`ms0:/seplugins/AdhocToUSB.prx 1` (for PSP 1000/2000/3000)  
or  
`ef0:/seplugins/AdhocToUSB.prx 1` (for PSP GO (E1000))

*Note: Only one plugin can use the USB port at a time, do not try to use this and for example RemoteJoyLite at the same time.*

# Part C: Setting Up the PC (Continued)

## Step 4 - Disabling Driver Signature Verification

[Use this guide](https://www.howtogeek.com/167723/how-to-disable-driver-signature-verification-on-64-bit-windows-8.1-so-that-you-can-install-unsigned-drivers/)

## Step 5 - Installing the PSP Type B Drivers

On your PSP connect it to your computer via USB and start a game with Adhoc multiplayer and activate it. *(when you see the wireless light come on you're good)*

Back on PC, open up the software package again and open the folders LibUSB/bin/, then run `inf-wizard.exe` as administrator, if you have your PSP in game you should see `PSP Type B`, click on that and then click next until it asks you to choose a location. Select the Type B folder provided in the software package, click save, then Install Now, it should install successfully.

At this point I highly advise that you open up the Admin PowerShell and type `bcdedit /set testsigning off` and re-enable Secure Boot if you had to disable it, the PSP drivers will still work.

# Part D: Profit

To go online anytime from now, Open Xlink Kai and go to the associated game lobby for the game, afterwards hop into the network section of the game while connected to your PC and then start the Bridge.exe in the AdhocToUSB folder, *(you may want to make a shortcut to this file)* and finally select the Loopback Adapter, if it shows some FFFFFFF error just restart it (not including the timeout errors,  thats just lag)

have fun using your PSP online.
