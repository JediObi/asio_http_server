cmake_minimum_required(VERSION 3.10)
project(asio_http)

set(CMAKE_CXX_STANDARD 11)

file(GLOB server_srcs ./*.cpp)

add_executable(asio_http2 ${server_srcs})
target_link_libraries(asio_http2
        boost_system
        pthread)