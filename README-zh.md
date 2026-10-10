# KyProfiler
[English](README.md) | [中文](README-zh.md)           
一个基于eBPF（扩展伯克利包过滤器）技术的具备细粒度、非侵入式特性的性能分析剖析器

# 环境配置
由于需要root权限，因此需要在系统真实环境下安装BCC，而非虚拟环境（比如docker）。     
1. 安装 bcc 头文件          
a) Ubuntu 操作系统          
```bash
sudo apt-get install bpfcc-tools linux-headers-$(uname -r)
```

2. 安装 bcc 工具
```bash
sudo apt install bpfcc-tools
```