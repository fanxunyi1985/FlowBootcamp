-------------
词汇表
-------------

Nutanix 核心词汇
++++++++++++

AOS
...

AOS是Acropolis操作系统，它是运行在Controller VM（CVM）上的OS。

Pulse
.....

Pulse向Nutanix客户支持团队提供系统的诊断数据，以便他们可以为Nutanix平台提供主动的，基于上下文的支持。

Prism Element
.............

Prism Element是Nutanix的本地管理平台。与许多企业应用程序的界面相比，它更直观，更易于使用。

Prism Central
.............

Prism Central是Nutanix的多云控制和多集群管理的界面。Prism Central可以管理多个Nutanix群集，并用实现多集群的监视和分析。

Node（节点）
....

本地存储介质为SSD和可选HDD（全闪存模式和混合模式）的行业标准x86服务器。

Block
.....

2U机架安装式机箱，包含1个，2个或4个节点，具有共享的电源和风扇，但没有共享的背板。

Storage Pool（存储池）
............

存储池是一组物理存储设备，包括用于群集的PCIe SSD，SSD和HDD设备。

储存容器
.................

容器是用于实施存储策略的可用存储的子集。

关于I/O的读取
.....................

性能和可用性

- 数据在本地读取
- 仅当本地不存在数据时才进行远程访问

关于I/O的写入
......................

性能和可用性

- 数据写入本地
- 在其他节点上复制以实现高可用性
- 副本分布在整个群集中以实现高性能

Nutanix Flow
++++++++++++

Application（应用）安全策略
...........................

当您想通过指定允许的流量源和目的地来保护应用程序安全时，请使用应用程序安全策略。

Isolation（隔离）策略
............................

当您要阻止按类别标识的两组VM之间的所有流量（无论方向如何）时，请使用隔离策略。但这每一组内部的VM可以相互通信。

Quarantine（检疫）策略
.................

当您想要隔离受到病毒感染或攻击的VM并选择对其进行取证时，请使用该策略。在这样的情况下，隔离VM的两种模式是Strict（严格检疫）或Forensic（取证检疫）。

严格检疫：要阻止所有入站和出站流量时，请使用严格检疫。

取证检疫：如果需要实验取证工具，验证两个类别的流量是否具备相互通信的条件，请使用取证检疫。

AppTier
.......

将应用程序中的不同层级（例如，web，application_logic和数据库）的值添加到此类别，并在配置安全策略时使用这些值将应用程序划为层。

AppType
.......

将应用程序中的VM与适当的内置应用程序类型（例如Exchange和Apache_Spark）相关联。您也可以创建新的应用类型。

Environment（环境）
...........

添加需要要彼此隔离的环境的值，然后将VM与这些值相关联。
