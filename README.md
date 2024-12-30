# Smart Parking System Using Ultrasonic Sensor 🚗

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![Issues](https://img.shields.io/github/issues/phirojshah/smart-parking-system)
![Forks](https://img.shields.io/github/forks/phirojshah/smart-parking-system)
![Stars](https://img.shields.io/github/stars/phirojshah/smart-parking-system)

A simple yet effective parking spot monitoring system built with Arduino and ultrasonic sensors. This system helps detect vehicle presence and displays real-time parking spot availability.

## Overview

The Smart Parking System utilizes an HC-SR04 ultrasonic sensor connected to an Arduino Uno to detect whether a parking spot is occupied. When a vehicle enters the sensor's range, the system updates its status and displays it through the Serial Monitor.

## Features

- Real-time parking spot occupancy detection
- Configurable distance threshold for different parking scenarios
- Simple serial monitor interface
- Easy to set up and modify
- Expandable to multiple parking spots

## Hardware Requirements

- Arduino Uno board
- HC-SR04 Ultrasonic Sensor
- USB Type-A to USB Type-B cable
- Jumper wires (4x)
- Breadboard (optional)

## Wiring Instructions

Connect the components as follows:

| Ultrasonic Sensor | Arduino Uno |
|-------------------|-------------|
| VCC              | 5V          |
| Trigger          | Pin 6       |
| Echo             | Pin 7       |
| GND              | GND         |

## Software Setup

1. Clone this repository:
```bash
git clone https://github.com/phirojshah/smart-parking-system.git
cd smart-parking-system
```

2. Open Arduino IDE
3. Load the project file `smart_parking.ino`
4. Configure your Arduino IDE:
   - Select "Arduino Uno" from Tools > Board
   - Choose the correct port from Tools > Port
5. Click the Upload button (→) to flash the code

## Usage

1. After uploading the code, open the Serial Monitor (Tools > Serial Monitor)
2. Set the baud rate to 9600
3. The system will start displaying distance measurements and parking spot status
4. Default threshold distance is 10cm - modify `thresholdDistance` in the code to adjust

Example output:
```
Distance: 5 cm
Parking Spot: Occupied

Distance: 25 cm
Parking Spot: Vacant
```

## How It Works

The system operates using these key components:

- **Distance Calculation**: Uses the speed of sound (343 m/s) to calculate distance based on the time taken for the ultrasonic pulse to return
- **Status Detection**: Compares measured distance with a threshold to determine if a spot is occupied
- **Serial Output**: Provides real-time feedback through the Arduino Serial Monitor

## Customization

You can modify these parameters in the code:

```cpp
const int thresholdDistance = 10; // Distance threshold in centimeters
const int trigPin = 6;           // Trigger pin connection
const int echoPin = 7;           // Echo pin connection
```

## Future Enhancements

- Add LED indicators for visual feedback
- Implement LCD display support
- Create a web/mobile interface
- Add multiple sensor support
- Integrate with parking management systems
- Add data logging capabilities

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b new-feature`
3. Commit your changes: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin new-feature`
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

- Open an issue for bug reports or feature requests
- Submit a pull request to contribute
- Star the repository if you find it useful

## Authors

- Initial work - [Your Name]

## Acknowledgments

- Thanks to the Arduino community for their excellent documentation
- Inspired by modern parking management systems
