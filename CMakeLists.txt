cmake_minimum_required(VERSION 3.7)

PROJECT(AdafruitGFX C CXX ASM)

file(GLOB ADD_SRC
				${CMAKE_CURRENT_SOURCE_DIR}/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/*.c
				${CMAKE_CURRENT_SOURCE_DIR}/arduino/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/arduino/*.c
)
SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wno-strict-aliasing -fno-exceptions -frtti")
additionalSources("${ADD_SRC}")
additionalImport(${CMAKE_CURRENT_SOURCE_DIR})
addSubmodule(../../micro/kernel/mcore)

configureModule()
