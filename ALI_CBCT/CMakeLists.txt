cmake_minimum_required(VERSION 3.13.4)

project(ALI_CBCT)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/ALI_CBCT")
set(EXTENSION_CATEGORY "Landmark detection")
set(EXTENSION_CONTRIBUTORS "Maxime Gillot (UoM)")
set(EXTENSION_DESCRIPTION "Detection of landmarks using DeepLearning")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/ALI_CBCT.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/ALI_CBCT/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(ALI)
add_subdirectory(ALI_CLI)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
