cmake_minimum_required(VERSION 3.16)

project(HelloCmake)

# Compile
add_executable(hello_cmake hello_cmake.c)

# Install
install(TARGETS hello_cmake DESTINATION /usr/bin)
install(FILES ${PROJECT_BINARY_DIR}/hello-cmake.service DESTINATION /etc/systemd/system)