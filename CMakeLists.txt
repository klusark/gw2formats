cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(gw2formats)

#add_subdirectory(src)

include_directories(include)

set(CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAG}")

add_library(gw2formats

src/StringsFile.cpp
src/TextureFile.cpp

src/bxml2/Bxml2Reader.cpp
src/bxml2/XmlAttribute.cpp
src/bxml2/XmlDocument.cpp
src/bxml2/XmlElement.cpp
src/bxml2/XmlWriter.cpp

src/pf/helpers/FileName.cpp
src/pf/helpers/FileReference.cpp

src/pf/chunks/ABIX/BankIndexData.cpp
src/pf/chunks/ABNK/BankFileData.cpp
src/pf/chunks/AMAT/AmatDx9Material.cpp
src/pf/chunks/AMAT/AmatGr.cpp
src/pf/chunks/AMSP/ScriptFileData.cpp
src/pf/chunks/ASND/WaveformData.cpp
src/pf/chunks/CINP/SceneData.cpp
src/pf/chunks/MODL/ModelFileAnimation.cpp
src/pf/chunks/MODL/ModelFileData.cpp
src/pf/chunks/MODL/ModelFileGeometry.cpp
src/pf/chunks/MODL/ModelFileProperties.cpp
src/pf/chunks/MODL/ModelFileRootMotion.cpp
src/pf/chunks/MODL/ModelFileSkeleton.cpp
src/pf/chunks/MODL/common.cpp
src/pf/chunks/PIMG/PagedImageTableData.cpp
src/pf/chunks/anic/PackAnimSequences.cpp
src/pf/chunks/cmaC/CollideModelManifest.cpp
src/pf/chunks/cmpc/PackComposite.cpp
src/pf/chunks/cntc/PackContent.cpp
src/pf/chunks/emoc/PackEmoteAnimations.cpp
src/pf/chunks/eula/PackEula.cpp
src/pf/chunks/hvkC/PackMapCollide.cpp
src/pf/chunks/mMet/PackMapMetadata.cpp
src/pf/chunks/mapc/MapAudio.cpp
src/pf/chunks/mapc/MapMission.cpp
src/pf/chunks/mapc/MapParam.cpp
src/pf/chunks/mapc/MapShore.cpp
src/pf/chunks/mapc/MapSurfaces.cpp
src/pf/chunks/mapc/MapTerrainImg.cpp
src/pf/chunks/mapc/PackMapAreas.cpp
src/pf/chunks/mapc/PackMapCubeMap.cpp
src/pf/chunks/mapc/PackMapDecals.cpp
src/pf/chunks/mapc/PackMapEnvironment.cpp
src/pf/chunks/mapc/PackMapLights.cpp
src/pf/chunks/mapc/PackMapProp.cpp
src/pf/chunks/mapc/PackMapRivers.cpp
src/pf/chunks/mapc/PackMapShadowExt.cpp
src/pf/chunks/mapc/PackMapTerrain.cpp
src/pf/chunks/mapc/PackMapZones.cpp
src/pf/chunks/mapc/common.cpp
src/pf/chunks/mpsd/PackMapShadow.cpp
src/pf/chunks/prlt/ContentPortalManifest.cpp
src/pf/chunks/txtV/TextPackVariants.cpp
src/pf/chunks/txtm/TextPackManifest.cpp
src/pf/chunks/txtv_/TextPackVoices.cpp

)
#target_link_libraries
