<font size="48">FalconBMS Quick Start Guide</font>

|Version|Date|
|-|-|
|v0.02|2019.8.1|

# What is FalconBMS

Falcon BMS (hereinafter BMS) is software developed based on source code leaked from MicroProse's flight simulator "Falcon 4.0" released in 1998.

Falcon 4.0 recreates the flight characteristics and avionics of the Lockheed Martin F-16C block 50/52, and has been widely adopted by combat sim users by the implemented dynamic campaign.

After the closure of the development studio due to the disappearance of the MicroProse brand, the volunteers of the community continued updating based on the leaked source code, and Falcon 4.0 has evolved into various versions and developed over approximately 20 years.

BenchmarkSims is the only survivor of such a volunteer development team, and develops and releases FalconBMS under the license of BillionSoft, the current owner of Falcon 4.0.

<div style="page-break-before:always"></div>

# What is Dynamic Campaign

Falcon 4.0 is like a flight simulator that can operate a fighter as a part of a strategy simulation game.

In Dynamic Campaign, every country of every coalitions, all forces, ground, sea, air, fight against each other. Missions will be automatically generated and fragged by HeadQuater AI, and each AI pilot joins there flight. You can take a sheet for those generated mission, and fly with them, or fly with your human friend. Or you can plan your own mission. You can debate and plan a mission with your mate in MP too. Every mission will be unique as they are not scripted but a result of entire war simulation, and affects entire situation, thus future missions.

Keep in mind there is a logistics, don't get your ammunition storage bombed or you will be run out of missiles.

<div style="page-break-before:always"></div>

# What BMS has been updated

## Flight Model

BMS coded a completely new flight model which do a calculation outside of legacy Falcon4.0 code but import position updates.
> I think that trying to plug new lines in the existing code could have been a wrong choice, therefore I decided to start from a blank page and use a dedicated data file format. The idea at this stage was to develop a new FM code that can be completely autonomous from F4. Then the new code would be fed values coming from F4 (atmosphere, terrain, weapons, fuel, etc) and would export output values into the F4 code (world positions, speeds, angles, etc).

