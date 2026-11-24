# Microcontroller Code - IMU Subsystem

The IMU subsystem is controlled by a Microchip PIC18F57Q43 Curiosity Nano programmed using MPLAB X IDE and MPLAB Code Configurator (MCC).

The subsystem receives a 0–5 V digital enable signal from the team interface. When the subsystem is enabled, the microcontroller monitors a BMI270 accelerometer/gyroscope using I²C communication. When the programmed motion-detection criteria are satisfied, the microcontroller asserts the required 0–5 V digital team output signals.


## Pin Configuration

The following PIC18F57Q43 pins are used by the IMU subsystem:

| Signal | PIC Pin | Direction | Purpose |
| --- | --- | --- | --- |
| BMI270 SDA | RB2 | I/O | I²C data connection to BMI270 |
| BMI270 SCL | RB1 | I/O | I²C clock connection to BMI270 |
| HAN_INPUT | RA0 | Input | Digital enable signal from Hannah's subsystem |
| MAT_OUTPUT | RD2 | Output | Digital output to Matthew's subsystem |
| YAZ_OUTPUT | RD5 | Output | Digital output to Yazmin's subsystem |
| TEAM_EXTRA_OUTPUT | RF1 | Output | Revised team GPIO connection |
| DEBUG_LED | RD0 | Output | Firmware/debug indication |
| DEBUG_BUTTON | RD1 | Input | Development and hardware-test input |

## Firmware Verification

Before final PCB assembly, the team-interface GPIO logic was tested directly using the PIC18F57Q43 Curiosity Nano.

For this test, `HAN_INPUT` represented the external subsystem-enable signal and `DEBUG_BUTTON` temporarily simulated an IMU detection event.

| HAN_INPUT | Simulated IMU Event | Team Outputs |
| --- | --- | --- |
| LOW | LOW | LOW |
| HIGH | LOW | LOW |
| LOW | HIGH | LOW |
| HIGH | HIGH | HIGH |

With both test inputs HIGH and the Curiosity Nano operating at the required 5 V, `MAT_OUTPUT`, `YAZ_OUTPUT`, and `TEAM_EXTRA_OUTPUT` each measured approximately **5.01 V** with a digital multimeter.

When either input was LOW, the team outputs remained LOW.

## BMI270 Communication

The BMI270 accelerometer/gyroscope communicates with the PIC18F57Q43 through the I²C1 peripheral.

The firmware includes support for:

- BMI270 register reads and writes
- BMI270 chip-ID verification
- Multi-byte I²C reads
- Raw X/Y/Z accelerometer measurements
- Raw X/Y/Z gyroscope measurements
- I²C communication error and timeout handling

The BMI270 uses the 7-bit I²C address `0x68`.

Final BMI270 hardware communication, initialization, and motion-detection calibration will be verified using the assembled subsystem PCB.

## Microcontroller Code

The MPLAB X project used for the final subsystem hardware verification will be provided as a packaged ZIP archive.

**Final MPLAB X project:** To be uploaded after final hardware verification.


