PROJECT(POLSARPROSIMTests)

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

