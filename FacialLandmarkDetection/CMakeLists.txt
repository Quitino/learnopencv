cmake_minimum_required(VERSION 2.8.12)

PROJECT(face_detection)
set (OpenCV_DIR  "/usr/local/opencv3.4.4/share/OpenCV")

find_package( OpenCV 3.4.4 REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS})

#include(./dlib/dlib/dlib/cmake)


set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/run)

#MACRO(add_example name)
#  ADD_EXECUTABLE(${name} src/${name}.cpp)
#  TARGET_LINK_LIBRARIES(${name} ${OpenCV_LIBS} dlib::dlib)
#ENDMACRO()

#add_example(face_detection_opencv_haar)
#add_example(face_detection_opencv_dnn)
#add_example(face_detection_dlib_hog)
#add_example(face_detection_dlib_mmod)
#add_example(run-all)


# Build tests
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/run)

add_executable(facialLandmarkDetection src/facialLandmarkDetection.cpp)
target_link_libraries(facialLandmarkDetection ${OpenCV_LIBS} )



