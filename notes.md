. <(curl https://aka.ms/vcpkg-init.sh -L)
git clone https://github.com/azure-rtos/getting-started --recursive
cd STMicroelectronics/B-L475E-IOT01A
~/.vcpkg/vcpkg activate
export ARM_GCC_PATH=~/.vcpkg/artifacts/aka_ms/vcpkg_ce_default/compilers.arm.gcc/2020.10.0/bin
cmake -Bbuild -GNinja -DCMAKE_TOOLCHAIN_FILE="../../cmake/arm-gcc-cortex-m4.cmake"
cmake --build build
