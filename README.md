# pi_filtered_adc_board
PCB for R-pi with 8-channel ADC with 2nd order active low pass filters.

This is a KiCad schematic and PCB design for a PCB that connects to a
Raspberry Pi via the 40-pin GPIO connector. The board hosts an 8-channel
ADC connected vi SPI to the R-Pi, with single supply op-amps and passive
component positions to implement a 2nd-order Butterworth low-pass filter
on each channel. 

A convenient pin-grid is supplies to connect the ADC to the SPI0 or SPI1 
interfaces on the R-Pi, or to connect the SPI interface of the ADC to any
R-Pi GPIO pins.

If you don't want to implement 2nd order filters on the inputs, you can simply
omit the filter capacitors and replace resistors with wire links to use the 
opamps and simple buffers, or you could place resistors to set gain.

Resistor placements are provided to allow for example forming a potential 
divider with an on-board resistor and an off-board thermistor. The on-board
resistor placements can be shorted to provide +3.3 or +5v (selectable) on the
inputs D connector, providing for either 2 or 3-pin inputs (ie resistor or
potentiometer style inputs).

