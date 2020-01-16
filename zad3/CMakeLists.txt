cmake_minimum_required(VERSION 3.5)

project(zad3)
#file(GLOB SOURCES "src/*.cpp")
include_directories(include)

add_library(testStudent STATIC "src/Student.cpp")
install(TARGETS testStudent DESTINATION "/home/jackie/Pulpit/kolokwium/zad3/lib")

set(PROJECT_LINK_LIBS libtestStudent.a)
link_directories("/home/jackie/Pulpit/kolokwium/zad3/build")

add_executable(myProgram "src/libtest.cpp")
install(TARGETS myProgram DESTINATION "/home/jackie/Pulpit/kolokwium/zad3/bin")
target_link_libraries(myProgram ${PROJECT_LINK_LIBS})

