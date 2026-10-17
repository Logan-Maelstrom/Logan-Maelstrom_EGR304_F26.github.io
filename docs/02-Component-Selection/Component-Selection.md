---
title: Component Selection Example
---

**6-Axis Inertial Measurement Unit (IMU)**

1. BMI323 Surface-Mount Accelerometer/Gyroscope/Temperature (6 axis)

    ![](BMI323.png)

    * $3.91/each
    * [link to product](https://www.digikey.com/en/products/detail/bosch-sensortec/BMI323/16719593)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Low power consumption                     | Tiny 14-pin LGA package                                          |
    | Compatible with 3.3V rail                 | More features than our project application may require           |
    | Supports I²C                              | Requires software/configuration work                             |
    | Small package                             | No integrated magnetometer                                       |
    | Built-in motion/orientation detection     |
    | Wide programmable measurement ranges      |

2. BMI270 Surface-Mount Accelerometer/Gyroscope/Temperature (6 axis)

    ![](BMI323.png)

    * $4.23/each
    * [Link to product](https://www.digikey.com/en/products/detail/bosch-sensortec/BMI270/9974486)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Low power consumption                                             | More expensive than BMI323     |
    | Compatable with 3.3V rail                                         | Tiny 14-pin LGA package is difficult to solder/prototype |
    | Supports I²C communication                                        | Many wearable features aren't useful for the specific Drowsy Driver Alarm project | 
    | Designed specifically for wearable applications                   | Requires software/configuration to work |
    | Small size/footprint (2.5mm x 3.0mm)                              |
    | Built-in motion detection features                                |

3. LSM6DSMTR Surface-Mount Accelerometer/Gyroscope/Temperature (6 axis)

    ![](LSM6DSMTR.png)

    * $4.55/each
    * [Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/LSM6DSMTR/6192777?s=N4IgTCBcDaIDYGcC2A2AJsgLgJxAXQF8g)
  
    | Pros                                                              | Cons                | 
    | ----------------------------------------------------------------- | ------------------- |
    | Low power consumption                                             | More expensive than both previous examples
    | Compatible with 3.3V rail                                         | Tiny 14-pin LGA package is difficult to solder/prototype |
    | Supports I²C communication                                        | Older-generation IMU design | 
    | Built-in tilt detection and significant motion detection          | No I3C interface    |
    | High mechanical-shock robustness                                  | OIS/EIS features are unnecessary for our Drowsy Driver Alarm project |
    | Dedicated motion interrupts                                       | LGA package is difficult to prototype with |

**Choice:** Option 2: BMI270 surface mount accelerometer/gyroscope (6 axis)

**Rationale:** The BMI270 was manufactured with the purpose of wearable applications, such as recognizing human/head motion, making it a striking candidate from the list. Bosch specifically designed this chip for the same purpose our project is meant to portray. the BMI270 also has on-chip any-motion, no-motion, stationary, significant-motion, and activity-change recognition, which lines up incredibly well with that our project is trying to accomplish. Overall, this is our best candidate for a fair price, and there are plenty of units in stock on DigiKey with quick shipping times.

----

**3.3V Voltage Regulator**

1. AP2112K-3.3TRG1 Surface-Mount 3.3V LDO Linear Regulator

   ![](APK2112K-3.3TRG1.png)

   * $0.28/each
   * [Link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP2112K-3-3TRG1/4470746)
  
   | Pros                                                              | Cons                |
   | ----------------------------------------------------------------- | ------------------- |
   | Very inexpensive                                                  | 80µA quiescent current     |
   | High 600mA output capacity                                        | Linear-regulator efficiency loss |
   | Low dropout voltage                                               | Limited to 6V maximum input voltage | 
   | Built-in overcurrent protection                                   | Surface-mount package may be more difficult to solder |
   | Built-in overtemperature protection                               | Fixed 3.3V output
   | Enable/shutdown control                                           |
   | High availability                                                 |

2. RT9080-33GJ5 Surface-Mount 3.3V LDO Linear Regulator

   ![](RT9080-33GJ5.jpg)

   * $0.28/each
   * [Link to product](https://www.digikey.com/en/products/detail/richtek-usa-inc/RT9080-33GJ5/6161634)
  
   | Pros                                                              | Cons                |
   | ----------------------------------------------------------------- | ------------------- |
   | Extremely low 4µA quiescent current                               | 5.5V maximum input voltage     |
   | High 600mA output capacity                                        | Higher maximum dropout than AP2112K |
   | 75dB power-supply rejection                                       | Surface-mount package may be more difficult to solder | 
   | Built-in overcurrent protection                                   | Fixed 3.3V output |
   | Built-in overtemperature protection                               | Linear-regulator efficiency loss
   | Enable/shutdown control                                           |
   | High availability                                                 |
   | Very inexpensive                                                  |

3. TLV75533PDBVR Surface-Mount 3.3V LDO Linear Regulator

   ![](TLV75533PDBVR.png)

   * $0.42/each
   * [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/TLV75533PDBVR/9685550)
  
   | Pros                                                              | Cons                |
   | ----------------------------------------------------------------- | ------------------- |
   | Low 31µA quiescent current                                        | Lower 500mA capacity than other candidates     |
   | Low 238mV maximum dropout                                         | Higher quiescent current than RT9080 |
   | Built-in overcurrent protection                                   | 5.5V maximum input | 
   | Built-in overtemperature protection                               | Fixed 3.3V output |
   | Wide -40°C to 125°C operating range                               | Linear-regulator efficiency loss
   | Compact SOT-23-5 package                                          |
   | High availability                                                 |

**Choice:** Option 2: RT9080-33GJ5 Surface-Mount 3.3V LDO Linear Regulator

**Rationale:** The RT9080-33GJ5 by Richtek has the lowest quiescent current of the candidates, being 4µA. Additionally, it still gives 600mA of maximum output current and is very affordable. Low power consumption is important for the Drowsy Driver Alarm project since the product is intended to be wearable. This LDO also provides exceptional protections built-in, such as overcurrent and overtemperature protection. Although its maximum input voltage is lower than other candidates like the AP2112K, this isn't a signifcant trade-off since the RT9080 can be powered by the system's 5V rail. Overall, this inexpensive LDO is exceptionally capable for our product's needs.

----

**5V Voltage Regulator**

1. L7805ACV-DG Through-Hole 5V LDO Linear Regulator

   ![](_____.png)

   * $1.21/each
   * [Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805ACV-DG/3945937)
  
   
