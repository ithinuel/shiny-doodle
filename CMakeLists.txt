cmake_minimum_required(VERSION 3.13)

project(demo)

add_subdirectory(mbed-os)


add_executable(app_k64f main.cpp)
target_link_libraries(app_k64f PRIVATE platform board_k64f)
# even though board_k64f depends on `board`, app_k64f needs to explicitely depend on `board` to have
# access to the header
target_link_libraries(app_k64f PRIVATE board)

add_executable(app_disco main.cpp)
target_link_libraries(app_disco PRIVATE platform )
target_link_libraries(app_disco PRIVATE board)
