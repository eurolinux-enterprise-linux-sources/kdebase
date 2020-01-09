project(kdebase)

#
#
# WARNING!
# 
# Existence of this file is mere convenience to developers! it is not part of KDE
# release. Adding anything here is almost always entirely wrong. Please add it
# to one of the subdirectories.
#
# If you don't understand this warning, contact release-team@kde.org
#
#

# search packages used by KDE
set(KDE_MIN_VERSION "4.2.95") # for the < 4.2 macro
find_package(KDE4 4.2.95 REQUIRED)
include (KDE4Defaults)
include (MacroLibrary)

macro_optional_add_subdirectory( runtime )

macro_optional_add_subdirectory( apps )

if ( NOT Q_WS_MAC )
   macro_optional_add_subdirectory( workspace )
endif ( NOT Q_WS_MAC )

macro_display_feature_log()
