# f2t-lab

## 简介

f2t-lab 是一个跟随 飞天闪客 的视频教程，一步步实现一个 Transformer 的代码库

【一小时从函数到Transformer！一路大白话彻底理解AI原理】
https://www.bilibili.com/video/BV1NCgVzoEG9

## 笔记
本项目跟随视频内容制作了对应的一些 notebook，方便大家跟随视频内容进行学习。
```bash
notebooks/
├── 01_from_functions_to_neural_networks
│   └── function_fitting_lab.ipynb   # 用神经网络拟合任意函数的实验
└── 02_calculate_the_parameters_of_a_neural_network

# 其他部分待更新
```

## 环境配置

本项目使用 uv 管理依赖, 主要使用 Pytorch 进行实验

拉取代码库
```bash
git clone https://github.com/DBinK/f2t-lab
```

同步依赖
```bash
cd f2t-lab
uv sync
```

默认使用 CUDA 12.9 的 PyTorch 环境, 若需要使用 CPU 版本的 PyTorch，将 `pyproject.toml` 中的 `[[tool.uv.index]]` 字段为如下内容, 再运行 `uv sync` 即可
```toml
[[tool.uv.index]]
name = "pytorch-cpu"
url = "https://download.pytorch.org/whl/cpu"
explicit = true
```

## 运行实验

```bash
cd notebooks
jupyter notebook 01_from_functions_to_neural_networks/function_fitting_lab.ipynb
```