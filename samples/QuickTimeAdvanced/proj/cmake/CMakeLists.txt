cmake_minimum_required( VERSION 3.0 FATAL_ERROR )
set( CMAKE_VERBOSE_MAKEFILE ON )

project( QuickTimeAdvanced )

get_filename_component( CINDER_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../../.." ABSOLUTE )
get_filename_component( APP_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../" ABSOLUTE )

include( "${CINDER_PATH}/proj/cmake/modules/cinderMakeApp.cmake" )

file(GLOB_RECURSE QTAdvanced_SRC "${APP_PATH}/src/*.*")

ci_make_app(
	SOURCES     ${QTAdvanced_SRC}
	CINDER_PATH ${CINDER_PATH}
)
