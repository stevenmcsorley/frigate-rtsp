# Frigate NVR Docker Configuration

This repository contains the Docker configuration for our Frigate NVR system. Frigate is an advanced Network Video Recorder (NVR) which uses AI object detection to improve video surveillance capabilities.

## Configuration Details

The configuration file in this repository is designed to work with Frigate and a MQTT server. It includes settings for object detection, motion detection, recording, and more. The configuration is set to prevent Frigate from recording stationary objects and to ignore the top half of the camera's view.
In this example a TAPO 360 CAmera was used as it provides RTSP streaming and is compatible with Frigate. The camera is configured to stream at 1080p and 15 FPS. Update as needed for your camera.

## Getting Started

To use this configuration, you will need to have Docker and Docker Compose installed on your system. You will also need a compatible video camera and a MQTT server.

1. Clone this repository to your local machine.
2. Update the `mqtt` section in the configuration file with your MQTT server details.
3. Update the `cameras` section with your camera details.
4. Run `docker-compose up -d` to start the Frigate NVR system.

## Configuration Breakdown

The configuration file is written in YAML and contains several sections:

- `mqtt`: This section contains the settings for the MQTT server.
- `cameras`: This section contains the settings for each camera, including the RTSP stream path and the object detection settings.
- `detect`: This section contains the settings for the object detection, including the frame size and rate.
- `objects`: This section contains the settings for the objects to be tracked.
- `record`: This section contains the settings for the video recording.

Please refer to the comments in the configuration file for more details about each setting.

## Contributing

Contributions are welcome. Please open an issue or submit a pull request if you have any improvements or suggestions.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.