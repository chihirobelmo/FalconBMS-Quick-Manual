<font size="48">FalconBMS Quick Start Guide</font>

|Version|Date|
|-|-|
|v0.01|2019.07.20|

# What is FalconBMS

Falcon BMS (hereinafter BMS) is software developed based on source code leaked from MicroProse's flight simulator "Falcon 4.0" released in 1998.

Falcon 4.0 recreates the flight characteristics and avionics of the Lockheed Martin F-16C block 50/52, and has been widely adopted by combat sim users by the implemented dynamic campaign.

After the closure of the development studio due to the disappearance of the MicroProse brand, the volunteers of the community continued updating based on the leaked source code, and Falcon 4.0 has evolved into various versions and developed over approximately 20 years.

BenchmarkSims is the only survivor of such a volunteer development team, and develops and releases FalconBMS under the license of BillionSoft, the current owner of Falcon 4.0.

<div style="page-break-before:always"></div>

# What is Dynamic Campaign

[WIP]

<div style="page-break-before:always"></div>

# What BMS has been updated

## Flight Model

- Performance: see HFFM manual
95% performance accuracy on the whole flight envelope:
- Turn Rate
- Turn Radius
- Energy Management
- Accel and Decel Performances
- Climb performances
- Drag indexes complex modeling
- Handling
- Real FLCS build in, including AutoPilot and TFR Tie In.
- Real stick responses curves built in
- Cruise gains, Landing Gains, Stand By gains, MPO
- Accurate aerodynamic departures: Roll , Pitch and yaw departures
- Aerodynamic modeling
- Complex aerodynamic coupling modeling: 30 couplings modeled
- Independent LEF and TEF model
- Ram drag model
- Buffeting model
- Flutter model
- Convective and mechanical turbulences
- Background Noise turbulences
- Jet Wash
- Wind Gusts
- Wind Aloft
- Mechanical Components
- Real time Gravity center management, (lateral and longitudinal), including fuel and weapons
- Real Time inertia matrix management, including fuel and weapons
- Fuel System: 7 tanks modeled with accurate pump system and transfer rates
- External tanks with 3 compartments model
- Trap fuel model
- Starve out model
- Complex gear modeling:
  - Stiffness
  - amortization
  - pre stressing
  - tire elasticity
- Brake temperature modeling
- Wing Flex: interacting with fuel, weapons and accelerations
- Canon recoil model
- FLCS Bit

## Engine Modeling

- DEEC and SEC modelwith accurate RPM / NOZZLE / FTIT andspooling times
- Oil pressure / quantity model
- EPU model
- Hydraulic pressure model
- JFS fuel and heating model
- Accurate Fuel Flows in the whole flight envelope
- Realistic Engine faults: Hung starts / Hot starts / oilpressure default
- Realistic Air Start model

## Damage Modeling

- Airframe damage model impacting performances andhandling
  - Engine inlet
  - Engine outlet
  - L/R wings
  - L/R elevators
  - Rudder / Tail
- Oil Leaks
- Fuel Leaks
- Hydraulics leaks
- FLCS faults

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

Falcon BMS Alternative Launcher is a replacement for stock BMS launcher including key/axis mapping feature. It can configure and save BMS SETUP per Joysticks. When you launch BMS through this app, it auto-generates proper setup files and overwrites them for current device order before BMS find them changed and initialize your setup. You don't have to worry about SETUP mixing up DX order nor resets axis setups even if device sort or numbers have been changed.

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

## Pinky Shift





