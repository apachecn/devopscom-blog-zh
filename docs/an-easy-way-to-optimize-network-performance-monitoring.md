# 优化网络性能监控的简单方法

> 原文：<https://devops.com/an-easy-way-to-optimize-network-performance-monitoring/>

网络性能监控，尤其是网络优化，与其说是一门科学，不如说是一门艺术，因为网络和应用程序的响应能力受到诸多因素的影响。此外，由于有大量数据在网络上传输，确定需要监控的数据类型(以及应该从哪里捕获数据)会变得非常困难。例如，根据 Enterprise Management Associates 在 2016 年 10 月进行的研究，41%的 IT 人员将超过 50%的时间用于解决网络和应用程序性能问题。

战术数据在 30 分钟后会损失 70%的价值，这使得数据收集过程更加复杂。如果您希望解决网络或应用程序问题，这使得数据分析的速度和准确性至关重要。

不过，有一个简单的方法可以改善你的生活:添加一个网络可见性架构。大多数 IT 人员都有安全架构和网络架构，但很少有人有可见性架构。网络可见性使您能够在正确的时间捕获正确的数据，因此您可以做一些有用的事情，例如快速隔离潜在的问题。

建立可见性架构非常简单。有四个主要组件:

*   数据存取
*   数据操作
*   应用智能
*   专用分析工具

数据访问可以由物理分路器、虚拟分路器和旁路开关提供。这些设备能让你及时获得你需要的数据。也可以使用 SPAN 端口；但是，这类设备的数据质量可能会有问题，因此不推荐使用。

在你获得了你需要的监控数据之后——可能还有一堆你不需要的数据——下一步就是把它发送给网络数据包代理(NPB)。该设备提供精细过滤功能，最大限度地将相关信息传递到您的监控工具。可以将特定类型的数据分割出来并发送到特定的工具，以提高效率并加快解决问题的速度。NPBs 还可以提供以下服务:数据聚合、重复数据删除和(OSI 模型的)第 2 层到第 4 层分组数据的负载平衡。

应用程序智能是 NPB 的另一项功能。该功能在应用层(即 OSI 堆栈的第 7 层)提供额外的过滤和分析。例如，您可以利用应用程序智能来防止网络上的应用程序带宽过载。您可以根据应用程序类型(如 Hulu、网飞、Pandora、FTP、HTTP、RTP 等)查看网络流量。).您还可以使用它来识别速度缓慢或性能不佳的应用程序。

可见性架构的最后一层由您的安全和监控工具组成。这些设备通常是专用工具(例如，嗅探器、网络性能监控[NPM]、应用性能监控[APM]等)。)来分析特定的数据。例如，APM 工具可以提供实时数据分析来帮助您管理网络，并让您先于用户发现问题。

然而，这些工具的独立部署可能会遇到不同的问题，例如过载的磁盘空间和处理、基于网络流量速度对不同接口端口的需求以及通过网络捕获数据的大量输入端口的需求。NPB 可用于捕获网络数据，并在数据进入 NPM 工具之前对其进行过滤。这通过减少混乱提高了工具的效率。对重复数据的额外过滤进一步提高了效率，并且还消除了与存储无关数据相关联的存储浪费。

网络管理员需要网络可见性解决方案来帮助他们发现、隔离和解决与网络及其应用相关的问题。这种架构为您的网络工具提供了一个完整的网络图，因此它们可以更快地解决问题。

基思·布罗姆利