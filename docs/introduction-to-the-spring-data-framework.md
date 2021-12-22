# 春季数据框架介绍

> 原文:[https://www . geesforgeks . org/spring-data-framework 简介/](https://www.geeksforgeeks.org/introduction-to-the-spring-data-framework/)

在之前的文章中，我们已经讨论过[弹簧框架](https://www.geeksforgeeks.org/introduction-to-spring-framework/)和[弹簧靴](https://www.geeksforgeeks.org/introduction-to-spring-boot/?ref=rp)。在本文中，我们将了解 spring 数据框架。

<u>**对 Spring Data Framework 的需求**</u>
我们的数字世界保存着超过 20 兆字节的数据，这些数据和我们物理宇宙中的恒星一样多。这些数据来自各种来源，如银行、零售、电子商务、教育、建筑、社交网站等，并以结构化和非结构化两种形式提供。创建、捕获、存储和管理这些数据的成本是该行业面临的最大挑战。市场上有很多软件和框架在一定程度上解决了这个问题。但是，这些框架仍然面临一些问题，例如:

*   在关系数据库管理系统中扩展写操作是极其困难和不可能的。
*   垂直或水平缩放它要么有一些限制，要么很昂贵。

NoSQL 数据解决了这个问题，该数据作为点解决方案出现，其思想是从 **ACID** (原子性、一致性、隔离性和持久性)转移到 **BASE** (基本可用、可扩展、最终一致)。NoSQL 是一个持续的趋势，对于非关系数据库的开发人员来说，这是一个为正确的工作使用正确工具的选择。除了 NoSQL，我们还有大数据，它指的是一个数据集，其大小超出了典型数据库软件工具捕获、存储、管理和分析数据的能力。几乎每个行业都有大数据，从 10tb 到几 PB 不等。

因此，我们可以观察到数据访问格局发生了很大变化。关系数据库管理系统仍然很重要，但不能被视为“一刀切”的解决方案。我们也知道 Spring 框架一直为 RDBMS 数据访问提供了很好的支持，但是缺乏处理其他类型的数据访问(NoSQL 和大数据)。因此，Spring Data 项目的目标是用各种数据技术(关系数据、非关系数据和大数据)更新 Spring 数据支持，同时保留特定于商店的特性和功能。

<u>**春季数据框架:**</u>

**Spring 数据框架**是包含多个子框架的父项目。所有这些子框架都处理特定于数据库的数据访问。该框架的设计目标是为所有数据访问技术(如关系或非关系数据库、基于云的技术或地图缩减框架)提供一个基于 Spring 的熟悉且一致的模型。简而言之，Spring Data 是一个让 Spring 开发人员轻松进入 NoSQL 新兴世界的计划。以下是 Spring Data 积极支持的一系列技术。

1.  **关系**
    *   联合行动计划扩展部分
    *   JDBC 扩展
2.  **非关系**
    *   Redis
    *   蒙戈
    *   巴什
    *   Neo4J
    *   Gemfire
    *   全文搜索引擎
3.  **查询 DSL**
    *   独立的开源项目，为执行查询提供类型安全。
4.  **大数据**
    *   Hadoop
    *   HDFS 和毛里求斯
    *   储备
    *   猪
    *   级联

<u>**这个框架中很少有热门的发布模块:**</u>

以下是 Spring Data 项目下发布的一些主要模块:

1.  JDBC 春天数据公司
2.  春季数据
3.  春季数据共享
4.  春季数据休息
5.  弹簧数据键值
6.  春季数据蒙古数据库
7.  春季数据 LDAP
8.  Spring Data Redis(春季数据重定向器)
9.  阿帕奇·卡珊德拉的春季数据
10.  阿帕奇索尔的春季数据
11.  Apache Geode 的春季数据
12.  Pivotal GemFire 的春季数据

**正在开发的模块:**

目前，spring data R2DBC 模块正在开发中。本模块的特点是:

*   存储库支持。
*   通过模板进行资源分配和异常翻译。
*   SQL 和 NoSQL 数据存储的对象/数据存储映射。
*   存储库方法名的动态派生查询。
*   透明的审计支持。

**关键词和定义:**以下是 Spring Data 框架中使用的一些关键术语及其定义。

1.  **存储库:**通过类似集合的接口在数据映射层和域之间进行中介，以访问域对象。
    *   创建 POJO，它将成为您的模型或实体。
    *   为 CRUD 操作扩展存储库接口，并添加查询方法(查找器方法)。
    *   配置 Spring 以扫描存储库接口并创建实现。
    *   将实现注入到您的服务中。
2.  **QueryDSL:** 支持为多个后端构建类型安全的类似 SQL 的查询，包括 MongoDB、Lucence、JPA、JDO、SQL 和 Java 中的普通集合。
3.  **NoSQL 数据模型:** NoSQL 数据模型通常以键值对的形式表示，并且大多以 JSON 或图形的形式记录。
4.  **Redis:** 它是一个致力于键值存储的持久缓存框架。它有很多特性，支持丰富的数据类型(字符串、二进制、列表、集合、有序集合、哈希映射等)。它可以对内存进行定期快照，并可以将命令附加到日志文件中。
5.  **HBase:** 是一个面向列的数据库。其中行指向作为键值对的“列”。柱可以分组为柱族。
6.  **MongoDB:** 它是一个开源的、可扩展的、高性能的、面向文档的 JSON 风格的数据库，文档被组织在集合中。它被认为是动态查询的丰富查询语言之一。它具有地理空间特征。
7.  **图形**图形是一种通用的数据结构。数据上下文中的图形并不意味着图表、图解或矢量图形，而是具有存储数据的特殊意义，数据被结构化为图形。

最后，我们可以得出结论，spring data 是一个伞式项目，旨在统一和简化对各种数据库系统的访问。