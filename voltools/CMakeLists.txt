
SET(DGTAL_TOOLS_SRC
  volAddBorder
  volCComponentCounter
  vol2raw
  raw2vol
)

FOREACH(FILE ${DGTAL_TOOLS_SRC})
  add_executable(${FILE} ${FILE})
  target_link_libraries (${FILE} ${DGTAL_LIBRARIES})
  install(TARGETS ${FILE} 
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)
ENDFOREACH(FILE)
