cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(gw2formats)

#add_subdirectory(src)

include_directories(include)

set(CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAG}")


set(SOURCES
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

set(HEADERS
include/gw2formats/Language.h
include/gw2formats/StringsFile.h
include/gw2formats/TextureFile.h
include/gw2formats/base.h
include/gw2formats/fcc.h

include/gw2formats/bxml2/Bxml2Reader.h
include/gw2formats/bxml2/XmlAttribute.h
include/gw2formats/bxml2/XmlDocument.h
include/gw2formats/bxml2/XmlElement.h
include/gw2formats/bxml2/XmlWriter.h
include/gw2formats/pf/AnimSequencesPackFile.h
include/gw2formats/pf/AudioPackFile.h
include/gw2formats/pf/BankIndexPackFile.h
include/gw2formats/pf/BankPackFile.h
include/gw2formats/pf/ChunkFactory.h
include/gw2formats/pf/CollideModelManifestPackFile.h
include/gw2formats/pf/CompositePackFile.h
include/gw2formats/pf/ContentManifestPackFile.h
include/gw2formats/pf/EmoteAnimPackFile.h
include/gw2formats/pf/EulaPackFile.h
include/gw2formats/pf/HavokPackFile.h
include/gw2formats/pf/MapMetadataPackFile.h
include/gw2formats/pf/MapPackFile.h
include/gw2formats/pf/MapShadowPackFile.h
include/gw2formats/pf/MaterialPackFile.h
include/gw2formats/pf/ModelPackFile.h
include/gw2formats/pf/PackFile.h
include/gw2formats/pf/PagedImagePackFile.h
include/gw2formats/pf/PortalManifestPackFile.h
include/gw2formats/pf/ScenePackFile.h
include/gw2formats/pf/ScriptPackFile.h
include/gw2formats/pf/TextManifestPackFile.h
include/gw2formats/pf/TextVariantPackFile.h
include/gw2formats/pf/TextVoicePackFile.h

include/gw2formats/pf/helpers/Array.h
include/gw2formats/pf/helpers/FileName.h
include/gw2formats/pf/helpers/FileReference.h
include/gw2formats/pf/helpers/Ptr.h
include/gw2formats/pf/helpers/RefList.h
include/gw2formats/pf/helpers/String.h
include/gw2formats/pf/helpers/StringBase.h
include/gw2formats/pf/helpers/Vector.h
include/gw2formats/pf/helpers/WString.h
include/gw2formats/pf/helpers/read.h

include/gw2formats/pf/chunks/ABIX/BankIndexData.h
include/gw2formats/pf/chunks/ABNK/BankFileData.h
include/gw2formats/pf/chunks/AMAT/AmatDx9Material.h
include/gw2formats/pf/chunks/AMAT/AmatGr.h
include/gw2formats/pf/chunks/AMSP/ScriptFileData.h
include/gw2formats/pf/chunks/ASND/WaveformData.h
include/gw2formats/pf/chunks/CINP/SceneData.h
include/gw2formats/pf/chunks/MODL/ModelFileAnimation.h
include/gw2formats/pf/chunks/MODL/ModelFileData.h
include/gw2formats/pf/chunks/MODL/ModelFileGeometry.h
include/gw2formats/pf/chunks/MODL/ModelFileProperties.h
include/gw2formats/pf/chunks/MODL/ModelFileRootMotion.h
include/gw2formats/pf/chunks/MODL/ModelFileSkeleton.h
include/gw2formats/pf/chunks/MODL/common.h
include/gw2formats/pf/chunks/PIMG/PagedImageTableData.h
include/gw2formats/pf/chunks/anic/PackAnimSequences.h
include/gw2formats/pf/chunks/cmaC/CollideModelManifest.h
include/gw2formats/pf/chunks/cmpc/PackComposite.h
include/gw2formats/pf/chunks/cntc/PackContent.h
include/gw2formats/pf/chunks/emoc/PackEmoteAnimations.h
include/gw2formats/pf/chunks/eula/PackEula.h
include/gw2formats/pf/chunks/hvkC/PackMapCollide.h
include/gw2formats/pf/chunks/mMet/PackMapMetadata.h
include/gw2formats/pf/chunks/mapc/MapAudio.h
include/gw2formats/pf/chunks/mapc/MapMission.h
include/gw2formats/pf/chunks/mapc/MapParam.h
include/gw2formats/pf/chunks/mapc/MapShore.h
include/gw2formats/pf/chunks/mapc/MapSurfaces.h
include/gw2formats/pf/chunks/mapc/MapTerrainImg.h
include/gw2formats/pf/chunks/mapc/PackMapAreas.h
include/gw2formats/pf/chunks/mapc/PackMapCollide.h
include/gw2formats/pf/chunks/mapc/PackMapCubeMap.h
include/gw2formats/pf/chunks/mapc/PackMapDecals.h
include/gw2formats/pf/chunks/mapc/PackMapEnvironment.h
include/gw2formats/pf/chunks/mapc/PackMapLights.h
include/gw2formats/pf/chunks/mapc/PackMapProp.h
include/gw2formats/pf/chunks/mapc/PackMapRivers.h
include/gw2formats/pf/chunks/mapc/PackMapShadowExt.h
include/gw2formats/pf/chunks/mapc/PackMapTerrain.h
include/gw2formats/pf/chunks/mapc/PackMapZones.h
include/gw2formats/pf/chunks/mapc/common.h
include/gw2formats/pf/chunks/mpsd/PackMapShadow.h
include/gw2formats/pf/chunks/prlt/ContentPortalManifest.h
include/gw2formats/pf/chunks/txtV/TextPackVariants.h
include/gw2formats/pf/chunks/txtm/TextPackManifest.h
include/gw2formats/pf/chunks/txtv_/TextPackVoices.h
)

add_library(gw2formats SHARED ${SOURCES} ${HEADERS})

install(TARGETS gw2formats DESTINATION "lib")
install(DIRECTORY include DESTINATION "include")
