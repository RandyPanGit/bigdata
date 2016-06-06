# Spark Intrdution

# Spark Install

    - OS:Ubuntu-14.04
    - Java:Open-JDK-1.7.0_101
    - Mesos-0.28
    - scala-2.11.8
    - spark-1.6
    - VirtualBox 5.0.20
    - master_ip = 10.10.10.13
    - hostname:slave

根據[此篇文章](http://amberfu.blogspot.tw/2016/05/ubuntu-1404-scalaspark.html)在slave node上安裝spark

# Spark on Mesos

依據之前[步驟](https://github.com/RandyPanGit/bigdata/blob/master/Mesos.md)安裝完mesos cluster

再依據[此篇文章](http://yenyu-lovelan.blogspot.tw/2015/10/mesos-for-spark-running-on-cent-os-63.html)進行spark跟mesos相關設置

>**Note** spark-shell啟動:spark-shell --master mesos://master_ip:5050

完成安裝後可在mesos管理介面看到Framework頁面看到相關資訊

![](https://goo.gl/1Yl3ow)
