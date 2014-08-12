Compact the performance.sensor_readings collection, with paddingFactor set to 1.0. Then run homework.d() and enter the result below.

----

```
homework.d()
```
28
```
db.runCommand({compact : 'sensor_readings', paddingFactor: 1.0})
homework.d()
```
21
