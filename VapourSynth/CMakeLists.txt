project(Anime4KCPP_VapourSynth LANGUAGES CXX)

if(Build_VapourSynth_plugin)

    aux_source_directory(src SOURCE)
    aux_source_directory(../Anime4KCore/src Anime4KCPPCoreSource)

    include_directories(../Anime4KCore/include)

    add_compile_definitions(BUILT_IN_KERNEL PARALLEL_SUPPORTS)

    add_library(${PROJECT_NAME} SHARED ${SOURCE} ${Anime4KCPPCoreSource})

    include(../cmake/ThirdPartyForVS.cmake)

endif()
