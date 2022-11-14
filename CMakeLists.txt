cmake_minimum_required(VERSION 3.0.0)
project(HMAC_SHA256 VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)

include_directories(HMAC_SHA256 include)
add_library(HMAC_SHA256 INTERFACE include/hmac_sha256.hpp)
