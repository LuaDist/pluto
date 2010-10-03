# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(pluto C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
INCLUDE(dist.cmake)

# Build
INCLUDE_DIRECTORIES(.)

ADD_LUA_MODULE(pluto pluto.c pdep.c lzio.c)

# Test files
#ADD_EXECUTABLE (pptest  pptest.c)
#TARGET_LINK_LIBRARIES (pptest ${LUA_LIBRARIES})

#ADD_EXECUTABLE (puptest puptest.c)
#TARGET_LINK_LIBRARIES (puptest ${LUA_LIBRARIES})

# Install all files and documentation
INSTALL (TARGETS pluto DESTINATION ${INSTALL_CMOD})

INSTALL (FILES README THANKS CHANGELOG FILEFORMAT DESTINATION ${INSTALL_DATA})
INSTALL (FILES pptest.lua puptest.lua DESTINATION ${INSTALL_TEST})
#INSTALL (TARGETS pptest puptest DESTINATION ${INSTALL_BIN})

