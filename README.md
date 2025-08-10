# picoPD_interrogator [Hardware Repository]
## __WARNING:__ Please see the 'Known Issues' section below.

If you're looking for firmware: [rp2040_pd_bmc](https://github.com/Samuelrmlink/rp2040_pd_bmc)

## Known issues
-------------------
[RevD-RC1-RC2](./docs/Rev_D.md)
- Pad connection to GP26 and GP27 ADC inputs should be cut to avoid RP2's internal diodes from drawing current from the CC pins when 3.3v is not present on the Pico. This will be addressed on a future revision - the consequence of this modification is just that we loose the ability to read the ADC voltage on each CC pin. 
- RevD-RC1 SWDIO and SWDCLK may be swapped on the schematic - likewise UART_RX and UART_TX may be swapped

[RevC-RC2](./docs/Rev_C.md)
* The NXP NX3DV3899 switch used to select CC lines doesn't actually connect common to either NC or even NO when the chip is unpowered. This was a design oversight when selecting this component for this use case. 
* Production of this PCB version is __NOT__ recommended.

[RevB](./docs/Rev_A_B.md)
* Everything works as expected design-wise
* This version lacks any voltage regulator for powering the Pico from VBUS power
* External USB power or a connected Flipper Zero may be used for operation

[RevA](./docs/Rev_A_B.md)
* USB-C port PCB footprint was incorrect & would not align with the target USB-C port (SM-G950 port)
* Comparator pins were connected incorrectly on this version - see RevB for the appropriate correction
* Production of this PCB version is __NOT__ recommended.




