cmake_minimum_required(VERSION 3.5)

project(ToDo)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Widgets)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Widgets)

set(PROJECT_SOURCES
        ./src/main.cpp
        ./src/forms/mainwindow.cpp
        ./src/forms/mainwindow.h
        ./src/forms/mainwindow.ui
)


add_executable(ToDo
    ${PROJECT_SOURCES}
)



target_link_libraries(ToDo PRIVATE Qt${QT_VERSION_MAJOR}::Widgets)
#install(TARGETS un3
#    BUNDLE DESTINATION .
#    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
