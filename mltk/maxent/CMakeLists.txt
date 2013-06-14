
SET(LIBRARY_OUTPUT_PATH ${MLTK_SOURCE_DIR}/lib)

SET(CMAKE_C_COMPILIER g++)

SET(SRC_LIST maxent.cc lbfgs.cc owlqn.cc sgd.cc)

INCLUDE_DIRECTORIES(${MLTK_SOURCE_DIR})

ADD_LIBRARY(maxent SHARED ${SRC_LIST})
SET_TARGET_PROPERTIES(maxent PROPERTIES CLEAN_DIRECT_OUTPUT 1)

ADD_LIBRARY(maxent_static STATIC ${SRC_LIST})
SET_TARGET_PROPERTIES(maxent_static PROPERTIES OUTPUT_NAME "maxent")
SET_TARGET_PROPERTIES(maxent_static PROPERTIES CLEAN_DIRECT_OUTPUT 1)
