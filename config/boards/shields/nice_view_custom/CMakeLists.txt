if(CONFIG_ZMK_DISPLAY AND CONFIG_NICE_VIEW_WIDGET_STATUS)
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/boards/shields/nice_view/widgets)

  set_source_files_properties(
    ${APPLICATION_SOURCE_DIR}/boards/shields/nice_view/widgets/status.c
    TARGET_DIRECTORY zephyr
    PROPERTIES HEADER_FILE_ONLY ON)
 
  zephyr_library_sources(widgets/status.c)
endif()
