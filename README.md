# Pitch-control
Integrating electronics and mechanical system to maintain pitch through feedback loop
![20250630_175155](https://github.com/user-attachments/assets/48409ab8-0e53-4d81-8a90-e20b76c1dbe8)
**Devices used**
* **3D printed cross axis flexure joint**
* **3D printed slider crank mechanism**
* **Arduino uno 5 volt**
* **MPU6050 gyroscope sensor**
* **Hobby servos**
* **Breadboard and jumper cables**
* **Plastic bottle with dry rice**
* **Hot glue gun and tape**
* **DC power supply**



  As we see here, I tried to simulate rocket gamble to control pitch using a plastic bottle with some dry rice. The dry rice was chosen for stability and ease of weight manipulation. All the orange parts here are 3D printed using filament and it involves the cross axis flexure joint which allows sideways rotation and the slider crank mechanism which allow the servo to push the model. The plan was to have he model maintain its initial pitch, say zero degrees which point straight upward no matter how much I tilt the base. For example, if I tilt the base 30 degrees sideways, the model will also tilt 30 degrees sideways. And that is where the slider comes into play; it pushes the model back to zero degrees which it started with. Because of this constant feedback, the model always faces upward regardless of the tilt of the base.An MPU 6050 gyroscope was attached to the top of the model to act as a sensor so whenever there is a tilt felt, it would feed the data into the arduino so that it could relay the necessary rotation to the servos. One should push while the other one should pull but both cannot pull/push at the same time. When the servos rotate, the slider crank mechanism converts the rotational motion to linear motion, thereby pushing or pulling the sliders. Here. a breadboard was used to power the two servos and arduino seperately (more stable than powerng the servos directly from the arduino). Also, a 470 microfarad polarized capacitor was placed in parallel to the arduino and servos to stabilize the setup further. This avoids sudden voltage drops and power fluctuations caused by current surges when the servos move, which can lead to erratic behavior or resets of the arduino. Finally, the plan was to create a block diagram on Simulink so it can convert to a C++ code to run on the arduino chip. 

  Overall, the setup was perfect except for the sliders, they are misplaced here, because they had to touch directly at the side of the model (not in the behind and front). The slider also showed tendency to rotate instead of going back and forth as expected. So the missing piece here was a slider rail which could have restricted its rotation. But the issue I faced was how to place the slider in such a way that it would be sturdy, static, at the right elevation and at the right distance. Also,there were concerns wether the gyroscope was placed at top where it experiences more vibration or at the base, where vibration levels are typically lower and the sensor may be less affected by mechanical disturbances. 
