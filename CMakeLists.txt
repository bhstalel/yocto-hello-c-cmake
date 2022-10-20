cmake_minimum_required(VERSION 3.16)

project(HelloCmake)

# Compile
add_executable(hello_cmake hello_cmake.c)

# Install
install(TARGETS hello_cmake DESTINATION /usr/bin)

option(WITH_SYSTEMD "Set to ON to install systemd service" OFF)

if(WITH_SYSTEMD)
	install(FILES ${PROJECT_SOURCE_DIR}/hello-cmake.service DESTINATION /etc/systemd/system)
endif(WITH_SYSTEMD)
