SET(master_dir ${PolsarProSimTests_BINARY_DIR}/master)
SET(slave_dir ${PolsarProSimTests_BINARY_DIR}/slave)
SET(prefix_path ${POLSARPROSIM_SOURCE_DIR}/track_master/pspsim_config)

FILE(MAKE_DIRECTORY ${master_dir})
PROJECT(POLSARPROSIMTests)

FILE(MAKE_DIRECTORY ${slave_dir})

MESSAGE(STATUS "--------------")
MESSAGE(STATUS "master_dir=${master_dir}")
MESSAGE(STATUS "slave_dir=${slave_dir}")
MESSAGE(STATUS "prefix_path=${prefix_path}")
MESSAGE(STATUS "--------------")

#EXECUTE_PROCESS(
#	COMMAND ${POLSARPROSIM_BINARY_DIR}/PolSARproSIM/Release/PolSARproSim ${prefix_path} ${master_dir} ${slave_dir}
#	RESULT_VARIABLE pspsim_ret
#	OUTPUT_VARIABLE pspsim_out
#)

#MESSAGE(STATUS "--------------")
#MESSAGE(STATUS "pspsim_ret=${pspsim_ret}")
#MESSAGE(STATUS "pspsim_out=${pspsim_out}")
#MESSAGE(STATUS "--------------")

ADD_EXECUTABLE(testCompareResult testCompareResult)

ADD_TEST(compareOutput testCompareResult)
#ADD_TEST(runSim PolSARproSim ${prefix_path} ${master_dir} ${slave_dir})

