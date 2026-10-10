# KyProfiler
[English](README.md) | [中文](README-zh.md)           
A fine-grained, non-intrusive profiler based on eBPF (extended Berkeley Packet Filter) technology.

# Prepare 
Install BCC in systerm real environment, not docker, as it needs root permission       
1. install bcc header          
a) Ubuntu OS          
```bash
sudo apt-get install bpfcc-tools linux-headers-$(uname -r)
```

2. install bcc tools
```bash
sudo apt install bpfcc-tools
```