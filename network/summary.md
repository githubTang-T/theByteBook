# 第二章：网络技术概论与应用实践

笔者多年的工作实践中，碰到的故障至少有 80% 属于网络问题。互联网系统架构中，网络体系是其中最基础也是最复杂的部分。最近几年像容器网络、SDN（Software Defined Networking）、观测技术，再具体到 DPDK、Cilium 等各类技术层出不穷，我们理清这些技术的核心脉络，总能发现 Linux 内核网络、网络虚拟化、内核旁路等技术的身影，所以夯实这些基础知识，才能看得更远。

在本章节笔者对这部分网络知识进行综合性概述，相信读者在学习此部分理论体系后，面对各类业务场景中错综复杂的问题，例如用户端弱网、高BDP（Bandwidth-Delay Product，带宽时延积）下的优化、数据中心组网等问题时，能有厚实的技术底蕴去分析问题并解决。

<div  align="center">
	<img src="../assets/guide.png" width = "500"  align=center />
	<p>图 2-1 本章内容导图 </p>
</div>
