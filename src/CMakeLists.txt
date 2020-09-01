set(TARGET_NAME roguelike)

find_package(Vulkan REQUIRED)

add_executable(${TARGET_NAME} main.cpp)

target_include_directories(${TARGET_NAME} PRIVATE ${Vulkan_INCLUDE_DIRS})

target_link_libraries(${TARGET_NAME}
    ${Vulkan_LIBRARIES}
    glfw)
