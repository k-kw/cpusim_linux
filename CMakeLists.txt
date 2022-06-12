set(OPENCV_SO 
libopencv_calib3d.so
libopencv_calib3d.so.4.6.0
libopencv_calib3d.so.406
libopencv_core.so
libopencv_core.so.4.6.0
libopencv_core.so.406
libopencv_dnn.so
libopencv_dnn.so.4.6.0
libopencv_dnn.so.406
libopencv_features2d.so
libopencv_features2d.so.4.6.0
libopencv_features2d.so.406
libopencv_flann.so
libopencv_flann.so.4.6.0
libopencv_flann.so.406
libopencv_gapi.so
libopencv_gapi.so.4.6.0
libopencv_gapi.so.406
libopencv_highgui.so
libopencv_highgui.so.4.6.0
libopencv_highgui.so.406
libopencv_imgcodecs.so
libopencv_imgcodecs.so.4.6.0
libopencv_imgcodecs.so.406
libopencv_imgproc.so
libopencv_imgproc.so.4.6.0
libopencv_imgproc.so.406
libopencv_ml.so
libopencv_ml.so.4.6.0
libopencv_ml.so.406
libopencv_objdetect.so
libopencv_objdetect.so.4.6.0
libopencv_objdetect.so.406
libopencv_photo.so
libopencv_photo.so.4.6.0
libopencv_photo.so.406
libopencv_stitching.so
libopencv_stitching.so.4.6.0
libopencv_stitching.so.406
libopencv_video.so
libopencv_video.so.4.6.0
libopencv_video.so.406
libopencv_videoio.so
libopencv_videoio.so.4.6.0
libopencv_videoio.so.406
)

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

include_directories(/usr/include /usr/local/include/opencv4 /usr/local/fftw3/include /home/kawamoto/cprjct/cpusim/include)

link_directories(/home/kawamoto/cprjct/cpusim/sos /usr/local/lib /usr/local/fftw3/lib)

add_executable(cpusim main.cpp)

target_link_libraries(cpusim libbmp_class.so libcomplex_array_class.so ${OPENCV_SO} ${FFTW3_SO})