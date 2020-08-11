#
# project: fips-logc
#

if (NOT FIPS_IMPORT)
	cmake_minimum_required(VERSION 2.8)
	project(fips-logc)
	# include the fips main cmake file
	get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
	include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
	fips_setup()
	fips_project(fips-logc)
endif()

fips_begin_lib(logc)
	fips_files_ex(log.c/src/ *.c)
fips_end_lib()

if (NOT FIPS_IMPORT)
	fips_finish()
endif()
