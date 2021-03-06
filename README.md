<h1 align="center">
  <br>
    <img src="https://cdn.rawgit.com/redline-forensics/t-rig/0fc987f4/img/logo.svg" alt="Magic Shade" width="200">
  <br>
    [t] Rig
  <br>
</h1>

<h4 align="center">Simple bus and trailer rigging scripts for Maya.</h4>
<br>

![screenshot](https://raw.githubusercontent.com/redline-forensics/t-rig/master/img/usage.gif)

## Key Features

* Animate vehicle motion using 2 paths to simulate large turning radii
* All motion controlled by a single master locator

## Installation

1. Clone or download repository
   * Clone: ```git clone https://github.com/redline-forensics/magic-shade.git```
   * Download: <a href="https://github.com/redline-forensics/t-rig/archive/master.zip">master.zip</a> and unzip
2. In ```\Documents\maya\scripts``` create a new folder ```t-rig```
3. Place repository contents (i.e. ```c-rig.py```, ```t-rig.py```, etc.) inside newly-created ```t-rig``` folder
4. In Maya, open the Script Editor (Windows - General Editors - Script Editor)
5. Open ```\Documents\maya\scripts\c-rig.py``` in the Script Editor (File - Open Script...)
6. Save the script to the shelf (File - Save Script to Shelf...)
7. Name the script (e.g. "C-Rig")
8. Repeat steps 5-7 for ```\Documents\maya\scripts\t-rig.py```

## Usage

1. C-Rig: creates a controller and locators for curve(s)
   1. Select either:
      * 1 curve which will be duplicated and can later be edited, or
      * 2 curves: 1 for the front of the vehicle (name should contain "front") and 1 for the back (name should contain "back")
   2. Click your "C-Rig" shelf button
   3. 4 locators will be created:
      * <b>vehicle_controller</b> (Blue): Move and key this locator to control the position along the curve.
      * <b>vehicle_front</b> (Red): Will be attached to the front of the vehicle. Controlled by vehicle_controller.
      * <b>vehicle_back</b> (Green): Will be attached to the back of the vehicle. Controlled by vehicle_controller.
      * <b>back_locator</b> (Yellow): Don't mess with this unless you know what you're doing. Helps calculate the position of vehicle_back.
   4. In addition, the original curve(s) will be recolored accordingly:
      * <b>Front</b>: Red
      * <b>Back</b>: Green
   5. Change the vehicle length by selecting the <b>vehicle_controller</b> and changing the "Vehicle Length" attribute in either the Channel Box or the Attribute Editor under Extra Attributes
2. T-Rig: attaches a vehicle to the locators
   1. Make sure your vehicle is contained in a group and that the group's pivot is located on "the ground" between the front wheels
   2. Select all of the following:
      * vehicle_front
      * vehicle_back
      * Group containing the vehicle
   3. Click your "T-Rig" shelf button
   4. The vehicle will be attached to the locators. You can move the <b>vehicle_controller</b> to move the vehicle.
      * NOTE: If the vehicle's rotation is incorrect, change the Aim Vector of the aim constraint:
         1. Under <b>vehicle_front</b>, select it's aim constraint
         2. Open the Attribute Editor to Aim Constraint Attributes
         3. Edit the aim vector so that the vehicle rotates in the correct direction

---


#### Contributors

Jake Cheek - [@jgchk](https://github.com/jgchk)

#### License

GPL
