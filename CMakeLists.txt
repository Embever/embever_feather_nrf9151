# Copyright (c) 2024 Circuit Dojo
# Copyright (c) 2025 Embever GmbH
# SPDX-License-Identifier: Apache-2.0

zephyr_library()
zephyr_library_sources_ifdef(CONFIG_EMBEVER_FEATHER_NRF9151_PMIC_STARTUP startup.c)

if (CONFIG_EMBEVER_FEATHER_NRF9151_STATIC_PARTITIONS_FACTORY)
set(PM_STATIC_YML_FILE ${CMAKE_CURRENT_LIST_DIR}/embever_feather_nrf9151_pm_static.yml CACHE INTERNAL "")
endif()