cmake_minimum_required(VERSION 2.8.9) 
project(TestLibrary) 
set(CMAKE_BUILD_TYPE release)

 
#For the shared library:
set(PROJECT_LINK_LIBS libtestStudent.so) 
link_directories(/home/josen/lib/)
 
#For the static library:
#set(PROJECT_LINK_LIBS libtestStudent.a) 
#link_directories(/home/josen/lib/)

include_directories(/home/josen/daily_practise_programs/15-June-2016/cmake-tutorials-5/include)

add_executable(libtest libtest.cpp)
target_link_libraries(libtest ${PROJECT_LINK_LIBS})
