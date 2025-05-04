# picoPD_interrogator [Hardware Repository]
## __WARNING:__ The current hardware design version may have issues! Please see the 'Known Issues' section below.

If you're looking for firmware: [rp2040_pd_bmc](https://github.com/Samuelrmlink/rp2040_pd_bmc)

## Known issues
-------------------
[RevC-RC2]
* The NXP NX3DV3899 switch used to select CC lines doesn't actually connect common to either NC or even NO when the chip is unpowered. This was a design oversight when selecting this component for this use case. 
* Production of this PCB version is __NOT__ recommended.
[RevB]
* Everything works as expected design-wise
* This version lacks any voltage regulator for powering the Pico from VBUS power
* External USB power or a connected Flipper Zero may be used for operation
[RevA]
* USB-C port PCB footprint was incorrect & would not align with the target USB-C port (SM-G950 port)
* Comparator pins were connected incorrectly on this version - see RevB for the appropriate correction
* Production of this PCB version is __NOT__ recommended.




