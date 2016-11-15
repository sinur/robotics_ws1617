cmake_minimum_required(VERSION 2.8.3)
project(robotics_u2)

find_package(catkin REQUIRED COMPONENTS
	roscpp
	rospy
	std_msgs
	genmsg
	sensor_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES robotics_u2
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

include_directories(${catkin_INCLUDE_DIRS})

add_executable(subscriber src/subscriber.cpp)
target_link_libraries(subscriber
	${catkin_LIBRARIES}
)
