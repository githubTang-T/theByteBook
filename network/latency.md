# 2.1 理解各类延迟

伯克利大学有个动态网页[^注1]可以查看每年计算机中各类操作耗时、延迟的变化。我汇总了 2020 年的数据供读者参考。

了解这些延迟指标有助于设计和比较不同的解决方案以及评估服务质量。举例来讲，比较硬盘寻址和同个数据中心往返的延迟，这就意味着使用数据库服务要比本地磁盘存储更有效率。再如 Kafka、Leveldb 等存储引擎利用了顺序读写快过随机读写的特性，只做追加写操作来达到最佳性能，这些都是基于延迟来设计的方案。

<center><p>表2-1 计算机中各类延迟数据</p></center>

操作|延迟
:---|:--:|
L1 缓存查询| 1 ns
分支预测错误（Branch mispredict）| 3 ns
L2 缓存查询 | 4 ns
互斥锁/解锁 | 17 ns
在 1Gbps 的网络上发送 2KB | 44 ns
主存访问 | 100 ns
Zippy 压缩 1KB | 2,000 ns ≈ 2 μs
从内存顺序读取 1 MB | 3,000 ns ≈ 3 μs
SSD 随机读 | 16,000 ns  ≈ 16 μs
从 SSD 顺序读取 1 MB | 49,000 ns  ≈ 49 μs
同一个数据中心往返 | 500,000 ns  ≈ 0.5 ms
从磁盘顺序读取 1 MB | 825,000 ns  ≈ 0.8 ms
磁盘寻址 | 2,000,000 ns ≈ 2 ms
从美国发送到欧洲的数据包 | 150,000,000 ns ≈ 150 ms

<div  align="center">
	<img src="../assets/time.png" width = "300"  align=center />
	<p>图 2-2 秒(s)、毫秒(ms)、微秒 (μs)、纳秒(ns)之间关系 </p>
</div>


> 注1: https://colin-scott.github.io/personal_website/research/interactive_latency.html