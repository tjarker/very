
- Simulator Backend
    - chisel3.svsim
        - provides unified way to interact with simulators (supported ones)
    - arcilator
        - transpiles MLIR to LLVM
    - question how to use features like coverage, assertions?
    - how to monitor ports for functional coverage
    - should internal signals be peekable? (does svsim offer this? verilator does)
- Constrained Random
    - chiselverify has Jacop backend for this
    - interface is not nice
    - should be directly integrated with chisel bundles
        - each chisel bundle should magically have a .randomize method
- UVM
    - basic copying of reference and PyUVM implementation of spec
    - then we should consider where scala gives nicer options
        - is it OK to change some of the spec? PyUVM does so
    - my dream would be to take the concepts and structure of UVM and tailor the API to scala
- Interoperability with verification IP
    - PyUVM book mentions that one of the big hurdles to adoption is reuse of existing IP alongside newly developed
    - how can we do this?
        - somehow link compiled system verilog using JNA/JNI?
- Provide some form of standard library
    - PyUVM book also mentions that it is important to build up an ecosystem of OS verification components
    - AXI components could be a start
    - also provide infrastructure for chisel DecoupledIO
    - this could also be a chance to standardize interface bundles for common interfaces used across chisel community
