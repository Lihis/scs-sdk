cmake_minimum_required(VERSION 3.7)
project(SCS_SDK VERSION 1.14)

set(SDK_SOURCES
    include/scs/scssdk.h
    include/scs/scssdk_input_device.h
    include/scs/scssdk_input_event.h
    include/scs/scssdk_input.h
    include/scs/scssdk_telemetry_channel.h
    include/scs/scssdk_telemetry_event.h
    include/scs/scssdk_telemetry.h
    include/scs/scssdk_value.h

    include/scs/common/scssdk_telemetry_common_channels.h
    include/scs/common/scssdk_telemetry_common_configs.h
    include/scs/common/scssdk_telemetry_common_gameplay_events.h
    include/scs/common/scssdk_telemetry_job_common_channels.h
    include/scs/common/scssdk_telemetry_trailer_common_channels.h
    include/scs/common/scssdk_telemetry_truck_common_channels.h

    include/scs/amtrucks/scssdk_ats.h
    include/scs/amtrucks/scssdk_input_ats.h
    include/scs/amtrucks/scssdk_telemetry_ats.h

    include/scs/eurotrucks2/scssdk_eut2.h
    include/scs/eurotrucks2/scssdk_input_eut2.h
    include/scs/eurotrucks2/scssdk_telemetry_eut2.h
    )

add_library(scssdk INTERFACE)
add_library(scs::sdk ALIAS scssdk)

target_include_directories(scssdk
                           INTERFACE
                           "${CMAKE_CURRENT_LIST_DIR}/include"
                           )
