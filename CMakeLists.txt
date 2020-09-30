cmake_minimum_required(VERSION 3.5)
project(aliencontrol)

## Find catkin macros and libraries.
## If COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages.
find_package(ament_cmake_auto REQUIRED)
ament_auto_find_build_dependencies()

###################################
## catkin-specific configuration ##
###################################
## The catkin_package macro generates cmake config files for your package.
## Declare things to be passed to dependent projects.
## INCLUDE_DIRS: uncomment this if your package contains header files.
## LIBRARIES: libraries you create in this project that dependent projects also need.
## CATKIN_DEPENDS: catkin_packages dependent projects also need.
## DEPENDS: system dependencies of this project that dependent projects also need.
# catkin_package(
#     CATKIN_DEPENDS rospy
# )
ament_export_dependencies()

#############
## Install ##
#############
# TODO Is there an ament variable that stores the destination?
# install(PROGRAMS ${PROJECT_NAME} RENAME ${PROJECT_NAME}_exe DESTINATION share)
install(PROGRAMS ${PROJECT_NAME} RENAME ${PROJECT_NAME}_exe DESTINATION lib/${PROJECT_NAME})

ament_auto_package()
