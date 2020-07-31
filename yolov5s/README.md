# yolov5

The Pytorch implementation is of yolov5 is provided in this repos. Please do not use the latest version 2.0 of [ultralytics/yolov5](https://github.com/ultralytics/yolov5).\
I was using [ultralytics/yolov5](https://github.com/ultralytics/yolov5)(Commits on July 05, 2020). Just in case the yolov5 model updated.\
You can download pt files of ultralytics/yolov5(version 1.0 ) on [Baidu](https://pan.baidu.com/s/1uFc8CNCINV1F4ta-PlcAGw),extraction code is 9cw1

## How to Run

```
1. generate yolov5m.wts from pytorch implementation with yolov5.pt

git clone https://github.com/AIpakchoi/yolov5_tensorrt.git

// download its weights 'yolov5s.pt'
cd yolov5
cp ../yolov5_tensorrt/yolov5s/gen_wts.py .
python gen_wts.py
// a file 'yolov5s.wts' will be generated.

2. put yolov5s.wts into yolov5s, build and run

mv yolov5s.wts ../yolov5_tensorrt/yolov5s/
cd ../yolov5_tensorrt/yolov5s
mkdir build
cd build
cmake ..
make
sudo ./yolov5s -s             // serialize model to plan file i.e. 'yolov5s.engine'
sudo ./yolov5s -d  ../samples // deserialize plan file and run inference, the images in samples will be processed.

3. check the images generated, as follows. _zidane.jpg and _bus.jpg
```

<p align="center">
<img src="https://user-images.githubusercontent.com/15235574/78247927-4d9fac00-751e-11ea-8b1b-704a0aeb3fcf.jpg">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/15235574/78247970-60b27c00-751e-11ea-88df-41473fed4823.jpg">
</p>

## Config

- Input shape defined in yololayer.h
- Number of classes defined in yololayer.h
- FP16/FP32 can be selected by the macro in yolov5s.cpp
- GPU id can be selected by the macro in yolov5s.cpp
- NMS thresh in yolov5s.cpp
- BBox confidence thresh in yolov5s.cpp
- Batch size in yolov5s.cpp
