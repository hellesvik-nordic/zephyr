# SPDX-License-Identifier: Apache-2.0
# Copyright (c) 2024 Silicon Laboratories Inc.

if(CONFIG_WIFI_SILABS_SIWX91X)
  zephyr_library_sources(
    siwx91x_wifi.c
    siwx91x_wifi_ap.c
    siwx91x_wifi_sta.c
    siwx91x_wifi_scan.c
    siwx91x_wifi_ps.c)

  if(CONFIG_WIFI_SILABS_SIWX91X_NET_STACK_OFFLOAD)
    zephyr_library_sources(siwx91x_wifi_socket.c)
  endif()
endif()
