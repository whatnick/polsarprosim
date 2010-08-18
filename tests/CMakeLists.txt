PROJECT(PolsarProSimTests)

FILE(MAKE_DIRECTORY ${PolsarProSimTests_BINARY_DIR}/master)
FILE(MAKE_DIRECTORY ${PolsarProSimTests_BINARY_DIR}/slave)

MESSAGE(STATUS ${POLSARPROSIM_BINARY_DIR}/PolSARproSIM/Release/PolSARproSim)

EXECUTE_PROCESS(
	COMMAND ${POLSARPROSIM_BINARY_DIR}/PolSARproSIM/Release/PolSARproSim
	RESULT_VARIABLE pspsim_ret
	OUTPUT_VARIABLE pspsim_out
)

MESSAGE(STATUS "--------------")
MESSAGE(STATUS "pspsim_out=${pspsim_ret}")
MESSAGE(STATUS "pspsim_out=${pspsim_out}")
MESSAGE(STATUS "--------------")


ADD_TEST(compareOutput testCompareResult)
ADD_EXECUTABLE(testCompareResult testCompareResult)
