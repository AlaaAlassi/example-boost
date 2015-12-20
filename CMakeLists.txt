PROJECT(MyRegex)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

INCLUDE(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
CONAN_BASIC_SETUP()

# Just comment or uncomment the FindPackage line to use it or not
FIND_PACKAGE(Boost 1.60.0 COMPONENTS regex)
IF(Boost_FOUND)
	INCLUDE_DIRECTORIES(${Boost_INCLUDE_DIRS})
	ADD_EXECUTABLE(regex main.cpp)
	TARGET_LINK_LIBRARIES(regex ${Boost_LIBRARIES})
ELSE()
	ADD_EXECUTABLE(regex main.cpp)
	TARGET_LINK_LIBRARIES(regex ${CONAN_LIBS})
ENDIF()