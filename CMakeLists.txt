cmake_minimum_required(VERSION 3.26)
project(TicTacToe C)

set(CMAKE_C_STANDARD 11)

# Source files
set(SOURCE_FILES tictactoe.c)  # Include all your source files here
set(TEST_FILES tests.c)

# Executable for main program
add_executable(main_program ${SOURCE_FILES})

# Executable for unit tests
add_executable(unit_tests ${TEST_FILES} ${SOURCE_FILES})

include_directories(/opt/homebrew/Cellar/cunit/2.1-3/include)

link_directories(/opt/homebrew/Cellar/cunit/2.1-3/lib)
target_link_libraries(unit_tests cunit)
