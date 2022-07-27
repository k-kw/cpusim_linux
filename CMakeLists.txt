set(FFTW3_SO 
libfftw3.so
libfftw3.so.3
libfftw3.so.3.6.10
libfftw3_threads.so
libfftw3_threads.so.3
libfftw3_threads.so.3.6.10
)

cmake_minimum_required(VERSION 3.13)

project(cpusim CXX)

find_package(OpenCV REQUIRED)

include_directories(/usr/include ${OpenCV_INCLUDE_DIRS} /usr/local/fftw3/include /home/kawamoto/cprjct/cpusim/include)

link_directories(/home/kawamoto/cprjct/cpusim/sos /usr/local/lib /usr/local/fftw3/lib)

add_executable(cpusim main.cpp)

target_link_libraries(cpusim libbmp_class.so libcomplex_array_class.so ${OpenCV_LIBRARIES} ${FFTW3_SO})