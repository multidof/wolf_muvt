cmake_minimum_required(VERSION 3.0.0)
project(wolf_muvt)

find_package(PkgConfig)
pkg_check_modules(EIGEN eigen3)
find_package(catkin REQUIRED COMPONENTS
    muvt_ros
    )

catkin_package()

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
  PATTERN ".svn" EXCLUDE)

install(DIRECTORY params/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/params
  PATTERN ".svn" EXCLUDE)

install(DIRECTORY rviz/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/rviz
  PATTERN ".svn" EXCLUDE)
