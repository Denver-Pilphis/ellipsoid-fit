
ellipsoid-fit
==============

Ellipsoid fitting in C++ using Eigen. Widely inspired by https://www.mathworks.com/matlabcentral/fileexchange/24693-ellipsoid-fit

This fork is a modification of the original repository for [CMake](https://github.com/Kitware/CMake) compilation of a shared library on Microsoft Windows using Microsoft Visual Studio with [vcpkg](https://github.com/microsoft/vcpkg) support. The license of this fork keeps the same as the original repository as **GNULGPL**. Please look at the [license.txt](./license.txt) file at the root of this repository for more details.

# Disclaimer

This library has the same problem as the original Matlab code: radii might not be in the correct order.

This is due to the algorithm relying on eigen values to compute them. These values are not guaranteed to be in any particular order by the algorithms computing them.

A new algorithm or a fix to this one needs to be found.

Installation and Usage
======================

The original **ellipsoid-fit** project is packaged using [PID](http://pid.lirmm.net), while this fork is using [vcpkg](https://github.com/microsoft/vcpkg) for Microsoft Visual Studio on Microsoft Windows. 

## Install Microsoft Visual Studio

Please visit the official website of [Microsoft Visual Studio](https://visualstudio.microsoft.com/) for information.

## Install and deploy vcpkg

Please follow the instructions on [vcpkg](https://github.com/microsoft/vcpkg) GitHub repository to install **vcpkg**.

It is suggested to add **vcpkg** installation directory to the system `PATH` environmental variable.

Make sure to integrate **vcpkg** with Microsoft Visual Studio:

> vcpkg integrate install

## Install Eigen version 3 on vcpkg

Use the following commands to install Eigen version 3: 

> vcpkg install eigen3

## Compilation

Clone this forked repository to a local directory.

Use Microsoft Visual Studio to open the local directory, open the `CMakeLists.txt`, configure the triplet and its corresponding settings, and then build.

A dynamic library will be built, along with a list of exported functions (the two fitting functions).

License
=======

The license that applies to the whole package content is **GNULGPL**. Please look at the [license.txt](./license.txt) file at the root of this repository for more details.

Authors
=======

**ellipsoid-fit** has been developed by the following authors: 
+ Benjamin Navarro (LIRMM)

Please contact Benjamin Navarro (navarro@lirmm.fr) - LIRMM for more information or questions.

Author for this fork (compilation on Windows):
+ Denver Pilphis (Di Peng)