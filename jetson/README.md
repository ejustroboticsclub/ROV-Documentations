# Documentations of the Jetson Nano


### Basic Info
- Model: P3541 180-13542-DAAF-A02


### Commands

1. To access the Jetson via SSH:
   First, make sure to connect to the `ejust` wifi. Passward: `12345678`
   ```
   ssh jetson@192.168.0.102
   ```
   Then type the passward: `jetson`.
   
   </br> </br>
   
1. To list the devices connected to Jetson's ports:
   ```
   ls /dev/ttyACM*
   ```
   or use this:
   ```
   ls ls /dev/ttyUSB*
   ```
   or you can use this alias:
   ```
   ports
   ```

   </br> </br>

1. To start a RTSP server to stream a video from a connected camera device:
   ```
   v4l2rtspserver -W <width> -H <height> -F <frame rate> -P <port> <video-input-device>
   ```
   `<video-input-device>` can be `/dev/video0`.

   </br> </br>

1. 
   
   
