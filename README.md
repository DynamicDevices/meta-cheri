# meta-cheri
Layer adding support to OpenEmbedded/Yocto for Capability Hardware Enhanced RISC Instructions (CHERI)

## Getting Started

### Container
- Install [Docker](https://docs.docker.com/engine/install/ubuntu/)
- Clone [imx-docker](https://github.com/DynamicDevices/imx-docker) to get your build environment

### meta-clang
- Clone meta-clang into the root of your build environment. You can get meta-clang [here](https://github.com/kraj/meta-clang/tree/kirkstone)
- Follow the steps in the meta-clang README to configure the local.conf files and add meta-clang to to bblayers.conf

## Obtaining CHERI Clang/LLVM and LLD

- Obtain cheribuild: ```git clone https://github.com/CTSRD-CHERI/cheribuild.git```

- ```cd cheribuild```

- The following command line builds CheriBSD/RISC-V, QEMU-CHERI, and the complete toolchain including tools such as CHERI GDB, and runs the resulting image in QEMU: ```./cheribuild.py --include-dependencies run-riscv64-purecap```
