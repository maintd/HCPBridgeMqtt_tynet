# How to connect sensors to a prebuild PCBs

The prebiuld PCBs sold by tynet.eu have four expansion ports ready to be extended with temperature sensors and more.
Adding a sensor is NOT plug & play currently, but still simple to get up and running.

## The expansion ports

| Name        | Pin 1 | Pin 2 | Pin 3 | Pin 4 |
| ----------- | ------|-------|-------|-------|
| EXP_1       | 3V3 | GND | IO_5 | IO_6       |
| EXP_2       | GND | IO_7 | IO_8 | 3V3       |
| ONEWIRE_1   | GND | IO_4 | 3V3  |           |
| ONEWIRE_2   | GND | IO_40 | 3V3 |           |


Here you can also see the pin layout on the PCB

![pinout](Images/pin_layout_hcpbridge_tyneteu.png)
