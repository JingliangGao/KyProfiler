# KyProfiler
[English](README.md) | [中文](README-zh.md)           
A fine-grained, non-intrusive profiler based on eBPF (extended Berkeley Packet Filter) technology.

# Prepare 
## 1. install system dependency
```bash
sudo apt update 
sudo apt install -y graphviz libgraphviz-dev pkg-config python3-pip
```

## 2. install BCC
Install BCC in systerm real environment, not docker, as it needs root permission       
a) install bcc header            
For Ubuntu system, use following commands:                
```bash
sudo apt-get install bpfcc-tools linux-headers-$(uname -r)
```

b) install bcc tools
```bash
sudo apt install bpfcc-tools
```

## 3. install Python package
```bash
sudo pip3 install -r requirements.txt --break-system-packages --ignore-installed typing_extensions
```

# Use
## 1. set environment variables
```bash
export GGUF_FILE=/opt/models/Llama-3.2-1B-Instruct-Q4_K_M.gguf
export LLAMA_BIN_DIR=/home/kylin/Code/profiler_workspace/llama.cpp/build_CPU/bin
```

## 2. run demo
```bash
sudo -E python3 run_llama.py --config jsons/config.json
```
