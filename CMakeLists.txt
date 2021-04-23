cmake_minimum_required(VERSION 3.0.2)
project(autocycle_extras)
find_package(catkin REQUIRED COMPONENTS message_generation roscpp std_msgs)
add_message_files(FILES
  Object.msg
  Point.msg
  ObjectList.msg
)
add_service_files(FILES
  LvxData.srv
  RollAdj.srv
  GetData.srv
  DetectObjects.srv
  CalcDeltas.srv
  GetDelta.srv
  ObjectDetectionList.srv
)
generate_messages(DEPENDENCIES std_msgs)
catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
include_directories(include ${catkin_INCLUDE_DIRS})
