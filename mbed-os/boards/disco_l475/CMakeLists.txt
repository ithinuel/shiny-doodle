add_library(board_disco_l475_iot01a)
target_sources(board_disco_l475_iot01a PRIVATE disco.cpp)
target_link_libraries(board_disco_l475_iot01a PRIVATE mcu board)

set_target_properties(board_disco_l475_iot01a PROPERTIES COMPILE_FLAGS "--save-temps")

