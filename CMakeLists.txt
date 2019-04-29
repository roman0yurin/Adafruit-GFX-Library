cmake_minimum_required(VERSION 3.7)

PROJECT(AdafruitGFX C CXX ASM)

file(GLOB ADD_SRC
				${CMAKE_CURRENT_SOURCE_DIR}/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/*.c
				${CMAKE_CURRENT_SOURCE_DIR}/arduino/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/arduino/*.c
)
additionalSources("${ADD_SRC}")
additionalImport(${CMAKE_CURRENT_SOURCE_DIR})
configureModule()
