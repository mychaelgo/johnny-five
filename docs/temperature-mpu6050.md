<!--remove-start-->

# Temperature - MPU6050

<!--remove-end-->






##### Breadboard for "Temperature - MPU6050"



![docs/breadboard/temperature-mpu6050.png](breadboard/temperature-mpu6050.png)<br>

Fritzing diagram: [docs/breadboard/temperature-mpu6050.fzz](breadboard/temperature-mpu6050.fzz)

&nbsp;




Run with:
```bash
node eg/temperature-mpu6050.js
```


```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var temperature = new five.Temperature({
    controller: "MPU6050"
  });

  temperature.on("change", function() {
    console.log("temperature");
    console.log("  celsius      : ", this.celsius);
    console.log("  fahrenheit   : ", this.fahrenheit);
    console.log("  kelvin       : ", this.kelvin);
    console.log("--------------------------------------");
  });
});


```








## Additional Notes
- [MPU-6050 - IMU with Temperature Sensor](http://www.invensense.com/products/motion-tracking/6-axis/mpu-6050/)

&nbsp;

<!--remove-start-->

## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.

<!--remove-end-->
