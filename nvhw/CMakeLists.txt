project(ENVYTOOLS C)
cmake_minimum_required(VERSION 2.6)

add_library(nvhw chipset.c tile.c comp.c mpeg_crypt.c
	pgraph_class.c pgraph_grobj.c
	pgraph.c pgraph_xy.c pgraph_xy3.c pgraph_xy4.c pgraph_d3d_nv3.c
	pgraph_idx.c
	pgraph_celsius.c pgraph_celsius_xfrm.c pgraph_kelvin.c
	fp.c sfu.c sfu_tab.c)

target_link_libraries(nvhw cgen)

install(TARGETS nvhw
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib${LIB_SUFFIX}
	ARCHIVE DESTINATION lib${LIB_SUFFIX})
