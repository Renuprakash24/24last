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


FetchContent_GetProperties(platform)
if(NOT depname_POPULATED)

  FetchContent_Populate(platform)
endif()
 
 FetchContent_GetProperties(platform2)
if(NOT depname_POPULATED)

  FetchContent_Populate(platform2)
endif()
