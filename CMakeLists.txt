
if(WIN32)
cmake_minimum_required (VERSION 3.6)
else()
cmake_minimum_required (VERSION 3.0)
endif()

project(math-rodriguesRotationFormula)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set (${PROJECT_NAME}._VERSION_MAJOR 1)
set (${PROJECT_NAME}._VERISON_MINOR 0)
set (${PROJECT_NAME}._VERSION_BUILD 0)

file(GLOB SOURCE_FILES "source/*.cpp")

source_group("source" FILES ${SOURCE_FILES})

add_executable(${PROJECT_NAME} ${SOURCE_FILES})

if (MSVC)
    execute_process(
        COMMAND ${CMAKE_COMMAND} -E tar xfz ${CMAKE_SOURCE_DIR}/lib/glm-0.9.7.1.zip
        WORKING_DIRECTORY ${CMAKE_BINARY_DIR}
    )

    include_directories(
        ${CMAKE_BINARY_DIR}/glm
    )
endif (MSVC)

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT ${PROJECT_NAME})