You can read articles about BMS FM at official website
[FLIGHT MODEL](https://www.benchmarksims.org/forum/content.php?45-documentation)

also check Mav-JP's description
[BMS : F16 FLIGHT MODELING](https://www.reddit.com/r/falconbms/comments/bptu8e/bms_f16_flight_modeling/)

## AI

### BVR

[WIP]

### SAM

[WIP]

## ATC

[WIP]

## IFF

[WIP]

- every IFF interrogation and reply might be intercepted by the enemy.
  > That can be by an enemy ground station - anything with a radar - or ELINT flights. It depends on the emitting aircraft altitude and ELINT item position. That will make the emitting aircraft spotted for a while. Be aware of this, whether on the transponder side (dont blast every mode all the time, especially in a NOE penetration), or the interrogator side (dont interrogate in SCAN every second if you want your teammates to stay discreet).
- there can be errors in the transmission, known as 'code garble'.
  > It happens especially at a distance or if multiple transponders are close together. That can result in a different code being perceived by the interrogator, a 'unknown' M4 reply, or no reply at all being seen. M4 is less prone to that. But it can be good practice to deactivate M1/M2/M3 when flying close together.

<div style="page-break-before:always"></div>

# How to Install BMS

## Do I need Falcon4.0?

Although BMS itself is not a MOD that overwrites Falcon 4.0, it is a stand-alone software that can be installed separately, but the user must own the original version of Falcon 4.0 since the code is a modification from Falcon 4.0.

Therefore, installing BMS requires installing Falcon 4.0 in advance.

BMS checks the installation of Falcon 4.0 at installation and application startup.

## Where can I get Falcon4.0?

You can get Falcon4.0 at

[Falcon Collection on GOG.com](https://www.gog.com/game/falcon_collection) or [Falcon4.0 on Steam](https://store.steampowered.com/app/429530/Falcon_40/)

or you can install CD version of Falcon4.0

The title Falcon 4.0: Allied Force, released by Lead Pursuit in 2005, also exists, but it can not be used to install BMS.

## Version Number

BMS will undergo major updates with a revision number of 0.01, such as 4.32 released in 2011, 4.33 released in 2015, and 4.34 released in 2019, with the next version expected to be 4.35.

Different versions of BMS are installed independently.

Also, minor update patches for each version will be released sequentially, and the same version of BMS will be overwritten and updated like "4.34 Update1" "4.34 Update2" "4.34 Update3".

Each upgraded version is also referred to as "4.34 U1" or "4.34.1".

## Download

To obtain FalconBMS, register as a user on the forum of BenchmarkSims official site, download torrent files from each relevant thread of Releases & Updates, and obtain BMS installers and update patches via torrent.

[BenchmarkSims](https://www.benchmarksims.org/forum/content.php)

Forum account will be cleared automatically if no first post can be confirmed for a week after registration.

## Install

After downloading of BMS installer via Torrent is complete, `"Falcon BMS 4.34 SETUP.zip"` will be saved in your specified folder.

If you extract this ZIP file, `"Falcon BMS 4.34 SETUP"` will be opened, and you will see `Setup.exe` and data folder in the middle.

Before launching `Setup.exe`, be sure to move this setup folder to a directory that you can remember other than the desktop and keep it there. You will need this folder for future updates and uninstalls.

## Update

Download `Falcon_BMS_4.34_U1_Incremental.exe`(Not yet released 2019.07.20), move it directly under the setup folder (in the same place as Setup.exe exists) and execute it.

You will be prompted to specify the setup folder when you run it, so select the correct folder.

When this is done, a BSF file of update data is generated in the `data` folder.

Since the incremental installer automatically executes `Setup.exe`, if you want to continue applying the U2 and U3 patches, please cancel and proceed in the same way.

Finally, execute `Setup.exe` to update BMS.

## Uninstall

When uninstalling BMS, please uninstall from `Setup.exe`.

If you uninstall BMS from the control panel without going through `Setup.exe`, the registry will not be cleared properly, and you will not be able to reinstall BMS until you manually delete the registry.

The registry will be at `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Benchmark Sims\Falcon BMS 4.34`

<div style="page-break-before:always"></div>

# How to Setup BMS

## Stock launcher or Alternative launcher

You can start BMS via stock launcher or you can install [Alternative Launcher](https://github.com/chihirobelmo/FalconBMS-Alternative-Launcher)

Falcon BMS Alternative Launcher is a replacement for stock BMS launcher including key/axis mapping feature. It can configure and save BMS SETUP per Joysticks. When you launch BMS through this app, it auto-generates proper setup files and overwrites them for current device order. You don't have to worry about SETUP mixing up DX order nor resets axis setups even if device sort or numbers have been changed.

However, this chapter will describe how to setup BMS with the stock launcher.

## Window or FullScreen

Right-click the shortcut before launching BMS, open `Properties` and Add `-window` launch option to the link destination.

example: `C:\Falcon BMS 4.34\Launcher.exe -window`

It is a success if the notation of `window` appears in the upper right of the launcher.
Remove the `Border` option on the `Main screen` from the `Cockpit Display Extraction` you can access from the launcher.
This will start BMS in borderless window mode.

When starting BMS full screen with WINDOWS 10, Right-click the shortcut and open `Properties` then Open the Compatibility tab and `disable full screen optimization`. There is a bug that the resolution of 3D rendering is not reflected correctly.

## SETUP page in BMS

Start BMS and you will see a main menu. Various settings can be done from `SETUP` on the menu screen.

The `SIMULATION` tab that appears first on the SETUP page allows you to set various simulation settings (such as the presence or absence of labels and the enabling / disabling of blackouts).

To change the resolution setting, **select the `GRAPHICS` tab and adjust the resolution to the monitor resolution.**

**By default, the lowest resolution is set.**

The antialiasing effect is also selected from `MULTISAMPLING` as well.

Joystick settings are done from the `CONTROLLERS` tab.

After changing the setting, press `APPLY` and then `OK`.

<div style="page-break-before:always"></div>

# SETUP Joysticks

## What to assign?

In BMS, F-16 can be operated by clicking on the switches and dials in the cockpit with the mouse cursor.

However, various HOTAS (Hands On Throttle and Stick) switches on the throttle and stick can only be operated via a device such as a joystick or keyboard.

Therefore, you need to make assignments so that the buttons on your joystick corresponds to the various switches on the F-16's control stick / throttle.

## How to assign?

Key binding for various switches and axes is done from the `CONTROLLERS` menu of `Setup` page.

First select the `primary device` from the `CONTROLLER pull-down menu`.

**The primary device is a control stick that inputs pitch and roll axes.**

Once set, do the key assignment **without changing the selection of the primary device.**

Find the callback you want to assign from the `MAPPING` column of the `CURRENT KEYFILE` table, and click the `KEY` column in the same row. The character turns to blue. Then press the joystick switch or keyboard key you want to assign to the selected callback in this state.

To assign the minimum required callback for F-16 operation, search following sections from the list of KEY MAPPING

`2.19 THROTTLE QUADRANT SYSTEM`  
`5.11 FLIGHT STICK`

Find out the section and assign each HOTAS switch to your joystick button.

once you done the key assignment, click `ADVANCED` tab and assign axis from the new window.

Falcon BMS builds in the input curves of the actual F-16 FLCS.

Therefore, Benchmark sims recommends that the pitch / roll axis of the joystick set to OFF the dead zone and curves.

## I can't assign POV hat of the throttle

BMS only recognize POV hats of the primary device, sorry.

## Recomended Joysticks

- **HOTAS Warthog (+ FSSB R3)** or **HOTAS Cougar**
- **TrackIR**
- Any Rudder Pedals

<div style="page-break-before:always"></div>

## F-16 HOTAS

![img/stick.jpg](img/stick.jpg)

![img/throttle.jpg](img/throttle.jpg)

![img/stickHotas.png](img/stickHotas1.png)

![img/stickHotas.png](img/stickHotas2.png)

![img/throttleHotas.png](img/throttleHotas1.png)

![img/throttleHotas.png](img/throttleHotas2.png)

<div style="page-break-before:always"></div>

## Why did my joystick setup gone/mixed up?

### DX setup mixed up

The ID number of the connected device is saved in `DeviceSorting.txt` in the `FalconBMS4.34\User\Config` directory.

When BMS recognizes a new device, the device GUID and name are written in the file.

For example
```
{B351044F-0000-0000-0000-504944564944} "F16 MFD 1"
{B352044F-0000-0000-0000-504944564944} "F16 MFD 2"
{0400044F-0000-0000-0000-504944564944} "Thrustmaster HOTAS Cougar"
```

In the example above, DX button 0-31 is assigned to F16 MFD 1, 32-63 for F16 MFD 2, and 64-95 for Thrustmaster HOTAS Cougar.

If you forget to connect F16 MFD 1 and start BMS, F16 MFD 2 will be assigned the 0-31 DX button, and the order of the DX buttons on Thrustmaster HOTAS Cougar will be 32-63.
But you were assigning HOTAS callbacks to DX 64-95, therefore your joystick does not work as HOTAS anymore.

In that case, connect F16 MFD 1 again and restart BMS.

### Axis gone

The axis settings of BMS will automatically disappear unless you have the same DX device environment(same devices connected, no more nor less) as when you setup it last time.

If you want to add a new DX device, you need to reconfigure axis, also remove them before start setup if there are any devices you don't use to play BMS but you are just connecting.

Even if you accidentally start Falcon in a different device environment, just quit Falcon without saving the settings, restore the device environment as same as you launched BMS last time, then reboot BMS will restore the previous settings.

## Modifier

The key assigned to **"STICK: PINKY SWITCH (DX SHIFT)"** (the callback name in the configuration file is SimHotasPinkyShift) will function as a normal pinkey when pressed short, and as a DX button shift key (same to "modifier" in DCS) when pressed hold.

While shifting the DX button, the DX button of each joystick switch will be recognized as the original DX number + 256th switch.

"STICK: PINKY SWITCH" (callback name in the configuration file is SimPinkySwitch) functions only as a normal pin key switch and does not have the shift function of the DX button.

If you change the value of `g_nHotasPinkyShiftMagnitude` from `falcon bms.cfg` in the `User\ Config` directory, the value of the DX button shifting number will be reflected (the default is 256).

You have to Edit `.key` file in `User/Config` folder manually to assign shifted DX key.

For example:

```
SimTriggerFirstDetent 0 -1 -2 0 0x0 0
SimPickle 256 -1 -2 0 0x0 0
SimHotasPinkyShift 2 -1 -2 0 0x0 0
```

In the example above, the first stage of the trigger is assigned to DX number 0, and the pickle is assigned to DX number 256.

While pressing the pinkey assigned to DX No. 2, pulling the trigger to the first step works the same as pressing the pickle switch.

**If you execute the DX shift, if you release the PINKEY switch after pressing the shift switch and then release the finger, all switches will remain shifted.**

To avoid this, you need to assign a second SimHotasPinkyShift callback to the DX shift destination as well.

For example:

```
SimTriggerFirstDetent 0 -1 -2 0 0x0 0
SimPickle 256 -1 -2 0 0x0 0
SimHotasPinkyShift 2 -1 -2 0 0x0 0
SimHotasPinkyShift 258 -1 -2 0 0x0 0
```

This will avoid shifted remain glitch. It's useful but not written in the official manual.

## I don't have a rudder pedals

You can enable Enable `Roll-linked NWS` option on the `VIEW CONTROL` tab of the `ADVANCED` setting screen. Enabling the option allows you to steer the wheel on the roll axis while turning NWS on the ground.

If any axis is assigned to the rudder, the option will be invalidated even if it is checked.

# Start Training Missions

BMS has training missions to learn the operation of F-16.
How to fly those missions is described in the **"Docs/BMS-Training.pdf"** in the BMS install directory.

To start a training mission, select `TACTICAL ENGAGEMENT` from the menu and select the `TRAINING` tab.

After selecting the mission you want to fly from the list, confirm the mission contents and `COMMIT`.

After entering the mission planning screen. Select the flight you want to fly from the `MISSIONS` list and then select which aircraft in the flight you want to board. Click the airplane icon to select a boarding aircraft. If your name appears below the icon, you are registered as a boarding aircraft.

The top icon is the captain and the next icon is the wingman.

# Start Campaign

## Select Campaign and Fighter Squardron

Start the campaign from the menu `CAMPAIGN`.

- select `NEW` tab if you want to play a new campaign
- `SAVED` if you want to start from save data
- `ONLINE` to participate in multiplayer

If you select `NEW`, then select the campaign to play from now on.

Each theater has up to six campaigns, and the start situation and victory conditions differ depending on the campaign.

After selecting a campaign, select the deployed base from the map. then, select a unit from the units deployed to the selected base. The selected unit's information will be displayed at the bottom left of the screen.

## Start A Mission

Once you have launched the campaign, select the mission you would like to join from `FRAG OREDER`.

Once you have selected a mission, board one of the aircraft in the flight. Click the airplane icon to select a boarding aircraft. If your name appears below the icon, you are registered as a boarding aircraft. The top icon is the captain and the next icon is the wing.

On the map screen, you can check the current time with the clock at the top right of the screen, and you can speed up the time forward up to 64x.

After registering the boarding to the aircraft, check the `BRIEFING`, change the arming with `LOADOUT` if necessary, adjust and confirm the mission with the map screen, and then start the mission with `TAKEOFF`.

After choosing `TAKEOFF` before the flight's takeoff time, you can choose how to start the mission.

- If you choose `Ramp`, the mission will start from the condition before the engine start 20 minutes before the takeoff time.  
- If you select `Taxiway`, the mission will start from the taxiway 4 minutes before the takeoff time.  
- If you choose `Runway`, the mission will start from the runway one minute before the start of takeoff.

If `TAKEOFF` is selected from the flight takeoff time before the aircraft reaches the IP on the map, the mission would start from the air.

# Plan A Mission

The flight plan course is represented by white circles(Steerpoint), squares(IP), triangles(EOR) and the lines connecting them.

Each steer point can be repositioned by drag and drop, and the arrival time of each point, flight altitude, passing speed, action to be performed, etc. can be set from the PKG window displayed by double clicking a steerpoint circle (or click the flight plan icon below).

When the flight plan is represented by a red line and a marker, it means that the setting of arrival time (TOS) or passing speed (CAS) of the point is unreasonable. In that case, open the PKG window and adjust again.

You can lock the TOS, CAS, or both by clicking on the lock symbol. Changing the locked TOS or CAS will automatically adjust the unlocked TOS / CAS of all steer points. Unlocking the TOS of all steer points, locking and adjusting the CAS makes it easy to modify the flight plan.

# Data cartridge settings

You can access the data cartridge settings from the DTC icon on the map screen.

The data cartridge is magnetic tape recording mission information, and it is inserted into a designated slot in the F-16 cockpit and data is read before flight.

The data cartridge contains data sets for radio frequency presets, initial settings for the MFD screen in each flight mode, preset settings for the self-defense program (chaff / flare emission pattern), target coordinates, steer point information, IFF.

Befoe starting a mission, open the Data Cartridge window from the DTC icon, select the COMMS tab, select UHF No. 15, press SET TOWER to register the tower frequency of the base you are belonging to. When DEFAULT is checked, the initial setting of the radio after avionics activation will be the preset number selected by DTC.

# Set steerpoint to a target cordinations

It is important to check the location of the target and its surroundings before the start of the mission. Open the right-click menu on any unit or point on the MAP, select Recon, and check the surroundings in the 3D screen.

When the Recon screen opens, select the target you want to attack from TARGET LIST, set the desired steer point number (ie: target steerpoint represented by the triangle) from DESIGNATE AS TGT STPT # in the RECON window and press ACCEPT to overwrite the steer point coordinates with the target coordinates.

After performing ACCEPT on the RECON screen, select the Data Cartridge window, confirm that the target coordinates have been overwritten to the specified steerpoint number from the TARGET tab, and then save. If this is not done, the information will not be registered in DTC properly.

# Preplanned Threat Steerpoint

Before the flight, confirm the presence of threats around the flight plan course (such as enemy air defence battalion units), and register the preplanned threat steer points to display the location and range of threats on the MFD HSD screen.

Open the right-click menu on the map to display Battalions from Ground Units and check Air Defense. You will now see your enemy's air defense battalion on the map. Right-click on the symbol representing a air defense battalion unit on the map and press Status to see the unit's formation.

Once you have identified the threat type, right-click on the map and select Set Preplanned Threat Stpt from the menu to add a green threat marker to the map. Drag and drop this threat marker onto the air defense sbatallion unit, and left-click to select the threat type from the setting window that appears, then press ACCEPT. This will allow threat markers to display the effective range as a circle. To delete a threat marker, open the right-click menu on the marker and delete it.

Please note that changes will not be reflected unless you open the Data Cartridge window and press SAVE after adding or deleting threat markers.

# Create a mission yourself

## Disable automatic generation of missions

If you create missions yourself, you may not be able to create new missions if a certain number of aircrafts are assigned by auto-generated missions. If you turn off automatic generation of missions in advance, it will be easier to create missions.

To disable the automatic generation of missions, click the Maximize icon on the map screen, select the Squardron Records icon, and uncheck Set by HQ from the FIGHTER SQUARDRON window.

## Create a Package

When creating a package, first determine the unit or airspace you want to target.

This time, I will create a DEAD mission package that will destroy enemy air defense battalion units as an example. If you want to create a mission to patrol a particular airspace, do the same for the airspace.

Switch to the unit display in Battalions units from the right click menu on the map this time to check the Air Defense unit.

Right-click the displayed unit and confirm the unit name from Status. Right-click the unit again and select Add Package.

When the ADD PACKAGE window is displayed, lock the takeoff time (TAKEOFF) of the package or lock the estimated time of arrival at the target (TIME ON TARGET) and press NEW.

When the ADD FLIGHT window appears, select the aircraft owned by your unit from AIRCRAFT. After selecting your base in AIR BASE, select your unit from SQUARDRON. Select the target unit's unit name from TARGET, set the mission content to DEAD from ROLE, and determine the number of flights from SIZE. Press OK to create the flight in the package.

To add a new flight to the package, set the takeoff time or arrival time again and press NEW. This time, we will add an ESCORT flight. After setting ROLE to ESCORT, set TARGET to the callsign of the flight to be escorted.

Although Escort flights are organized from the same base and the same stage in the example in the figure, flights may be created in the same way from other units on other bases.

If you confirm the created package, press OK.

If you want to add a new flight to the package created once, select the created flight from the FRAG ORDER list, double-click the flight plan and identify the package number from the name of the PKG window that appears, and click the ATO icon to show it AIR TASKING Activate Show All Packages from the ORDER window, search for the package number with the same name, select Show Flights from the package right-click menu, and the Add Package window will be displayed again.

# Multiplayer

In BMS, you need to set port forwarding and firewall exceptions and bandwidth correctly, and if the client does not know some rules, it will make the server unstable.

BMS also an in-game voice chat called Internal Voice Communications (IVC), which enables voice chat in conjunction with the in-game cockpit radio settings. The use of the IVC makes it possible to reproduce more realistic flight operations.

## Port forwarding and firewall exception settings

The following ranges of ports need to be opened before hosting the BMS server:

- The BMS server host: UDP 2934-2935.
- The IVC server host: UDP 9987-9989.

You can also set up a DMZ (take on your own security issues).

# Host a server / connect as a client

Check the upload speed on [SPEEDTEST.NET](https://www.speedtest.net/) when hosting/connecting to a server. Make a note of the upload and download speeds in kbps. This value will be used later for band setting.

Before launching BMS, launch the IVC Server from the launcher if using IVC. The host of the IVC server can be same PC to the BMS host, ot may be on a separate PC from the BMS host.

After starting BMS, select COMMS from the top menu, and set the opened COMMS window as follows.

If you are hosting a server for the first time, you may want to create a new server list with NEW and then start the configuration.

- ServerName:  
Set any name you want.

- Connect to IP Address:  
0.0.0.0 when setting up a server as a host, or set the host IP address when connecting to a server as a client.

- Upload Bandwidth:  
Enter 90% of the upload speed value checked by SPEEDTEST.NET in kbps. For example, for an upload speed of 50 MB, enter 45000.

- Download Bandwidth:  
  Enter 90% of the download speed found in SPEEDTEST.NET in kbps. For example, for an upload speed of 50 MB, enter 45000.

If you want to host/join an IVC server, make the following settings.

- IVC Enabled: Check

- Dedicated IVC Server: 127.0.0.1 when you host an IVC server  
(If another machine hosts IVC server, enter the IPv4 address of the IVC host)

- Dedicated IVC Password:
Enter the password, leave blank if you do not want to set the path.

If this is your first setup, you may want to save these settings by selecting SAVE before opening the server. Also, when connecting to the server as a client for the first time, it is better to save the server information with the SAVE button.

The saved server list is written to User/Config/phonebkn.ini in text file format.

Select CONNECT when you are done.

When the server host or client connection is successful, COMMS on the menu screen blinks.

Clicking on the COMMS menu will display a list of connected clients.

To start a session, the host has to load or start a new game mode: Dogfight, Tactical Engagement, or Campaign.

After selecting TE, new campaign or saved data to load, click COMMIT ONLINE and the RULES OF ENGAGEMENT window will be displayed.


The server host can now define room rules when starting a session.

- GAME NAME:  
Set the session name displayed on the ONLINE tab of each mode.

- PASSWORD:  
You can add a password to the session. or Leave blank.

- MAX # PLAYERS:  
Set the maximum number of people who can connect at the same time.

If you are a client and want to join the session, select the game mode in which the host started: Dogfight, Tactical Engagement, or Campaign. After selecting the game mode, find the session started by the host from the ONLINE tab and click it.

If you select COMMIT ONLINE, the RULES OF ENGAGEMENT window will be displayed.

Clients must now configure their settings to the host's defined room rules before joining the session. The list on the left are the server rules, and the right is your current settings. Let's COMPLY if the setting conforms to the server specification.
