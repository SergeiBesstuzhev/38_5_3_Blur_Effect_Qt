cmake_minimum_required(VERSION 3.14)

project(38_5_3_Blur_Effect_Qt LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core Widgets)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core Widgets)

add_executable(38_5_3_Blur_Effect_Qt
  main.cpp
  window.h
  window.cpp
  window.ui
)
target_link_libraries(38_5_3_Blur_Effect_Qt
    Qt${QT_VERSION_MAJOR}::Core
    Qt${QT_VERSION_MAJOR}::Widgets
)

install(TARGETS 38_5_3_Blur_Effect_Qt
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
