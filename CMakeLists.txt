cmake_minimum_required(VERSION 3.16.3)

project(cmake)



include(FetchContent)


FetchContent_Declare(
    platform
    GIT_REPOSITORY     https://github.com/Renuprakash24/fetch_content.git    
    GIT_TAG   main
    CONFIGURE_COMMAND   ""
    BUILD_COMMAND       ""
    
)
FetchContent_Declare(
    platform2
    GIT_REPOSITORY     https://github.com/Renuprakash24/poco_repo.git
    GIT_TAG   main
    CONFIGURE_COMMAND   ""
    BUILD_COMMAND       ""
    
)

FetchContent_MakeAvailable(platform platform2)

add_executable(${PROJECT_NAME} /platform-src/include/Can_main.cpp)

target_link_libraries(${PROJECT_NAME} platform platform2)

