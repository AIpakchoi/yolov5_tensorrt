# yolov5_tensorrt
This is the implementation that supports the version 1.0 of yolov5s, yolov5m, yolov5l and yolov5x.\
The Pytorch implementation of yolov5 version 1.0 is provided in this repos.\
The latest ultralytics/yolov5 version 2.0 of https://github.com/ultralytics/yolov5 is not supported \
You can see source code of yolov5s on https://github.com/wang-xinyu/tensorrtx/tree/master/yolov5
You can see source code of Pytorch implementatuon of ultralytics/yolov5(version 1.0) on https://github.com/ultralytics/yolov5/releases/tag/v1.0

# Test Environment
1. GTX1080 / Ubuntu16.04 or GTX2080Ti / Ubuntu18.04 
2. cuda >= 10.0 , cudnn >= 7.0.0 , tensorrt7.0.0, nvinfer7.0.0, opencv3.3(I use opencv3.4)

# How to Run
You should check the compile environment in the CMakeLists.txt for each folder(yolov5s,yolov5m,yolov5l,yolov5x).\
Each folder has a readme inside, which explains how to run the models inside.\
You can download pt files of ultralytics/yolov5(s,m,l,x)(version 1.0) on [BaiduCloud](https://pan.baidu.com/s/1uFc8CNCINV1F4ta-PlcAGw), passwd:9cw1 \
Or you can download pt files of ultralytics/yolov5(s,m,l,x)(version 1.0) on https://github.com/ultralytics/yolov5/releases/tag/v1.0
Now, this repos only support yolov5 version 1.0. 


# Acknowledgments
Thanks to [wang-xinyu](https://github.com/wang-xinyu/tensorrtx) for his great works and repos.
