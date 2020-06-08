cmake_minimum_required(VERSION 3.10)
project(banking)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(account STATIC banking/Account.cpp)
target_include_directories(account
 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/banking)

add_library(transaction STATIC banking/Transaction.cpp)
target_include_directories(account
 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/banking)
 target_link_libraries(transaction account)
