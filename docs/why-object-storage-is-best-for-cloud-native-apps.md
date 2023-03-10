# 为什么对象存储最适合云原生应用

> 原文：<https://devops.com/why-object-storage-is-best-for-cloud-native-apps/>

困扰云应用程序开发人员的一个至关重要的问题是，“我们应该为我们的应用程序使用什么样的存储？”与计算运行时(Lambda/无服务器、容器或虚拟机)等其他选择不同，[数据存储选择](https://www.cio.com/article/219638/data-gravity-and-what-it-means-for-enterprise-data-analytics-and-ai-architectures.html)具有高度粘性，使得未来的应用改进和迁移更加困难。

所有三种超大规模存储都有存储服务，可提供基于数据块、文件和对象的数据访问。这些存储服务都很成熟，并提供不同的优势，这使得选择更加困难。尽管基于数据块和文件的存储已经存在了几十年，但在本文中，我们将阐述一些关键优势，这些优势应该使对象存储成为您在云中编写的新应用程序的默认存储选择。

| **存储类型/云提供商** | **谷歌云** | **亚马逊网络服务** | **微软 Azure** |
| **挡住** | [持久盘](https://cloud.google.com/persistent-disk) | [弹性块储存](https://aws.amazon.com/ebs/) | [磁盘存储](https://azure.microsoft.com/en-us/services/storage/disks/) |
| **文件** | [文件存储](https://cloud.google.com/filestore) | [弹性文件系统](https://aws.amazon.com/efs/) | [文件](https://azure.microsoft.com/en-us/services/storage/files/) |
| **对象** | [云存储](https://cloud.google.com/storage) | [【简单仓储服务(S3)](https://aws.amazon.com/s3/) | [斑点存储](https://azure.microsoft.com/en-us/services/storage/blobs/) |
|  |  |  |  |

### 易于扩展

可伸缩性是大多数云应用程序的重要需求。预计横向增加应用程序可用的计算能力会提高其处理请求、用户等的能力。处理高峰工作量。大多数云提供商也很容易扩展计算资源来满足高峰需求。随着计算资源的扩展，
基于数据块和文件的存储需要装载/连接到新的计算实例。

但是，粗略搜索一下就会发现，这些操作可能会因为多种原因而失败，甚至无限期挂起。它们通常也很难调试。使用文件和数据块存储解决方案的另一个问题是，由于同样的原因，计算机实例的拆卸可能会失败或挂起。这些问题立即否定了应用程序根据需要自由伸缩的能力。但是，对于基于对象的存储来说，这不是问题，因为不涉及装载步骤。新创建的计算实例可以立即访问您的对象存储。

### 共享和一致性

与其他存储类型相比，数据共享和一致性是对象存储真正闪光的地方。在基于数据块和基于文件的数据存储中，应用程序的一个实例最终可能会看到另一个实例写入的部分数据。应用程序开发人员最终不得不使用持久锁来解决这个问题。然而，这样的方案有它们自己的挑战:性能、正确性等。持久锁最终会使应用程序变得非常复杂；我见过即使是经验丰富的存储工程师在使用持久锁时也会犯错误。对象存储通过不公开部分写入的对象或主动写入的对象来避免这个问题。另外，请注意，对象通常是不可变的，因此一旦写入，它们只能作为一个整体被覆盖，而不能被部分覆盖。这意味着更新数据需要昂贵的读取-修改-写入周期。然而，大多数云提供商通过特殊的 API 来帮助避免这些额外的读取，这些 API 可以从现有对象的部分创建对象，如 GCS compose、Azure 的 put page blob 和 AWS multipart upload。

### 数据保护

在应用程序开发或推出期间，错误是必然会发生的。这些错误最终会影响关键数据，并可能中断正常的应用程序操作。这就是为什么必须在您使用的存储上配置某种备份/快照。

虽然大多数存储服务都有某种形式的备份/快照机制，但大多数都不太容易配置或恢复(也就是说，两者都需要多个步骤或云管理员的参与)。所有云对象服务都支持本地数据/对象版本控制功能，这非常容易实现。因此，基本上每当应用程序更新和/或删除时，对象存储服务都会保留数据的旧副本。如果需要恢复数据的旧副本，您只需读取旧版本并将其作为新对象写入即可。细心的读者可能会发现，如果一个应用程序经常写/删除数据，可能会留下许多旧版本的数据。有人可能会认为，在不需要的时候，这些东西很难识别和移除。然而，所有云提供商都支持基于策略的[数据生命周期管理](https://devops.com/?s=data+life+cycle+management)(见下一节)，因此您可以设置策略来删除不必要的副本。请注意，对象版本控制还提供了针对勒索软件攻击的出色防御。

### 基于策略的数据生命周期管理

应用程序生成的数据量只会逐年增加。这就是所有云提供商都支持其对象存储服务的基于策略的数据生命周期管理的原因。即使您不希望使用超过几千兆字节的数据，基于策略的生命周期管理也可以帮助您控制存储成本，并降低处理应用程序崩溃的代码复杂性。当您或您的云管理员出于数据保护和合规性原因决定启用对象版本控制和对象保留等功能时，基于策略的生命周期管理尤其方便。这些策略的设置非常简单，并且可以根据各个组织/应用程序/开发人员的需求轻松进行定制。

### 结论

从上面可以看出，对象存储服务的建立是为了支持简单和可伸缩的应用程序的开发。因此，如果您正在从头开始编写一个新的应用程序，请选择基于对象的存储来保持您的应用程序简单且易于维护。