# Yolo_mark
**Windows** & **Linux** GUI for marking bounded boxes of objects in images for training Yolo v3 and v2

* To compile on **Linux** type in console 3 commands:
    ```
    cmake .
    make
    ./linux_mark.sh
    ```
* if cmake not installed install cmake as:
  ```
  sudo apt-get install cmake
  ```
* if compile error no opencv, install OpenCV
  ```
  sudo apt-get install libopencv-dev
  ```
* if compile error no highgui.hpp
  ```
  sudo apt-get install libopencv-highgui-dev
  ```
* if error highgui persists then change line in main.cpp as
  ```
  opencv2/highgui/highgui.hpp
  ```
Supported both: OpenCV 2.x and OpenCV 3.x

--------

1. To test, simply run
  * **on Linux:** `./linux_mark.sh`

2. To use for labeling your custom images:

 * delete all files from directory `x64/Release/data/img`
 * put your `.jpg`-images to this directory `x64/Release/data/img`
 * run file: `./linux_mark.sh`

 PS: for missing highgui.hpp file following solved the problem
 * search for the file in apt-cache as:
 ```
 apt-file search highgui.hpp
 ```
 * installed the package which had highgui ie. ```libopencv-highguid-dev```
 * finally changed main.cpp to indicate the path of highgui-dev
 ```
 from opencv2/highgui.hpp to
 opencv2/highgui/highgui.hpp
 ```
