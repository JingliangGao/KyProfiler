# KyProfiler
[English](README.md) | [中文](README-zh.md)           
一个基于eBPF（扩展伯克利包过滤器）技术的具备细粒度、非侵入式特性的性能分析剖析器

# 环境配置
## 1. 安装系统依赖
```bash
sudo apt update 
sudo apt install -y graphviz libgraphviz-dev pkg-config python3-pip
```

## 2. 安装BCC
由于需要root权限，因此需要在系统真实环境下安装BCC，而非虚拟环境（比如docker）。     
a) 安装 bcc 头文件          
对于 Ubuntu 操作系统， 采用如下命令：              
```bash
sudo apt-get install bpfcc-tools linux-headers-$(uname -r)
```

b) 安装 bcc 工具
```bash
sudo apt install bpfcc-tools
```

## 3. 安装Python软件包
```bash
sudo pip3 install -r requirements.txt --break-system-packages --ignore-installed typing_extensions
```

# 使用
## 1. 设置环境变量
```bash
export GGUF_FILE=/opt/models/Llama-3.2-1B-Instruct-Q4_K_M.gguf
export LLAMA_BIN_DIR=/home/kylin/Code/profiler_workspace/llama.cpp/build_CPU/bin
```

## 2. 运行案例
```bash
sudo -E python3 run_llama.py --config jsons/config.json
```
