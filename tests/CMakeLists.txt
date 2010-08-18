PROJECT(PolsarProSimTests)

FILE(MAKE_DIRECTORY ${PolsarProSimTests_BINARY_DIR}/master)
FILE(MAKE_DIRECTORY ${PolsarProSimTests_BINARY_DIR}/slave)

ADD_TEST(compareOutput testCompareResult)
ADD_EXECUTABLE(testCompareResult testCompareResult)
