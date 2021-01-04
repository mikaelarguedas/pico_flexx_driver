cmake_minimum_required(VERSION 3.0.2)

project(pico_flexx_driver)

## Find catkin macros and libraries
find_package(catkin REQUIRED)

catkin_package()

#############
## Install ##
#############

## Mark other files for installation (e.g. launch and bag files, etc.)
install(DIRECTORY
  launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
install(FILES
  nodelet_plugins.xml
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(PROGRAMS
  cmake/findPicoFlexxSDK.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
