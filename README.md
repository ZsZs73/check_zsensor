Icinga/Nagios check for zSensor
===============================

The script is to query zSensor (web based temperature/humidity sensor)

Both low and high thresholds can be defined. 
For example, let's set the following thresholds:
```
----5----10---------------27-------35------
  -c 5  -w 10           -W  27   -C 35
```
Readings of the sensor will result following alarms:
- 3 °C: CRITICAL - temperature reading 3 is lower than critical low [5]
- 7 °C: WARNING - temperature reading 7 lower than warning low [10]
- 15 °C: OK
- 29 °C: WARNING - temperature reading 29 higher than warning high [27]
- 38 °C: CRITICAL - temperature reading 38 higher than critical high [35]

# Known limitations
Only integers are supported as critical/warning thresholds.

# License
MIT
