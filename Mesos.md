# Mesos Introduction

Apache Mesos，一個開放原始碼軟體專案，是一種叢集電腦管理工具，由加州大學柏克萊分校開發。能夠將資料中心電腦系統中的CPU、記憶體、儲存裝置以及其他運算資源，全部加以虛擬化，並進行管理。

## Why Mesos

http://dockone.io/article/686

## Mesos Architecture

![](http://cdn2.infoqstatic.com/statics_s2_20160601-0225u2/resource/articles/analyse-mesos-part-01/zh/resources/0413011.jpg)

    (1)    Mesos-master：Mesos master，主要負責管理各個framework和slave，並將slave上的資源分配给各個framework
    (2)    Mesos-slave：Mesos slave，負責管理本节点上的各個mesos-task，例如：為各個executor分配资源
    (3)    Framework：如：Hadoop，Spark等，通過MesosSchedulerDiver接入Mesos
    (4)    Executor：安装到mesos-slave上，用於啟動Framework中的task。




