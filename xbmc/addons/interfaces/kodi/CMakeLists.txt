set(SOURCES General.cpp
            AudioEngine.cpp
            Filesystem.cpp
            Network.cpp)

set(HEADERS General.h
            AudioEngine.h
            Filesystem.h
            Network.h)

include_directories(${CORE_SOURCE_DIR}/xbmc/addons/kodi-addon-dev-kit/include)

core_add_library(addonInterface_kodi)

if(ENABLE_INTERNAL_FFMPEG)
  add_dependencies(addonInterface_kodi ffmpeg)
endif()
