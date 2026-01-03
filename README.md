# Mumo - Compact ICM-45686+QMC6309 Module

A compact 13×18mm IMU module featuring the TDK InvenSense ICM-45686 6-axis IMU with integrated 32.768kHz clock and QST QMC6309 3-axis magnetometer.

![PCB Image](http://cdn.kouno.xyz/sppRNCOt.png)

## Features

- **Compact Design**: 13×18mm form factor
- **High-Performance IMU**: TDK InvenSense ICM-45686 6-axis IMU with integrated 32.768kHz clock for precise output timesteps
- **3-Axis Magnetometer**: QST QMC6309 for 9-DOF sensing
- **Connectivity**: Castellated holes for flat mounting on compatible carrier PCBs
- **Power Optimization**: Solder bridges to disconnect I2C pull-ups for improved power efficiency when using SPI
- **Easily Configurable I2C Address**: Solder bridge for SD0 pin to change I2C address from `0x69` to `0x68`

## Compatibility

The pinout is **mostly compatible** with popular BMI160 and LSM6DS3 modules found on Amazon and AliExpress, with these differences:

- **OSDO**: Functions as VIN on AliExpress modules
- **CLK_CTL**: Not present on AliExpress modules

## Schematic

![Schematic](http://cdn.kouno.xyz/7azwuG30.png)

## Ordering Information

### Important Notes

⚠️ **IMU Pin 7**: Pin 7 of the IMU is intentionally disconnected as recommended for the ICM-45686. If substituting with another IMU that requires pin 7 as GND, modify the PCB to connect IMU pin 7 to ground.

⚠️ **Surface Finish**: ENIG surface finish is recommended for easier soldering and better reliability with the BGA magnetometer.

⚠️ **Castellated Holes**: While castellated holes significantly increase manufacturing cost, they enable flat soldering onto carrier boards. Consider your application requirements before deciding to omit them.

## License

See [LICENSE.md](LICENSE.md) for license information.