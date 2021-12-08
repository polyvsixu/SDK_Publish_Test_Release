project(SDK_Publish_Demo)

add_executable(${PROJECT_NAME}
    demo.c
)
target_include_directories(${PROJECT_NAME} PRIVATE ${SDK_PUBLISH_INCLUDE_DIR})
target_link_libraries(${PROJECT_NAME} PRIVATE ${SDK_PUBLISH_LIB})

if(WIN32)
    add_custom_command(TARGET ${PROJECT_NAME} POST_BUILD
        COMMAND "${CMAKE_COMMAND}" -E copy_if_different
            ${SDK_PUBLISH_DLL}
            $<TARGET_FILE_DIR:${PROJECT_NAME}>
        VERBATIM)
endif()