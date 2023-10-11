cmake_minimum_required(VERSION 2.6)

PROJECT(Bezier0)

SET(VTK_DIR /media/heaven7/h7/med_bak/IAS/vtk-9.2.6/_install_R/lib/cmake/vtk-9.2)

FIND_PACKAGE(VTK REQUIRED)
INCLUDE(${VTK_USE_FILE})

ADD_EXECUTABLE(BezierSource Example_Source.cxx vtkBezierSurfaceSource.cxx)
TARGET_LINK_LIBRARIES(BezierSource ${VTK_LIBRARIES})

ADD_EXECUTABLE(BezierSourceWidget Example_Source_Widget.cxx vtkBezierSurfaceWidget.cxx vtkBezierSurfaceSource.cxx)
TARGET_LINK_LIBRARIES(BezierSourceWidget ${VTK_LIBRARIES})
