cmake_minimum_required(VERSION 3.0.2)
project(sigverse_hsrb_utils)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  geometry_msgs
  trajectory_msgs
  tf
  message_generation
)

################################################
## Declare ROS messages, services and actions ##
################################################

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  HandymanMsg.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

###################################
## catkin specific configuration ##
###################################
catkin_package(
  CATKIN_DEPENDS roscpp rospy std_msgs message_runtime
)

###########
## Build ##
###########

include_directories(
  ${catkin_INCLUDE_DIRS}
)

include_directories(include ${catkin_INCLUDE_DIRS})
link_directories(/usr/local/lib)

# add_executable(handyman_sample src/handyman_sample.cpp)
# target_link_libraries(handyman_sample ${catkin_LIBRARIES})
# add_dependencies(handyman_sample ${PROJECT_NAME}_generate_messages_cpp)

add_executable(teleop_key_handyman src/teleop_key_handyman.cpp)
target_link_libraries(teleop_key_handyman ${catkin_LIBRARIES})
add_dependencies(teleop_key_handyman ${PROJECT_NAME}_generate_messages_cpp)
# add_dependencies(teleop_key_handyman handyman_generate_messages_cpp)
