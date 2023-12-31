# pfpp-rtcc-boosterpack
A boosterpack-compatible board for pfpp project.

This board holds a battery-backup'ed precision RTCC. It's main duty is to keep the time of the day and manage alarms that are set for feeding your pet.

on top of an RTCC, it also holds a MicroSD card cage, and a TB6612 motor controller. The MicroSD card can be used for logging events. The motor controller is used to activate the feeder.

This project was originally built for the EK-TM4C129EXL development board, on boosterpack2 location. It should work on any BoosterPack-compatible interface.

## GPIO Mapping

GPIO match for various development boards.

### EK-TM4C129EXL

J1
Pin | MCU Pin | BoosterPack Schematic
--- | --- | ---
1 | +3.3V | +3.3V
2 | PD2 | NC
3 | PP0 | NC
4 | PP1 | NC
5 | See JP4 | SPI_SDC_CSn
6 | See JP5 | NC
7 | PQ0 | SPI_CLK
8 | PP4 | NC
9 | PN5 | NC
10 | PN4 | NC

J2
Pin | MCU Pin | BoosterPack Schematic
--- | --- | ---
1 | GND | GND
2 | PM7 | NC
3 | PP5 | NC
4 | PA7 | SD_DET
5 | Reset | NC
6 | PQ2/PA3 | SPI_MOSI
7 | PQ3/PA2 | SPI_MISO
8 | PP3 | RTCC_INTn
9 | PQ1 | SPI_RTCC_CSn
10 | PM6 | AIN2

J3
Pin | MCU Pin | BoosterPack Schematic
--- | --- | ---
1 | +5V | NC
2 | GND | GND
3 | PB4 | NC
4 | PB5 | NC
5 | PK0 | NC
6 | PK1 | NC
7 | PK2 | NC
8 | PK3 | NC
9 | PA4 | NC
10 | PA5 | NC

J4
Pin | MCU Pin | BoosterPack Schematic
--- | --- | ---
1 | PG1 | PWMB
2 | PK4 | PWMA
3 | PK5 | NC
4 | PM0 | NC
5 | PM1 | NC
6 | PM2 | BIN2
7 | PH0 | BIN1
8 | PH1 | STBYn
9 | PK6 | AIN1
10 | PK7 | RTCC_RST

### EK-TM4C123GXL

**Even if the board was 1st developed for the EK-TM4C129EXL, the GPIO pin matching for the EK-TM4C123GXL corresponds to the symbols in the schematic.**

Pin | J1 MCU Pin | J1 BoosterPack Schematic | J3 MCU Pin | J3 BoosterPack Schematic
--- | --- | --- | --- | ---
1 | +3.3V | +3.3V | +5V | NC
2 | PB5 | NC | GND | GND
3 | PB0 | NC | PB4 | NC
4 | PB1 | NC | PB5 | NC
5 | PE4 | SPI_SDC_CSn | PK0 | NC
6 | PE5 | NC | PK1 | NC
7 | PB4 | SPI_CLK | PK2 | NC
8 | PA5 | NC | PK3 | NC
9 | PA6 | NC | PA4 | NC
10 | PA6 | NC | PA5 | NC


Pin | J4 MCU Pin | J4 BoosterPack Schematic | J2 MCU Pin | J2 BoosterPack Schematic
--- | --- | --- | --- | ---
1 | PF2 | PWMB | GND | GND
2 | PF3 | PWMA | PB2 | NC
3 | PB3 | NC | PB0 | NC
4 | PC4 | NC | PF0 | SD_DET
5 | PC5 | NC | Reset | NC
6 | PC6 | BIN2 | PB7 | SPI_MOSI
7 | PC7 | BIN1 | PB6 | SPI_MISO
8 | PD6 | STBYn | PA4 | RTCC_INTn
9 | PD7 | AIN1 | PA3 | SPI_RTCC_CSn
10 | PC4 | RTCC_RST | PA2 | AIN2

