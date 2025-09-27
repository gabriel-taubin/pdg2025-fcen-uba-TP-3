set(NAME core)

set(HEADERS
  Edges.hpp
  Faces.hpp
  Graph.hpp
  HalfEdges.hpp
  Partition.hpp
  PolygonMesh.hpp
  PolygonMeshTest.hpp
  Variable.hpp
) # HEADERS    

set(SOURCES
  Edges.cpp
  Faces.cpp
  Graph.cpp
  HalfEdges.cpp
  Partition.cpp
  PolygonMesh.cpp
  PolygonMeshTest.cpp
  Variable.cpp
) # SOURCES

add_library(${NAME}
    ${HEADERS}
    ${SOURCES}
    ${FORMS}
    ${ASSETS}
) # add_library

target_compile_features(${NAME} PRIVATE cxx_lambdas)

target_link_libraries(${NAME} ${LIB_LIST})


