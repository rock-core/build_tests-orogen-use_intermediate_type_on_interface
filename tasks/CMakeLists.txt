# Generated from orogen/lib/orogen/templates/tasks/CMakeLists.txt

include(use_intermediate_type_on_interfaceTaskLib)
ADD_LIBRARY(${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_NAME} SHARED 
    ${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_SOURCES})
add_dependencies(${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_NAME}
    regen-typekit)



TARGET_LINK_LIBRARIES(${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_NAME}
    ${OrocosRTT_LIBRARIES}
    ${QT_LIBRARIES}
    ${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_DEPENDENT_LIBRARIES})
SET_TARGET_PROPERTIES(${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_NAME}
    PROPERTIES LINK_INTERFACE_LIBRARIES "${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_INTERFACE_LIBRARIES}")
SET_TARGET_PROPERTIES(${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_NAME}
    PROPERTIES INTERFACE_LINK_LIBRARIES "${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_INTERFACE_LIBRARIES}")

INSTALL(TARGETS ${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_NAME}
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib/orocos)

INSTALL(FILES ${USE_INTERMEDIATE_TYPE_ON_INTERFACE_TASKLIB_HEADERS}
    DESTINATION include/orocos/use_intermediate_type_on_interface)

