Markdown
???? Auto Feeding System for Dogs

A/

## ?????????? Project Overview
It is a cheap, programmable robotic feeder for pets that can be utilized in shelters for pets. It is programmable such that it can feed the dogs and cats dry rations at specified hours, store rations eaten, and inform personnel of being out of food trays or non-eating pets. It is utilizing cheap off-the-shelf components such as servo motors and sensors in a bid to be economical and durable.

---

## ⚙️ Features
- Timed feeding (morning and evening)
- Detection of the storage bin level at the food level
CALCULATION OF INTAKE FROM MEASUREMENTS OF BOWL WEIGHTS
-Regular first aid and safety drills
- Exclusively for dry food
-No internet, no cell notifications logical control functionality

---

Components of the System

### Inputs
| Enter                | Type        | example values     | Comments                              |
|--------------------
| Feeding Schedule     | Time (hh:mm)| 08:00, 18:00       | Manually set by staff                  |
| Real-Time Clock | System Time | 07:59, 08:00       | 24-hour format                         |
| Food Level Sensor    | Boolean/Int | 1 = present, 0 = empty | Only senses food presence         |
| Bowl Weight Sensor | Float (g) | 0g → 250g         | ±5g accuracy                           |

### Outputs
| Output               | Type        | Example Values     | Notes                                 |
|----------------------|-------------|--------------------|--------------------------------------|
|--------------------
| Servo Motor          | Action      | 45° rotation       | Releases a single portion                |
| Alert System         | Message     | “Food bin empty”, “Pet did not eat” | Simple, localized alerts only

---

## ???? Algorithmic Reasoning
1. Verify whether the current hour is feeding time.
2. In case, check that double-check food bin is in food.
3. If there is food, rotate servo motor to release.
4. Weight bowl after 30 minutes.
5. Notify staff if no weight gain, then the animal did not eat.
6. Inform employees right away if the bin of food is depleted.

---

## ???? Sample Pseudocode


````
READ currentTime
FOR EACH feedingTime IN schedule DO
If currentTime is feedingTime TH
READ foodBinLevel
IF foodBinLevel = 0 THEN SEND alert("Food bin empty")

CONTINU
