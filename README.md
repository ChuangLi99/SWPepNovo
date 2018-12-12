# SWPepNovo
SWPepNovo: An Efficient De Novo Peptide Sequencing Tool for Large-scale MS/MS Spectra Analysis

Introduction： As the number of the MS/MS spectra increases rapidly, the excessive computation time taken by MS/MS spectra data analysis has become a critical concern in computational biology. In this work, we designed and implemented SWPepNovo, an efficient de novo peptide sequencing tool for large-scale MS/MS spectra data analysis using a novel peptide-spectrum matches (PSMs) algorithm. To achieve the high performance, we designed an improved scoring algorithm to reduce the time complexity and eliminate the data dependence to enable all possible locality and vectorizations. Performance is also tuned by pre-fetching, double buffering mechanism, and an optimized memory access scheme, to achieve an optimum performance and best utilization of various computing resources within neo-heterogeneous many-core architecture.

SWPepNovo is a C++ program designed to accelerate large-scale de novo peptide sequencing . We assume that reader is familiar with C++ to some extent and is able to run C++ programs.

Installation and Requirements

CPU | SW2610 processor

Processor Node | 4 CGs (4 MPEs and 256 CPEs)

OS | Sunway Raise OS 2.0.5 (based on Linux)

Instruction | Sunway-64 Instruction Set

Compile language | C, C++, Fortran

Parallel programming interface | MPI 3.0, OpenMP 3.1, OpenACC 2.0

Usage: eg: bsub –I –b –q queue_name –n 1 –cgsp 64 –share_size 4096 –host_stack 128 ./SWPepNovo input-path output-path ...
