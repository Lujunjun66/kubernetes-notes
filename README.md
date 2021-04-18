# Kubernetes 学习笔记

> 本系列是 [Kubernetes 学习笔记](https://www.huweihuang.com/kubernetes-notes/)
> 
> 更多的学习笔记请参考：
> - [Kubernetes 学习笔记](https://www.huweihuang.com/kubernetes-notes/)
> - [Golang 学习笔记](https://www.huweihuang.com/golang-notes/)
> - [Linux 学习笔记](https://www.huweihuang.com/linux-notes/)
> - [数据结构学习笔记](https://www.huweihuang.com/data-structure-notes/)
>
> 个人博客：[www.huweihuang.com](https://www.huweihuang.com/)


# 目录

## 前言

* [序言](README.md)

## PaaS

* [12-Factor](paas/12-factor.md)
* [k8s知识体系](paas/k8s.md)
  
## 安装与配置

* [使用kubespray安装kubernetes](setup/install-k8s-by-kubespray.md)
* [使用minikube安装kubernetes](setup/install-k8s-by-minikube.md)
* [使用kind安装kubernetes](setup/install-k8s-by-kind.md)
* [k8s证书及秘钥](setup/k8s-cert.md)

## 基本概念

* [kubernetes架构]()
    * [Kubernetes总架构图](concepts/architecture/kubernetes-architecture.md)
    * [基于Docker及Kubernetes技术构建容器云（PaaS）平台概述](concepts/architecture/paas-based-on-docker-and-kubernetes.md)
* [kubernetes对象]()
    * [理解kubernetes对象](concepts/object/understanding-kubernetes-objects.md)
    * [kubernetes常用对象说明](concepts/object/kubernetes-basic-concepts.md)
* [Pod]()
    * [Pod介绍](concepts/pod/pod.md)
    * [Pod定义文件](concepts/pod/pod-definition.md)
    * [Pod生命周期](concepts/pod/pod-lifecycle.md)
    * [Pod健康检查](concepts/pod/pod-probe.md)
    * [Pod存储卷](concepts/pod/pod-volume.md)
    * [Pod配置管理](concepts/pod/pod-configmap.md)
    * [Pod调度](concepts/pod/pod-scheduler.md)
    * [Pod操作](concepts/pod/pod-operation.md)

## 流程图

* [Pod创建流程](flow/pod-flow.md)
* [PVC创建流程](flow/pvc-flow.md)

## 核心原理

* [Api Server](principle/kubernetes-core-principle-api-server.md)
* [Controller Manager](principle/kubernetes-core-principle-controller-manager.md)
* [Scheduler](principle/kubernetes-core-principle-scheduler.md)
* [Kubelet](principle/kubernetes-core-principle-kubelet.md)

## 网络

* [Docker网络](network/docker-network.md)
* [k8s网络](network/kubernetes-network.md)
* [Flannel]()
    * [Flannel介绍](network/flannel/flannel-introduction.md)

## 存储

* [Volume](storage/volume.md)
* [Persistent Volume](storage/persistent-volume.md)
* [Persistent Volume Claim](storage/persistent-volume-claim.md)   
* [Storage Class](storage/storage-class.md)
* [Dynamic Volume Provisioning](storage/dynamic-provisioning.md)

## CSI

* [csi-cephfs-plugin](csi/ceph/csi-cephfs-plugin.md)
* [部署csi-cephfs](csi/ceph/deploy-csi-cephfs.md)
* [部署cephfs-provisioner](csi/provisioner/cephfs-provisioner.md)
* [FlexVolume介绍](csi/flexvolume.md)

## 资源配额

* [资源配额](resource/resource-quota.md)
* [Pod限额](resource/limit-range.md)
* [资源服务质量](resource/quality-of-service.md)   

## 运维指南

* [kubectl安装与配置](operation/install-kubectl.md)
* [kubectl命令说明](operation/kubectl-commands.md)
* [kubectl命令别名](operation/kubectl-alias.md)
* [安全迁移节点](operation/safely-drain-node.md)
* [kubernetes集群问题排查](operation/kubernetes-troubleshooting.md)
* [指定Node调度与隔离](operation/nodeselector-and-taint.md)

## 开发指南

* [client-go的使用及源码分析](develop/client-go.md)
* [nfs-client-provisioner源码分析](develop/nfs-client-provisioner.md)
* [csi-provisioner源码分析](develop/csi-provisioner.md)

## 源码分析

* [kubelet]()
    * [NewKubeletCommand](code-analysis/kubelet/NewKubeletCommand.md)
    * [NewMainKubelet](code-analysis/kubelet/NewMainKubelet.md)
    * [startKubelet](code-analysis/kubelet/startKubelet.md)
    * [syncLoopIteration](code-analysis/kubelet/syncLoopIteration.md)
    * [syncPod](code-analysis/kubelet/syncPod.md)
* [kube-controller-manager]()
    * [NewControllerManagerCommand](code-analysis/kube-controller-manager/NewControllerManagerCommand.md)
    * [DeploymentController](code-analysis/kube-controller-manager/deployment-controller.md)
    * [Informer机制](code-analysis/kube-controller-manager/sharedIndexInformer.md)
* [kube-scheduler]()
    * [NewSchedulerCommand](code-analysis/kube-scheduler/NewSchedulerCommand.md)
    * [registerAlgorithmProvider](code-analysis/kube-scheduler/registerAlgorithmProvider.md)
    * [scheduleOne](code-analysis/kube-scheduler/scheduleOne.md)
    * [findNodesThatFit](code-analysis/kube-scheduler/findNodesThatFit.md)
    * [PrioritizeNodes](code-analysis/kube-scheduler/PrioritizeNodes.md)
    * [preempt](code-analysis/kube-scheduler/preempt.md)
* [kube-apiserver]()
    * [NewAPIServerCommand](code-analysis/kube-apiserver/NewAPIServerCommand.md)

## 监控体系

* [监控体系介绍](monitor/kubernetes-cluster-monitoring.md)
* [cAdvisor介绍](monitor/cadvisor-introduction.md)
* [Heapster介绍](monitor/heapster-introduction.md)
* [Influxdb介绍](monitor/influxdb-introduction.md)


## Docker

* [安装Docker](docker/install-docker.md)
* [Docker架构图](docker/docker-architecture.md)
* [Docker常用命令原理图](docker/docker-commands-principle.md)
* [Dockerfile使用说明](docker/dockerfile-usage.md)
* [Docker源码分析]()
    * [Docker Client](docker/code-analysis/code-analysis-of-docker-client.md) 
    * [Docker Daemon](docker/code-analysis/code-analysis-of-docker-daemon.md) 
    * [Docker Server](docker/code-analysis/code-analysis-of-docker-server.md) 

## Etcd

* [Etcd介绍](etcd/etcd-introduction.md)
* [Raft算法](etcd/raft.md)
* [Etcd启动配置参数](etcd/etcd-setup-flags.md)
* [Etcd访问控制](etcd/etcd-auth-and-security.md)
* [etcdctl命令工具-V2](etcd/etcdctl-v2.md)
* [etcdctl命令工具-V3](etcd/etcdctl-v3.md)
* [Etcd中的k8s数据](etcd/k8s-etcd-data.md)
* [Etcd-Operator的使用](etcd/etcd-operator-usage.md)

## Virtual Kubelet

* [Virtual Kubelet介绍](virtual-kubelet/virtual-kubelet.md)
* [Virtual Kubelet命令](virtual-kubelet/virtual-kubelet-cmd.md)

## KubeEdge

* [KubeEdge介绍](kubeedge/kubeedge-arch.md)
* [KubeEdge源码分析]()
    * [cloudcore](kubeedge/code-analysis/cloudcore.md)
    * [edgecore](kubeedge/code-analysis/edgecore.md)

## GPU

* [nvidia-device-plugin介绍](gpu/nvidia-device-plugin.md)

# 赞赏

> 如果觉得文章有帮助的话，可以打赏一下，谢谢！

<img src="https://res.cloudinary.com/dqxtn0ick/image/upload/v1551599963/blog/donate.jpg" width="70%"/>
