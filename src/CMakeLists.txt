cmake_minimum_required(VERSION 2.8)

find_package(PythonLibs)
find_package(Boost COMPONENTS python REQUIRED)
include_directories(${Boost_INCLUDE_DIRS} ${PYTHON_INCLUDE_DIRS} include)

LINK_LIBRARIES(${Boost_LIBRARIES} ${PYTHON_LIBRARIES})
PYTHON_ADD_MODULE(hello SHARED HW.cpp)