add_circt_dialect(Ibis ibis)
add_circt_dialect_doc(Ibis ibis)

set(LLVM_TARGET_DEFINITIONS IbisPasses.td)
mlir_tablegen(IbisPasses.h.inc -gen-pass-decls)
add_public_tablegen_target(CIRCTIbisTransformsIncGen)
add_circt_doc(IbisPasses IbisPasses -gen-pass-doc)
