# Mars-Rover-Group-2

## Altitude/Pressure

Altitude was recorded by the GPS and BARO sensors. The BARO sensor uses a zero altitude position as the initial point and is also working on the pressure-altitude sensing principle to find the altitude, while the altitude from the GPS sensor is relative to sea level and is pulled from the GPS sensor and mission planner software. When looking 



## DHT-11

DHT-11 data was only recorded for 301 seconds of the total run however when looking at the data we see a recorded range of 14.3 to 13.3 degrees Celsius looking at the link below for our time frame of testing from 2:00 P.M. to 3:00 P.M. we can say that the DHT-11 is fairly accurate in it's temperature readings. As far as humidity it appears to also be accurate to data found from weather stations.




## Baro/IMU_Temp 

The Baro temperature sensor like the DHT-11 senses the surrounding ambient temperature however since the Baro is in close proximity to the IMU you notice that the IMU temperature and Baro temperature are practically overlapping with each other. To deal with this discrepancy you should program the software of your navio to subtract the IMU temperature from your Baro and affect the hardware of your system so the Baro has better access to notice the ambient temperature instead of being insulated in the rover.

## Links for accuracy 
Humidity link (https://www.localconditions.com/weather-edwardsville-illinois/62025/past.php) Look for Fri December 1

Temperature and Pressure link note pressure is in millibar and needs conversion to pascals look for the 2 pm value (https://www.visualcrossing.com/weather/weather-data-services/Edwardsville,%20Il/metric/2023-12-01/2023-12-01#)

Calcmaps link to find accurate altitude  (https://www.calcmaps.com/map-elevation/)





1

## Waypoints

The displacement from the expected path was monitored in NTUN.XTrack. 
There was a maximum deviation of 1.95 meters. 
The next maximum deviation was 0.57 meters. 
Both of these errors were preceded by the only right turns conducted during the rover's operation, leading to the hypothesis; if the error is greatest after each right turn, then the rover has an issue turning right.  
