## 简介
parallelmnn是HOPE-Scheduler的运行时部分，是一个可以根据执行计划异构并行的执行DNN模型的框架。
本仓库用于存放parallelmnn的patch，用于区分[MNN](https://github.com/alibaba/MNN)和parallelmnn的修改部分。

## 从开源版本应用patch
首先从github克隆MNN:
```shell
git clone https://github.com/alibaba/MNN.git
```
克隆本仓库：
```shell
git clone https://gitee.com/ict_huawei_2020/parallelmnn-patch.git
```
因为我们的parallelmnn是是基于MNN的0.2.1.6版本开始修改的，所以检出MNN的0.2.1.6版本
```shell
cd path/to/MNN
git checkout 0.2.1.6
```
之后，将patch文件拷贝到MNN目录
```shell
cd path/to/parallelmnn-patch
cp ./parallelmnn.path path/to/MNN/
```
应用patch
```shell
cd path/to/MNN
git apply parallelmnn.patch
```
之后，就可以编译MNN了。
## 编译
平台要求：`Ubuntu 16.04及以上`

要编译的目标为MNN中的`path/to/MNN/benchmark/CMakeList.txt`的`benchmark.out`。使用`bench_android.sh`可以快速编译安卓的二进制文件。编译需要Android NDK、Flatbuffer等。具体要求参见[compilation-Android](https://www.yuque.com/mnn/en/build_android)，[build-benchmark-tool](https://www.yuque.com/mnn/en/tool_benchmark)。

## 联系
有问题欢迎联系`xiachunwei@ict.ac.cn`。
