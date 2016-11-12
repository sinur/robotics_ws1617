# Robotics ws 16/16

Use the [stackedit.io](https://stackedit.io/editor) online markdown editor with LaTeX support, or use [GitHub's Atom](https://atom.io/) editor with  [LaTeX plugin](https://atom.io/packages/markdown-preview-enhanced).

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
