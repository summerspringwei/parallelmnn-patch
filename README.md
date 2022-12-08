# ParallelMNN

parallelMNN is the heterogeneous execution engine of HOPE.

## How to apply

First check out MNN from github:
```shell
git clone https://github.com/alibaba/MNN.git
```

Clone this repo:
```shell
git clone https://gitee.com/ict_huawei_2020/parallelmnn-patch.git
```

Our parallelMNN is implemented based on MNN version 0.2.1.6,
first we need check out the corresponding version:
```shell
cd path/to/MNN
git checkout 0.2.1.6
```

Copy patch file to the directory of MNN and apply it:
```shell
cd path/to/parallelmnn-patch
cp ./parallelmnn.patch path/to/MNN/
cd path/to/MNN
git apply parallelmnn.patch
```

Then follow the instructions in the MNN repo to build MNN for android.

## How to build
OS platform: `Ubuntu 16.04` or later version.

Build target: the `benchmark.out` executable binary file defined in `path/to/MNN/benchmark/CMakeList.txt`.
You can use the `bench_android.sh` in the benchmark directory.
Detailed instrumentations can be found at [compilation-Android](https://www.yuque.com/mnn/en/build_android) and [build-benchmark-tool](https://www.yuque.com/mnn/en/tool_benchmark).

## Contact Us
For any questions, feel free to send an e-mail to `xiachunwei@ict.ac.cn`
