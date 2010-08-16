SET(CommonPolsarProSRCS 
Allometrics.c
Attenuation.c
Branch.c
Complex.c
Cone.c
Crown.c
Cylinder.c
Drawing.c
Facet.c
GraphicIMage.c
GrgCyl.c
Ground.c
InfCyl.c
JLkp.c
Jnz.c
Leaf.c
LightingMaterials.c
MonteCarlo.c
Perspective.c
Plane.c
PolSARproSim_Direct_Ground.c
PolSARproSim_Forest.c
PolSARproSim_Procedures.c
PolSARproSim_Progress.c
PolSARproSim_Short_Vegi.c
Ray.c
RayCrownIntersection.c
Realisation.c
SarIMage.c
Shuffling.c
Sinc.c
Spheroid.c
Tree.c
YLkp.c
c33Matrix.c
c3Vector.c
d33Matrix.c
d3Vector.c
soilsurface.c
)

SET(LIB_SRC ../lib/matrix.c ../lib/util.c)

SET(PPS_SRC PolsarProSim.c)
SET(PPS_FE_KZ_SRC PolSARproSim_FE_Kz.c)
SET(PPS_ImgSize_SRC PolSARproSim_ImgSize.c)
SET(PPS_ImgSizeSV_SRC PolSARproSimSV_ImgSize.c)
SET(PPS_ImgSizeGR_SRC PolSARproSimGR_ImgSize.c)

IF(WIN32)
ADD_DEFINITIONS(-D_CRT_SECURE_NO_WARNINGS)
ENDIF(WIN32)

ADD_EXECUTABLE(PolSARproSim ${CommonPolsarProSRCS} ${PPS_SRC})
ADD_EXECUTABLE(PolSARproSim_FE_Kz ${LIB_SRC} ${PPS_FE_KZ_SRC})
ADD_EXECUTABLE(PolSARproSim_ImgSize ${CommonPolsarProSRCS} ${PPS_ImgSize_SRC})
ADD_EXECUTABLE(PolSARproSimSV_ImgSize ${PPS_ImgSizeSV_SRC})
ADD_EXECUTABLE(PolSARproSimGR_ImgSize ${PPS_ImgSizeGR_SRC})