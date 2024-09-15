cmake_minimum_required(VERSION 3.10)

project(DesktopApp)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)


set(SFML_DIR "C:\\SFML-2.6.1\\lib\\cmake\\SFML")
find_package(SFML 2.6.1 COMPONENTS system window graphics REQUIRED)


add_executable(DesktopApp src/main.cpp)
link_directories("C:\\SFML-2.6.1\\lib")
target_link_libraries(DesktopApp
    sfml-system
    sfml-window
    sfml-graphics
)
target_include_directories(DesktopApp PRIVATE "C:\\SFML-2.6.1\\include")

