# TODO: Make the check source feature optional as an argument on *_add_library.
set(LLVM_OPTIONAL_SOURCES
  CHIRRTL.cpp
  Comb.cpp
  Debug.cpp
  ESI.cpp
  FIRRTL.cpp
  FSM.cpp
  HW.cpp
  HWArith.cpp
  Handshake.cpp
  LLHD.cpp
  LTL.cpp
  MSFT.cpp
  Moore.cpp
  OM.cpp
  SV.cpp
  Seq.cpp
  Verif.cpp
)

add_mlir_public_c_api_library(CIRCTCAPIComb
  Comb.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTComb
)

add_mlir_public_c_api_library(CIRCTCAPIDebug
  Debug.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTDebug
)

add_mlir_public_c_api_library(CIRCTCAPIESI
  ESI.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTESI
)

add_mlir_public_c_api_library(CIRCTCAPIFIRRTL
  FIRRTL.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTFIRRTL
)

add_mlir_public_c_api_library(CIRCTCAPICHIRRTL
  CHIRRTL.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTFIRRTL
)

add_mlir_public_c_api_library(CIRCTCAPIMSFT
  MSFT.cpp

  DEPENDS
  MLIRTransforms

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  MLIRTransforms
  CIRCTMSFT
  CIRCTMSFTTransforms
)

add_mlir_public_c_api_library(CIRCTCAPIHW
  HW.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTHW
)

add_mlir_public_c_api_library(CIRCTCAPILLHD
  LLHD.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTLLHD
)

add_mlir_public_c_api_library(CIRCTCAPIMoore
  Moore.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTMoore
)

add_mlir_public_c_api_library(CIRCTCAPIOM
  OM.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTOM
  CIRCTOMEvaluator
)

add_mlir_public_c_api_library(CIRCTCAPISeq
  Seq.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTSeq
  CIRCTSeqTransforms
)

add_mlir_public_c_api_library(CIRCTCAPISV
  SV.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTSV
  CIRCTSVTransforms
)

add_mlir_public_c_api_library(CIRCTCAPIFSM
  FSM.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTFSM
  CIRCTFSMTransforms
  CIRCTFSMToSV
)

add_mlir_public_c_api_library(CIRCTCAPIHandshake
  Handshake.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTHandshake
  CIRCTHandshakeTransforms
  CIRCTHandshakeToHW
  CIRCTCFToHandshake
)

add_mlir_public_c_api_library(CIRCTCAPIHWArith
  HWArith.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTHWArith
  CIRCTHWArithToHW
)

add_mlir_public_c_api_library(CIRCTCAPIVerif
  Verif.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTVerif
  CIRCTVerifToSV
)

add_mlir_public_c_api_library(CIRCTCAPILTL
  LTL.cpp

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTLTL
)
