# Robotics ws 16/16

## install ros
* look [here](http://wiki.ros.org/kinetic/Installation/Ubuntu)

## connect to car
* WIFI SSID: `ROS`
* WIFI Password: `elfmeter`
* Car IP: `192.168.43.102`
* Car ROS Port: `11311`
* Get local IP Adress ` ifconfig | grep inet`

 __Exports:__

 ```bash
export ROS_IP=<local ip address>
export ROS_HOSTNAME=<local ip address>
export ROS_MASTER_URI=http://192.168.43.102:11311
 ```
`
