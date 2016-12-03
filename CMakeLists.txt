cmake_minimum_required(VERSION 2.8)
project(ros_fview_fmf_saver)

find_package(catkin REQUIRED message_generation std_msgs)

add_service_files()

generate_messages(DEPENDENCIES std_msgs)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)

catkin_install_python(PROGRAMS nodes/start_saving_fmf
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
