SET( LIB_NAME OpenIG-Plugin-OSGEarthSimpleLighting )

ADD_LIBRARY( ${LIB_NAME} SHARED
    IGPluginOSGEarthSimpleLighting.cpp
)

TARGET_LINK_LIBRARIES( ${LIB_NAME}
    ${OSG_LIBRARIES}
    OpenIG-Engine
	${OSGEARTH_LIBRARY}
)

SET_TARGET_PROPERTIES( ${LIB_NAME} PROPERTIES VERSION ${OPENIG_VERSION} )
SET_TARGET_PROPERTIES( ${LIB_NAME} PROPERTIES SOVERSION ${OPENIG_VERSION} )
SET_TARGET_PROPERTIES( ${LIB_NAME} PROPERTIES PROJECT_LABEL "Plugin OSGEarthSimpleLighting" )

INCLUDE( PluginInstall REQUIRED )

