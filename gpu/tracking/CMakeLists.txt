set(SUBSYS_NAME gpu_tracking)
set(SUBSYS_PATH gpu/tracking)
set(SUBSYS_DESC "Tracking with GPU")
set(SUBSYS_DEPS common gpu_containers gpu_utils gpu_octree tracking search kdtree filters octree)

set(build FALSE)
PCL_SUBSYS_OPTION(build "${SUBSYS_NAME}" "${SUBSYS_DESC}" OFF)
PCL_SUBSYS_DEPEND(build "${SUBSYS_NAME}" DEPS ${SUBSYS_DEPS})
PCL_SET_SUBSYS_INCLUDE_DIR("${SUBSYS_NAME}" "${SUBSYS_PATH}")
mark_as_advanced("BUILD_${SUBSYS_NAME}")
