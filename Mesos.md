# Mesos Introduction

Apache Mesos，一個開放原始碼軟體專案，是一種叢集電腦管理工具，由加州大學柏克萊分校開發。能夠將資料中心電腦系統中的CPU、記憶體、儲存裝置以及其他運算資源，全部加以虛擬化，並進行管理。

## Why Mesos

http://dockone.io/article/686

## Mesos Architecture

![](http://mesos.apache.org/assets/img/documentation/architecture3.jpg)

    (1)    Mesos-master：Mesos master，主要負責管理各個framework和slave，並將slave上的資源分配给各個framework
    (2)    Mesos-slave(agent)：Mesos slave，負責管理本节点上的各個mesos-task，例如：為各個executor分配资源
    (3)    Framework：如：Hadoop，Spark等，通過MesosSchedulerDiver接入Mesos
    (4)    Executor：安装到mesos-slave上，用於啟動Framework中的task。
    
## Example of resource offer

![](http://mesos.apache.org/assets/img/documentation/architecture-example.jpg)

    - Slave 1向Master汇报其空闲资源：4个CPU、4GB内存。然后，Master触发分配策略模块，得到的反馈是Framework 1要请求全部可用资源。
    - Master向Framework 1发送资源邀约，描述了Slave 1上的可用资源。
    - Framework的调度器（Scheduler）响应Master，需要在Slave上运行两个任务，第一个任务分配<2 CPUs, 1 GB RAM>资源，第二个任务分配<1 CPUs, 2 GB RAM>资源。
    - 最后，Master向Slave下发任务，分配适当的资源给Framework的任务执行器（Executor）,接下来由执行器启动这两个任务（如图中虚线框所示）。 此时，还有1个CPU和1GB的RAM尚未分配，因此分配模块可以将这些资源供给Framework 2。
    
## Mesos Installation

http://mesos.apache.org/gettingstarted/

## Example


