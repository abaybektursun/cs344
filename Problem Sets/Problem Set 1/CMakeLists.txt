############################################################################
# <summary> CMakeLists.txt for OpenCV and CUDA. </summary>
# <date>    2012-02-07          </date>
# <author>  Quan Tran Minh. edit by Johannes Kast, Michael Sarahan </author>
# <email>   quantm@unist.ac.kr  kast.jo@googlemail.com msarahan@gmail.com</email>
############################################################################

# collect source files

# Updated by Abay Bektursun for modern CUDA and CMake
cmake_minimum_required(VERSION 3.18)
project(HW1 LANGUAGES CXX CUDA)

# Collect source files
file(GLOB hdr *.hpp *.h)
file(GLOB cu  *.cu)
set(HW1_files main.cpp reference_calc.cpp compare.cpp ${cu})

# Create executable
add_executable(HW1 ${HW1_files} ${hdr})
