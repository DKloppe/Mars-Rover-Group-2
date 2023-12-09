# Mars-Rover-Group-2

## Altitude/Pressure

Altitude was recorded by the GPS and BARO sensors. The BARO sensor uses a zero altitude position as the initial point and uses pressure changes to determine the altitude. This can be seen in the inverse relationship between its altitude and pressure readings. A source for the ground truth was found on calcmaps.com, which is linked below. Based on the rise and fall in altitude at the waypoints, it is evident the sensor's readings are not ideal. A possible reason for this relates to how the altitude uses the pressure readings. The day the test was conducted was windy, with infrequent gusts. It is possible the wind gusts could alter the air pressure in slight ways, and therefore could lead to inacurate readings. If readings on the wind speed were gathered, it may be possible to utilize Bernouli's principle and subtract the pressure caused by the wind, which would in turn lead to a more accurate altitude reading.

The altitude from the GPS sensor is relative to sea level and is pulled from the GPS and mission planner software. When compared to the readings from calcmaps, the readings seem to be fairly off. One worthy note of detail is that the initial altitude seems to be very high, before it suddenly drops down. It is possible this is due to the sensor still finding its position. During the initial start up of the rover, ten to twenty minutes were used to let the GPS find itself. On mission planner, this was visible by the rover seemingly jumping from place to even though it was stationary. It is possibly that because the rover was turned on, it was armed, and its pathing was initialezed within seconds of each other, that the GPS was still finding itsself. In future tests, it may be possible to prevent this by giving the rover a minimum of five minutes between start-up and initalizing.  



## DHT-11

DHT-11 data was only recorded for 301 seconds of the total run however when looking at the data we see a recorded range of 14.3 to 13.3 degrees Celsius looking at the link below for our time frame of testing from 2:00 P.M. to 3:00 P.M. we can say that the DHT-11 is fairly accurate in it's temperature readings. As far as humidity it appears to also be accurate to data found from weather stations.




## BARO/IMU_Temp 

The BARO temperature sensor like the DHT-11 senses the surrounding ambient temperature however since the BARO is in close proximity to the IMU you notice that the IMU temperature and Baro temperature are practically overlapping with each other. To deal with this discrepancy you should program the software of your navio to subtract the IMU temperature from your BARO and affect the hardware of your system so the BARO has better access to notice the ambient temperature instead of being insulated in the rover.

## Links for accuracy 
Humidity link (https://www.localconditions.com/weather-edwardsville-illinois/62025/past.php) Look for Fri December 1

Temperature and Pressure link note pressure is in millibar and needs conversion to pascals look for the 2 pm value (https://www.visualcrossing.com/weather/weather-data-services/Edwardsville,%20Il/metric/2023-12-01/2023-12-01#)

Calcmaps link to find accurate altitude  (https://www.calcmaps.com/map-elevation/)



## Waypoints

The displacement from the expected path was monitored in NTUN.XTrack. There was a maximum deviation of 1.95 meters. The next maximum deviation was 0.57 meters. 
Both of these errors were preceded by the only right turns conducted during the rover's operation, leading to an idea; if the error is greatest after each right turn, then the rover has an issue turning right. After disassembling, it was noticed that one of the motor housings had broken. The breakage was around one of the mounting screws. It is possible for this breakage to cause problems with torques in only one direction, which could explain why the error reached its top two maximums only during its right turns.

The distances from the next waypoint was also recorded. The total distance traveled was found to be 165.34 meters. This distance is greater than the projected 160 meters based on the path setting. It is still possible for this to be true because the rover's slight swerving and overcorrecting leads to further distance needed for completion. The swerving was originally reduced with Position Integral Derivative (PID) adjustments. The position was first adjusted so the rover would stay in the right direction. An appropriate value was determined to be 0.5. The integral was adjusted next so the error sum would minimize. Having this too high resulted in an oscilitory motion around the expected path, so it was placed at 0.02. Finally, the derivitive was left alone due to advisement from Brandon Hickey, so it was at 0. These steps were taken to minimize the difference between the total and projected distances. The extra 5 meters may be mostly due to the motor housing breakage. As stated earlier, the breakage could have resulted in the major deviations. By reducing the deviations with a more stable motor housing, it may have been possible to reduce the total distance traveled even further.
