
- POE means supplying power over normal data cables such as a voice over IP (VoIP) handset, camera, or wireless access point.
- PoE is defined in several IEEE **standards**:

	- **802.3af** **(Type 1 PoE or 2-pair PoE)** allows powered devices to draw up to about 13 W. Power is supplied as 350mA@48V and limited to 15.4 W, but the voltage drop over the maximum 100m (328 feet) of cable results in usable power of around 13 W. Basic devices such as a VoIP handset, basic wireless access points, and basic security cameras will use this standard.
	- **802.3at (PoE+ or Type 2 PoE)** allows powered devices to draw up to about 25 W, with a maximum current of 600 mA. Devices that require more power, such as advanced wireless access points, pan-tilt-zoom security cameras, and video IP phones, will use this standard.
	- **802.3bt (PoE++, Type 3 and Type 4 PoE, 4PPoE)** supplies up to about 51 W (Type 3) or 73 W (Type 4) usable power. Devices such as LED lighting, digital signage, point-of-sale systems, and other high-power devices will use this standard.


**PoE SWITCH**

A **PoE-enabled switch** is referred to as endspan power sourcing equipment (PSE). When a device is connected to a port on a PoE switch, the switch goes through a detection phase to determine whether the device is PoE enabled. If so, it determines the device's power consumption and sets an appropriate supply voltage level. If not, it does not supply power over the port and, therefore, does not damage non-PoE devices.
Powering these devices through a switch is more efficient than using a wall-socket AC adapter for each appliance. It also allows network management software to control the devices and apply energy-saving schemes, such as making unused devices go into sleep states and power capping.

## PoE Injector

If the switch does not support PoE, a device called a "power injector" (or "midspan") can be used. One port on the injector is connected to the switch port. The other port is connected to the device. The overall cable length cannot exceed 100m.