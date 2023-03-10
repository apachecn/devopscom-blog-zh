# Diamanti 通过新的容器网络和存储功能加快了 MemSQL 的持续集成流程

> 原文：<https://devops.com/diamanti-accelerates-continuous-integration-pipeline-memsql-new-container-networking-storage-capabilities/>

多伦多 LINUXCON—(market wired—8 月 22 日)— Diamanti 是业内首款为 Linux 容器带来有保证的网络和存储性能水平的专用交钥匙容器设备的制造商，今天在 LINUXCON 上宣布，MemSQL 已加入 Diamanti 的测试计划，以实现其持续集成(CI)管道的高容量、一致的测试自动化。

CI 是一种流行的开发方法，它通过自动化的构建和测试过程来验证代码，从而快速识别和解决缺陷。虽然 CI 极大地提高了开发人员的工作效率，但是组织经常发现大量的自动化测试带来了计算挑战，需要定制的测试平台环境。

MemSQL 是领先的实时分析数据库平台提供商，处于 CI 和自动化验证的前沿。在公司早期，MemSQL 开始使用几个 Linux 节点进行验证集群，后来扩展到数百台服务器，每小时支持数千次测试，以保持非常高质量的代码发布。

MemSQL 首席架构师 Carl Sverre 表示:“作为一个针对速度和规模进行了优化的分布式内存数据库，MemSQL 提供一个超越用户期望的坚如磐石的平台，并在许多客户环境中工作，这一点至关重要。MemSQL 有数百万个复杂配置的测试场景。我们发现 Diamanti 的 container appliance 帮助我们在真实环境中快速验证新功能和软件更新，最终使 MemSQL 在创新上超越其他分布式数据库。"

Diamanti 于今年早些时候推出，旨在解决 Linux 容器化环境中的网络和存储挑战。MemSQL，一个早期的 Diamanti beta 站点，报告了在他们的 CI 自动化测试环境中的显著优势:

运营自动化–Diamanti 设备允许通过 API 为大量测试场景快速配置网络和存储，而不是手动配置基础架构或依赖固定配置。这使得创建隔离网络和存储卷的控制和自动化程度更高，比以前更容易扩展验证。

工作负载优先级和有保证的性能——不是每个测试场景都有相同的优先级或持续时间。有些测试更加 I/O 密集型，有些更关键，有些只持续几秒钟，而有些则需要几个小时。Diamanti 简化了工作负载优先级，使测试相互隔离，并保证长时间运行的测试不会被短时间运行的测试中断。

快速模拟存储和网络配置–MemSQL 等强大的软件平台必须针对客户环境的多种变化进行验证。在所谓的“四角测试”中，在极端情况下模拟多个条件，在最坏情况下评估代码。Diamanti 使像 MemSQL 这样的组织能够在其 CI 管道中快速模拟许多不同的网络和存储变量。组织可以使用 Diamanti 虚拟化网络和存储环境，而不必构建大型硬件实验室。

Diamanti 产品和营销副总裁 Mark Balch 说:“容器技术重量轻，部署速度快，非常适合现代持续集成方法的快速发展。“Diamanti 通过与主流开源容器堆栈紧密集成的自动化部署流程，提供敏捷的容器网络和存储能力。我们可以连接到现有网络，而无需成本高昂的重新架构，并且消除了会减缓应用生命周期的手动基础架构调整。Diamanti 很高兴欢迎 MemSQL 加入我们的测试计划，并帮助推进他们的创新分析平台。”

访问 LinuxCon 上的 Diamanti，观看产品演示并了解更多信息。Diamanti 现在对新的测试版用户开放。在[www.diamanti.com](http://www.diamanti.com/)报名试驾，亲自体验。

###

关于迪亚曼蒂

Diamanti 解决了组织在将容器化工作负载从开发转移到生产时面临的最具挑战性的网络和存储要求。Diamanti 设备可插入现有环境，提供有保证的性能，并将 I/O 吞吐量和延迟提高 10 倍，允许开发人员和运营商可预测地部署、扩展和管理容器，而无需耗时的定制。总部设在加州圣何塞的迪亚曼蒂得到了风险投资者 CRV、DFJ、GSR Ventures 和高盛的支持。欲了解更多信息，请访问[www.diamanti.com](http://www.diamanti.com/)或关注@diamanticom。