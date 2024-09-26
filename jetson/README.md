# Documentations of the Jetson Nano


### Basic Info
- Model: P3541 180-13542-DAAF-A02


### Commands

1. To access the Jetson via SSH:
   First, make sure to connect to the `ejust` wifi. Password: `12345678`
   ```
   ssh jetson@192.168.0.102
   ```
   Then type the password: `jetson`.
   
   </br>
   
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

   </br> 

1. To start a RTSP server to stream a video from a connected camera device:
   ```
   v4l2rtspserver -W <width> -H <height> -F <frame rate> -P <port> <video-input-device>
   ```
   `<video-input-device>` can be `/dev/video0`.

   </br> 

1. To check the Jetson's temperature:
   ```
   sudo tegrastats
   ```
   </br>

1. To list running processes and their corresponding ports:
   ```
   sudo lsof -i -n -p
   ```

   </br>
   
1. To Kill process using its id:
   ```
   sudo kill -9 <id>
   ```
   </br>

1. To view available wifi networks:
   ```
   nmcli d
   ```
   </br>

1. To connect to a wifi network:
   ```
   nmcli device wifi connect <SSID name> password <password>
   ```
   </br>
   
1. The Internet will not work if ethernet and wifi are both connected.
   To stop ethernet in order for wifi to work:
   ```
   sudo ifconfig eth0 down
   ```
   To stop wifi inorder for ethernet to work:
   ```
   sudo ifconfig wifi down
   ```
   </br>

1. To restart the Jetson:
   ```
   sudo reboot
   ```
   
