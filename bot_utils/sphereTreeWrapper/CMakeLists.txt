set(BOT_LIB_NAME sphereTreeWrapper)
file(GLOB_RECURSE LibSource src/*.cpp)

add_library(${BOT_LIB_NAME} ${COMPILE_TYPE}
        ${LibSource}
)
set_target_properties(${BOT_LIB_NAME} PROPERTIES VERSION "${${PROJECT_NAME}_VERSION}")

target_link_libraries(${BOT_LIB_NAME} STG yaml-cpp)

set_target_properties(${BOT_LIB_NAME} PROPERTIES VERSION ${PROJECT_VERSION} SOVERSION ${PROJECT_SO_VERSION})
