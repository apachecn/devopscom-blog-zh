# 量子计算如何解决现实世界的问题

> 原文：<https://devops.com/how-quantum-computing-can-solve-real-world-problems/>

回顾过去，技术的历史似乎很容易预测，但未来通常更不确定。这种不确定性在量子计算领域表现得最为明显。当可能的结果范围从“量子计算机将是有史以来最重要的技术发展之一”到“量子计算可能永远不会变得足够实用，以证明可以取代经典计算机”时，试图做出预测似乎是徒劳的。然而，作为一个技术专家、投资者、消费者或者仅仅是一个好奇的观察者，不确定性本身的边界和纹理可能是非常有趣、有价值和信息丰富的。

量子计算不太可能取代今天的经典计算——至少最初不会——而是特定应用的潜在补充。德勤 的一份 [2021 年报告列出了几十种可以通过量子计算方法转变的应用:蛋白质折叠、流体模拟、信用核保、金融风险分析、供应链优化和预测、车辆路由、欺诈检测、故障分析、天气预报、半导体芯片设计、产品组合优化、消费品推荐——这只是清单的一半。](https://www2.deloitte.com/us/en/insights/topics/innovation/quantum-computing-business-applications.html)

量子计算可以使以前难以处理的模拟、搜索和优化计算变得相对容易和快速。对于某些种类的计算，量子计算机可能比强大的经典计算机要快得多。虽然今天运行机器学习系统的经典计算机可以做出令人难以置信的准确预测，但理论上，基于量子的系统在某些预测相关的任务上可以远远超过它们的速度。

量子计算机背后的物理学、数学和计算机科学的融合令人着迷，但也很复杂。计算机科学家 Scott Aaronson 是最好的科学传播者之一，他最近为 *Quanta* 杂志写了一篇文章[](https://www.quantamagazine.org/why-is-quantum-computing-so-hard-to-explain-20210608/)，名为“为什么量子计算如此难以解释？”

简单来说，量子计算机是围绕“量子位”构建的，量子位是亚原子级别的组件，通常保持在令人难以置信的低温下(想象一下:绝对零度)，以最大限度地减少来自宇宙其他部分的干扰。这些成分可以被置于一种称为“叠加”的量子物理状态，这种状态允许它们在某种意义上同时呈现许多潜在值。尽管它们的值是不确定的，但在被还原到更经典的状态之前，可以在这些量子位上进行可靠的计算和转换，从而有效地并行化计算。量子计算机中的量子位也可以相互纠缠(这种现象被爱因斯坦称为“幽灵般的超距作用”)，将它们作为一个团队来利用，以增加可能计算的各种逻辑计算。对于某些类型的数学——例如，从无数选项中寻找最佳结果——与运行在经典计算硬件上的算法相比，量子算法似乎接近即时。

## **量子计算挑战**

公开可用的量子计算已经出现了几十年，但对于能够被广泛采用的产品何时发布，系统将采取什么形式，或者量子计算的影响将有多广多深，仍然没有可靠的预测。当涉及到广泛适用的量子计算机在规模上有用时，有许多技术挑战。量子计算机正在与经典计算机竞争，经典计算机在能力、多功能性和易用性方面也一直在快速进步。

量子计算机的一个重要瓶颈是，正确读取量子计算的结果容易出现非常高的错误率——在正确的结果作为输出呈现之前，微妙的叠加态可能会恶化。

阿伦森解释道:

> 简而言之，问题在于退相干，这意味着量子计算机与其环境之间不必要的相互作用——附近的电场、温暖的物体和其他可以记录量子位信息的东西……这个问题唯一已知的解决方案是量子纠错……但研究人员现在才开始让这种纠错在现实世界中发挥作用。当你读到关于 50 或 60 个物理量子位的最新实验时，重要的是要明白量子位是不能纠错的。在此之前，我们不指望能够扩展到几百个量子位以上。

一些理论家甚至认为实用的量子计算机是不可能建造的，因为系统中固有的大量“噪音”。数学家 [吉尔·卡莱](https://www.quantamagazine.org/videos/gil-kalai-why-quantum-computers-wont-work/) 预测，通过基本计算定理，通过纠错将噪音降低到可用水平会将计算机的数字处理能力限制得太低，以至于不值得使用。

尽管如此，研究人员继续凿除纠错的挑战，并通过了关键的技术里程碑。例如，7 月，谷歌研究人员在 [*【自然】*](https://www.nature.com/articles/s41586-021-03588-y) 发表了一篇论文，解释了他们如何找到一种有前途的减少误差的方法，这种方法可以随着更多量子位添加到系统中而扩展。

## **硬件、软件和应用前景**

量子硬件有几种不同的方法。 [里盖蒂](https://www.rigetti.com/) 和 [牛津量子电路](https://oxfordquantumcircuits.com/) 使用超导量子电路，一种更普遍的方法也受到了 [谷歌](https://blog.google/technology/ai/unveiling-our-new-quantum-ai-campus/) 、[、微软](https://www.microsoft.com/en-us/research/research-area/quantum-computing/?facet%255Btax%255D%255Bmsr-research-area%255D%255B0%255D=243138&sort_by=most-recent#:~:text=The%2520Microsoft%2520Quantum%2520team%2520innovates,a%2520general%252Dpurpose%2520quantum%2520computer.) 和 [IBM](https://www.ibm.com/quantum-computing/) 的青睐。 [IonQ](https://ionq.com/) (计划通过特殊目的收购公司交易 上市 [)和霍尼韦尔(最近](https://icr.swoogo.com/De-SPAC_IonQ) [宣布将其量子计算部门](https://cambridgequantum.com/wp-content/uploads/2021/06/210608_CQ_HON_PressRelease.pdf) 与英国剑桥量子计算合并)使用捕获的离子。 [D-Wave](http://www.dwavesys.com/) 采用量子退火， [ColdQuanta](https://coldquanta.com/) 采用冷原子， [Xanadu](https://www.xanadu.ai/) 采用光子学。每种方法都有其优点和缺点，每种硬件技术在达到可承受的规模时都面临着一系列不断变化的瓶颈。材料层的工作也在继续推进，例如， [Raicol 晶体](https://raicol-quantum.com/#applications) 正在生长量子准相位匹配晶体，可用于量子计算、传感、加密和通信等各种应用。不确定是否会有另一种方法超越他们，解决纠错和价格的挑战。

其他公司，如 [量子机器](https://www.quantum-machines.co/platform/?gclid=CjwKCAjwgb6IBhAREiwAgMYKRtW-OJ1BePOvrzD6vfKfftLcQraD_MQVT2doE8ppMCuLlBpGVQNL8BoCl1YQAvD_BwE) 、 [Q-CTRL](https://q-ctrl.com/) 和 [Seeqc](https://seeqc.com/) 正在构建可以在经典和量子硬件之间的空间运行的控制硬件。控制系统可以在高于绝对零度，但低于室温的温度下工作。其中一些系统涉及软件和硬件，可以执行诸如监控量子处理器性能、执行纠错或作为连接经典和量子硬件的抽象层等任务。

也有公司开发量子计算应用层软件，如 [萨帕塔](https://www.zapatacomputing.com/?gclid=Cj0KCQjw6s2IBhCnARIsAP8RfAjT7AvEgU9MEm_6abe0s1AgeefeairoTIF2u0tBeYuSdUuXqCgsqiIaAuzcEALw_wcB) [计算](https://www.zapatacomputing.com/)[river lane](https://www.riverlane.com/)或 [QC Ware](https://qcware.com/) 。这可以包括应用框架、组件、算法，甚至是交钥匙量子计算应用。 [Classiq](https://www.classiq.io/) 有用于量子电路综合的软件。量子计算和人工智能之间的软件交叉领域也有许多有趣的基础研究——例如，Zapata [发表的作品](https://www.zapatacomputing.com/news/generate-handwritten-digits/) 最近使用 IonQ 的离子阱量子系统训练机器学习系统，以生成高质量的低错误率手写数字。

数学家彼得·肖(Peter Shor)在 1994 年提出的量子计算的第一个理论用途之一，是用 [破解如今广泛用于保护数据的 RSA 加密](https://www.technologyreview.com/2019/05/30/65724/how-a-quantum-computer-could-break-2048-bit-rsa-encryption-in-8-hours/) 。这种威胁催生了对 [后量子密码术](https://en.wikipedia.org/wiki/Post-quantum_cryptography) 的研究，研究人员提出了多种新的加密方法，需要取代今天的算法来保护数据的隐私。诸如 [ISARA](https://www.isara.com/) (抗量子加密)和[Quantum Xchange](https://quantumxc.com/)(带外对称密钥交付平台)等公司的出现，帮助政府和公司为一个基于量子的加密破解算法开始破解当今加密的世界做好准备。

有几个广泛使用的软件开发工具包(SDK ),让开发人员为量子计算机编写软件，而实际上没有运行它的软件。事实上，量子计算开发环境之间已经爆发了一场格式战。

一个广泛使用的 quantum SDK 是[IBM qi skit](https://www.ibm.com/blogs/research/2018/02/qiskit-index/)，这是一个基于 Python 的开源开发工具包，用于在模拟器上原型化软件和设备，或者是基于云的 quantum 服务[IBM Quantum Experience](https://en.wikipedia.org/wiki/IBM_Quantum_Experience)。埃克森美孚、高盛、波音、摩根大通、三星和贝宝只是 IBM Quantum 的几个主要客户。 [另一个基于 Python 的开发工具包 Google Cirq](https://quantumai.google/cirq) 将大众吹捧为用户，大众也是 Google[TensorFlow Quantum](https://ai.googleblog.com/2020/03/announcing-tensorflow-quantum-open.html)的贡献者，这是一个开源库，将 Google 的 tensor flow 机器学习算法扩展到量子处理器，用于快速原型制作。微软的 [量子开发套件(QDK)](https://docs.microsoft.com/en-us/azure/quantum/overview-what-is-qsharp-and-qdk#:~:text=Q%2523%2520is%2520Microsoft's%2520open%252Dsource,developing%2520and%2520running%2520quantum%2520algorithms.&text=As%2520a%2520programming%2520language%252C%2520Q,statements%252C%2520and%2520common%2520data%2520types.) 基于微软的 Q#编程语言，为微软 Azure 云服务带来了量子兼容性。Azure Quantum 的早期客户包括化学模拟公司陶氏化学(Dow)和丰田贸易公司丰田通商(Toyota Tsusho)，后者正在开发交通灯优化技术，以减少城市交通拥堵。

在最近的一篇文章中，[](https://www.theinformation.com/articles/quantum-computing-startups-draw-record-investment)的信息指出，“ 亚马逊正在寻求在其亚马逊网络服务云业务 内招聘 100 多名新的量子计算科学家、硬件开发人员和工程师，“跟随大量资金流向该领域的初创公司，如 [【量子运动】](https://quantummotion.tech/) 、 [原子计算](https://www.atom-computing.com/) 和 [PsiQuantum 亚马逊还推出了亚马逊 Braket，这是一项完全托管的量子计算服务，客户可以使用来自不同供应商的硬件，如 IonQ、Rigetti 和 D-Wave。](https://psiquantum.com/)

也有可能最有价值的量子平台根本不会是通用的、水平的平台；相反，这个空间可能会发展到包括专用机器，或量子专用集成电路(ASICs)。与经典计算的发展方式不同，这可能意味着量子计算机将是高度专业化的集成硬件和软件的机器，为特定的应用量身定制，例如流体模拟或欺诈检测。

早期的用例可能涉及量子系统，作为更大的经典系统的一部分，扮演专门的角色，类似于英伟达的图形处理单元(GPU)，通常与高级 CPU 一起运行，可用于卸载 GPU 非常适合的特定计算。在这种模型中，量子组件是经典系统的“加速器”，信贷承销商可能会使用量子处理器来处理对申请人评分所涉及的任务之一，并可能使用不同的专用量子处理器来执行一部分计算，以优化其借款人的投资组合。

对于许多用例来说，计算的错误率仍然太高，开发人员只能在量子模拟平台上磨练他们的编码能力，等待量子计算机开始真正大规模工作。量子模拟器，如 [QMware](https://qm-ware.com/) ，让量子软件算法和应用相信自己运行在实际的量子硬件上，但实际上是运行在伪装成量子计算机的经典计算机上。

与此同时，为了管理一些时间上的不确定性，量子相关的初创公司可以 与政府、企业和大学买家一起寻求有利可图的项目，作为资金和需求的来源。 像一些生物技术创业公司一样，他们可以在组建强大团队和寻找早期采用者客户的同时做这件事 ，在科学里程碑上前进，同时关注未来的商业市场。

普遍可用的量子计算机面临的障碍很像替代能源面临的障碍:释放潜力需要硬件设计的突破、更低的制造成本和刺激大规模采用的驱动力。很多方法都行不通。

与任何技术一样，软件开发人员当然有可能为量子处理器找到人们今天尚未想到的有价值的应用程序——就像开发人员发现旨在处理图形处理的 GPU 也擅长训练高度并行的机器学习模型一样。

也就是说，一台广泛有用和有效的量子计算机的到来有可能成为一个颠覆性的机会，就像互联网的创造或使用机器学习进行预测一样。