# OneFlow IR

OneFlow IR, a MLIR dialect

## Code style

Inevitably, developers maintaining OneFlow IR would face these challenges:
- Debugging components related to IR, compiler could be complicated and puzzling.
- IR subsystems should follow latest changes of OneFlow and MLIR closely.

To address these problems,
within the IR source code directory,
there are some rules must be enforced for all the optimizers, importers, exporters, runners:
- separate library, include, target
- MLIR-releted code should follow the style and paradigm of MLIR and LLVM closely
- ensure every component could be independently compiled and tested
    - there should be one `CMakeLists.txt` in every sub-directory
    - don't link anything from OneFlow unless it is necessary for the feature
