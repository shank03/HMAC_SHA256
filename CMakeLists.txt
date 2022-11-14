cmake_minimum_required(VERSION 3.0.0)
project(HMAC_SHA256 VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)

add_library(HMAC_SHA256 hmac_sha256.h hmac_sha256.cpp)
