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
   
