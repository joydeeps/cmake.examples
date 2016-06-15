cmake_minimum_required(VERSION 2.8.9) 
project(directory_test) 
set(CMAKE_BUILD_TYPE release)

 
#Bring the headers, such as Student.h into the project 
include_directories(include) 

 
#Can manually add the sources using the set command as follows: 
#set(SOURCES src/mainapp.cpp src/Student.cpp) 

 
#However, the file(GLOB...) allows for wildcard additions: 
file(GLOB SOURCES "src/*.cpp") 

#Generate the shared library from the sources
add_library(testStudent STATIC ${SOURCES})

#Set the location for library installation -- i.e., /usr/lib in this case 
#not really necessarily in this example. Use "sudo make install" to apply
#install(TARGETS testStudent DESTINATION /usr/lib/)
install(TARGETS testStudent DESTINATION /home/josen/lib/)
