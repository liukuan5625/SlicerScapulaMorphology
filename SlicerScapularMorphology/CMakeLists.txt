cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(ScapulaMorphology)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/ScapulaMorphology")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Kuan Liu (Ruijin Hospital, Shanghai Jiaotong University School of Medicine)")
set(EXTENSION_DESCRIPTION "Scapula Morphology for glenoid segmentation and landmarks location.")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/ScapulaMorphology.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/ScapulaMorphology/Screenshots/1.png")
set(EXTENSION_DEPENDS "PyTorch")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(ScapulaMorphology)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
