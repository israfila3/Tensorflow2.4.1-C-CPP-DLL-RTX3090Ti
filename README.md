# Tensorflow2.4.1-C-CPP-DLL-RTX3090Ti

Basic Requirements

![image](https://user-images.githubusercontent.com/20577227/114127659-9c540300-9935-11eb-83ca-20cf7a83fc27.png)


#CUDA

 Install CUDA 11.0 and download CuDNN (https://developer.nvidia.com/cudnn). After downloading copy all the files to CUDA installed location. 
 Install Bazel 3.1.0 “https://github.com/bazelbuild/bazel/releases/tag/3.1.0”
 
Download “bazel-3.1.0-windows-x86_64.exe”

Make Bazel folder and copy the “exe” file and rename it as “bazel.exe”

Add “bazel.exe” to the system path. Environment variable Path “C:\bazel”

Setting environment variable(System variable)
BAZEL_VC(Variable name): C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC
BAZEL_VS(Variable name): C:\Program Files (x86)\Microsoft Visual Studio\2019\Community
BAZEL_SH(Variable name): C:\msys64\usr\bin\bash.exe

Download Tensorflow r2.4 from "https://github.com/tensorflow/tensorflow/tree/r2.4"
Unzip the file.
Configure the Tensorflow with install CUDA 11.1
Run “configure.py”. Configure according to images shown below

![포맷변환 noname01](https://user-images.githubusercontent.com/20577227/114127469-66af1a00-9935-11eb-9e62-b4c4d598aca3.jpg)



Run “D:\tensorflow-r2.4>bazel --output_base=D:/AI/tensorflow-r2.0 build --config=opt //tensorflow:tensorflow.dll”

After “INFO: Build completed successfully, 8708 total actions”

"D:\tensorflow-r2.4\bazel-bin\tensorflow” will have the “Tensorflow.dll”

Expected time to build : 15-20min
