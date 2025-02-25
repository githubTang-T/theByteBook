# 1.1 理解云原生

云原生，其实不是一个全新的概念，而是云计算发展历程中的对理念的更新和延伸。按照云技术的发展以及业务对云要求的变化，初期的云计算关注点更多的是 基础设施层的建设，交付形式为 IaaS（Infrastructure as a Service，基础设施即服务），这个阶段的目标让基础设施运维成本更低。

云计算的第二个阶段，也是移动互联网飞速发展的阶段，产品服务对`在线`有了更高的要求（例如可用性 99.999%，迭代升级用户无感知，业务可靠性适应流量变化等等），支撑此类产品的架构所具备的特点也要求诸如：高可用、快速迭代/交付、资源按需分配等。在这个阶段，对云计算提供的服务形式有了新的转变，更多的是考虑平台服务，资源的束缚的摆脱以及直接面向服务、运维和管理的程序化操作，同时业务架构会充分利用`云`的特点来设计和满足业务需求，技术架构变成了类似于云中派生出来的产物。

这也就是`云原生`概念核心本意：充分利用云的先天优势，例如计算弹性、敏捷、资源池和服务化等特性，解决业务在开发、运行整个生命周期中遇到的问题。

CNCF 官网对云原生的定义如下：

> 云原生技术有利于各组织在公有云、私有云和混合云等新型动态环境中，构建和运行可弹性扩展的应用。云原生的代表技术包括容器、服务网格、微服务、不可变基础设施和声明式 API。 这些技术能够构建容错性好、易于管理和便于观察的松耦合系统。

>采用基于云原生的技术和管理方法，结合可靠的自动化手段，云原生技术使工程师能够轻松地对系统作出频繁和可预测的重大变更。可以更好地从云中诞生业务，也可以把业务迁移到不同的云中，从而享受云的高效和持续服务的能力。

<div  align="center">
	<img src="../assets/cloud-native.png" width = "280"  align=center />
	<p>图 1-2 云原生概念图</p>
</div>

## 1.1.1 什么是 CNCF？

CNCF (Cloud Native Computing Foundation，云原生计算基金会)，致力于云原生（Cloud Native）技术的普及和可持续发展。

CNCF 中有个 Landscape 全景图，用户可以了解实施云原生架构有哪些具体的软件和产品选择。CNCF Landscape 几乎包揽了所有云计算相关开源项目，迄今为止，CNCF 在其公布的云原生全景图中，显示了目前近 30 个领域、数百个项目的繁荣发展。

<div  align="center">
	<img src="../assets/landscape.png" width = "100%"  align=center />
	<p>图 1-3 CNCF 云原生项目 Landscape </p>
</div>

至 2023 年，CNCF graduated 级别项目中已包括 Kubernetes、Prometheus、Helm、argo、etcd、istio、Envoy、Harbor 等众多应用，孵化级别的项目更是数不胜数。

可以说 CNCF 早已超出了 Kubernetes 的范畴，而是旨在一个建立在 Kubernetes 为底层资源调度和应用生命周期管理之上的生态系统，CNCF 中还演进出了如 Service Mesh 和 Serverless 之类的分支。


