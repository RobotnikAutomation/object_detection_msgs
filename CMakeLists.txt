cmake_minimum_required(VERSION 3.0.2)
project(object_detection_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS std_msgs message_generation)


#######################################
## Declare ROS messages and services ##
#######################################

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  DetectorState.msg
  DetectorsState.msg
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  ManageDetector.srv
  SetFrequency.srv
)

#add_action_files(
#    FILES
#    action.action
#)


## Generate added messages and services with any dependencies listed here
generate_messages(
DEPENDENCIES
   std_msgs  # Or other packages containing msgs
)

catkin_package(CATKIN_DEPENDS
  message_runtime
  std_msgs
)
