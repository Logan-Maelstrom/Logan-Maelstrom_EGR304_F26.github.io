---
title: Component Selection Example
---

## Examples

### Style 1

> This is the example found in the assignment, uses more html

*Table 1: Example component selection*

**External Clock Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](image1.png)<br>Option 1.<br> XC1259TR-ND surface mount crystal<br>$1/each<br>[link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)                 | \* Inexpensive[^1]<br>\* Compatible with PSoC<br>\* Meets surface mount constraint of project                                               | \* Requires external components and support circuitry for interface<br>\* Needs special PCB layout. |
| ![](image3.png)<br>\* Option 2. <br>\* CTX936TR-ND surface mount oscillator <br>\* $1/each <br>\* [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940) | \* Outputs a square wave <br>\* Stable over operating temperature <br> \* Direct interface with PSoC (no external circuitry required) range | * More expensive <br>\* Slow shipping speed                                                         |

**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.

### Style 2

> Also acceptable, more markdown friendly

**6-Axis Inertial Measurement Unit (IMU)**

1. BMI323 surface mount accelerometer/gyroscope (6 axis)

    ![](BMI323.png)

    * $3.91/each
    * [link to product](https://www.digikey.com/en/products/detail/bosch-sensortec/BMI323/16719593)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Low power consumption                     | Tiny 14-pin LGA package                                          |
    | Compatible with 3.3 V rail                | More features than our project application may require           |
    | Supports I²C                              | Requires software/configuration work                             |
    | Small package                             | No integrated magnetometer                                       |
    | Built-in motion/orientation detection     |
    | Wide programmable measurement ranges      |

2. BMI270 surface mount accelerometer/gyroscope (6 axis)

    ![](BMI323.png)

    * $4.23/each
    * [Link to product](https://www.digikey.com/en/products/detail/bosch-sensortec/BMI270/9974486)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Low power consumption                                             | More expensive than BMI323     |
    | Compatable with 3.3 V rail                                        | Tiny 14-pin LGA package is difficult to solder/prototype |
    | Supports I²C communication                                        | Many wearable features aren't useful for the specific Drowsy Driver Alarm project | 
    | Designed specifically for wearable applications                   | Requires software/configuration to work |
    | Small size/footprint (2.5mm x 3.0mm)                              |
    | Built-in motion detection features                                |

3. LSM6DSMTR surface mount accelerometer/gyroscope/temperature (6 axis)

    ![](LSM6DSMTR.png)

    * $4.55/each
    * [Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/LSM6DSMTR/6192777?s=N4IgTCBcDaIDYGcC2A2AJsgLgJxAXQF8g)
  
    | Pros                                                              | Cons                | 
    | ----------------------------------------------------------------- | ------------------- |
    | Low power consumption                                             | More expensive than both previous examples
    | Compatible with 3.3 V rail                                        | Tiny 14-pin LGA package is difficult to solder/prototype |
    | Supports I²C communication                                        | Older-generation IMU design | 
    | Built-in tilt detection and significant motion detection          | No I3C interface    |
    | High mechanical-shock robustness                                  | OIS/EIS features are unnecessary for our Drowsy Driver Alarm project |
    | Dedicated motion interrupts                                       | LGA package is difficult to prototype with |

**Choice:** Option 2: BMI270 surface mount accelerometer/gyroscope (6 axis)

**Rationale:** The BMI270 was manufactured with the purpose of wearable applications, such as recognizing human/head motion, making it a striking candidate from the list. Bosch specifically designed this chip for the same purpose our project is meant to portray. the BMI270 also has on-chip any-motion, no-motion, stationary, significant-motion, and activity-change recognition, which lines up incredibly well with that our project is trying to accomplish. Overall, this is our best candidate for a fair price, and there are plenty of units in stock on DigiKey with quick shipping times.
