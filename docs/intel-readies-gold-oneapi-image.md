# 英特尔准备好黄金 oneAPI 工具包

> 原文：<https://devops.com/intel-readies-gold-oneapi-image/>

英特尔本周表示，其代码为的统一[基础设施的](https://devops.com/?s=infrastructure%20as%20code) [oneAPI](https://newsroom.intel.com/news/intel-xpu-vision-oneapi-server-gpu/#gs.ksmf3l) 的黄金图像将于下月开始提供。

英特尔数据中心 XPU 产品和解决方案副总裁杰夫·麦克维(Jeff McVeigh)表示，目标是提供一个标准的应用编程接口(API)，用于访问任何处理器的计算能力，无论是哪家公司制造的处理器。

oneAPI 的推出恰逢英特尔推出一系列专用图形处理器单元(GPU)，旨在取代英伟达的主导地位。

![](img/3af724bd407e10088a7d41d7527b8dcc.png) McVeigh 表示，英特尔正在鼓励云服务提供商和内部部署系统的构建者采用 oneAPI 作为一种标准化方式，将任何 CPU、GPU、现场可编程门阵列(FPGAs)或任何其他类别的处理器整合到一个环境中，而不是继续依赖编程模型，如英伟达(NVIDIA)的 CUDA，该模型仅为一个类别的处理器设计。

普通开发人员可能永远不会直接与低级 oneAPI 进行交互，但 McVeigh 表示，处理器级别的一组标准 API 最终应该有助于降低 IT 的总成本，因为开发人员可以通过他们的应用程序调用多种处理器。

当然，英特尔也将 oneAPI 视为一个机会，可以取代 NVIDIA 成为 GPU 的主导供应商，这些 GPU 现在被广泛用于云端，以训练机器学习模型。虽然英特尔 CPU 仍然被大多数人用来运行推理引擎，使这些模型能够部署在生产环境中，但英伟达现在正在寻求利用其在云领域的成功来提供可用于运行推理引擎的 GPU 或 Arm 处理器。NVIDIA 正在收购 Arm，这是一家广泛应用于嵌入式系统和边缘计算环境的处理器提供商。

微软和负责监督构建人工智能(AI)应用程序的 TensorFlow 框架开发的开源贡献者迄今为止已经认可了 oneAPI。此外，伊利诺伊大学贝克曼高级科学技术研究所(University of Illinois Beckman Institute for Advanced Science and Technology)本周宣布，它正在创建一个 oneAPI 卓越中心(CoE)，该中心将把 oneAPI 编程模型扩展到纳米级分子动力学(NAMD)环境，该环境使用代码来模拟大型生物分子系统。

此前，斯德哥尔摩大学(SeRC)已经承诺将对 oneAPI 的支持添加到 GROMACS，这是一种用于构建生物分子模拟的开源软件，而海德堡大学正在努力将对 oneAPI 的支持添加到其他供应商的 GPU。McVeigh 补充说，英特尔也在开发基于 oneAPI 的软件，该软件与 CUDA 兼容。

最后，英特尔本周还宣布，英特尔隐式 SPMD 程序编译器(ISPC)将运行在 oneAPI Level Zero 之上，该编译器提供低级的直接到金属的接口。用 X 写的，ISPC 用于在英特尔 CPU 上加速英特尔 OSPRay 光线跟踪引擎。英特尔 GPU 即将支持 ISPC。

DevOps 团队可能需要一段时间才能看到 oneAPI 的好处；然而，随着以最合适的方式混合和匹配处理器变得越来越容易，很可能是因为后端的开销已经通过使用通用 API 而大大减少了。