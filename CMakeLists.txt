cmake_minimum_required(VERSION 2.8.3)
project(state_server_msgs)

find_package(catkin REQUIRED COMPONENTS rtt_roscomm geometry_msgs sensor_msgs message_generation actionlib_msgs)

#add_action_files(DIRECTORY action FILES BHMove.action)
#add_message_files(DIRECTORY msg FILES BHPressureState.msg BHTemp.msg BHPressureInfo.msg BHPressureInfoElement.msg)
add_service_files(DIRECTORY srv FILES ChangeState.srv)

generate_messages(DEPENDENCIES geometry_msgs sensor_msgs actionlib_msgs)

catkin_package(
  CATKIN_DEPENDS geometry_msgs sensor_msgs message_runtime)
