# 简述

  本工程将使用最新源代码创建etcd-discovery私人镜像、通过使用docker-compose将etcd结合etcd-discovery集群容器化。本工程基于Docker version 18.09.4,docker-compose version 1.24.0,ubuntu 18环境创建

  - 从/go/src/github.com/coreos/discovery.etcd.io获取Dockerfile,然后docker build -t       thomas.discovery.etcd.io .
  - 创建etcd_discovery_store，通过docker-compose.yml进行etcd discovery token集群节点数的存储，读取。
  - 创建discovery,通过docker-compose.yml启动etcd discovery服务
  - 最后使用同路径下的docker-compose.yml进行多节点集群服务启动。
