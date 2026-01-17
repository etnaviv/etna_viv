cmake_minimum_required(VERSION 3.18)
project(ENVYTOOLS C)

add_library(envyutil
	path.c mask.c hash.c symtab.c colors.c yy.c astr.c aprintf.c
	vardata.c varinfo.c varselect.c
)

install(TARGETS envyutil
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib${LIB_SUFFIX}
	ARCHIVE DESTINATION lib${LIB_SUFFIX})
