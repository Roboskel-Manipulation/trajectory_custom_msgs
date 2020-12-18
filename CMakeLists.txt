cmake_minimum_required(VERSION 3.0.2)
project(trajectory_custom_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  geometry_msgs
  message_generation
)

## Generate messages in the 'msg' folder
add_message_files(
	FILES
	PointArray.msg
	PointStampedArray.msg
)

generate_messages(
	DEPENDENCIES
	geometry_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES trajectory_custom_msgs
 CATKIN_DEPENDS geometry_msgs message_runtime
#  DEPENDS system_lib
)
