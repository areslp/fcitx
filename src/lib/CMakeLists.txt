add_subdirectory(fcitx-config)
add_subdirectory(fcitx-utils)


if (_ENABLE_DBUS AND ENABLE_GLIB2)
    PKG_CHECK_MODULES(GIO2 "gio-2.0>=2.26")
    if (GIO2_FOUND)
        add_subdirectory(fcitx-gclient)
    endif (GIO2_FOUND)
endif (_ENABLE_DBUS AND ENABLE_GLIB2)
add_subdirectory(fcitx)
