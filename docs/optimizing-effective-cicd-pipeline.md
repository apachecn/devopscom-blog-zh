# 优化有效的 CI/CD 渠道

> 原文：<https://devops.com/optimizing-effective-cicd-pipeline/>

持续集成和持续交付(CI/CD)经常被认为是成功开发运维的支柱。为了建立和优化 CI/CD 开发模型并从中获益，公司需要建立一个有效的管道来自动化他们的构建、集成和测试过程。这需要用五个关键要素来构建 CI/CD，当这些要素有效结合时，将作为 DevOps 的成功基石，并提供无数的底线收益。

## 建设管道

让我们先来看看健康的 CI/CD 架构所需的五个基本要素，然后讨论它们对业务的好处:

*   **频繁测试和提交代码形式的微敏捷:**开发生命周期始于对开发的请求，然后开发接受请求并设计解决方案、编码、测试并提交给代码库。从这里开始，代码由 QA 测试，然后部署到生产中。虽然每一步都很重要，但我们从这里开始，因为本地测试发生得最频繁，在流程的这个阶段发现的错误有助于避免在生产中发现错误的巨大开销。为了实现微敏捷，开发人员必须清楚地了解在做出更改后他们应该将代码提交到哪里，并且他们应该经常测试和更新他们的代码——一天多次。这意味着开发测试应该易于在本地运行，并且是 QA 的一个子集。结果是由开发推动的代码根据定义是 QA 就绪的。
*   自动化 QA: 在我的工作中，我看到许多组织的 QA 团队是流程中最大的瓶颈之一。这不是因为缺乏技能，而是因为很少有人花大量时间在 QA 测试环境上等待，而这正是他们工作所需要的。为了避免这种情况，QA 流程应该完全自动化，从进门的 QA 就绪代码到另一边的一键提升。在这两者之间，QA 应该与开发有一个持续的反馈循环，在这个循环中，关于 bug 的交流——以及对 bug 的跟踪——是清晰且易于遵循的，允许开发轻松地修复问题并重新提交代码以供进一步测试。此外，CI/CD 环境中的自动化 QA 应该关注由小测试批次组成的微循环，而不是为期一周的宏观测试。自动化和沟通在这里是压倒一切的必要条件，通过立即传达给开发人员的报告和自动拒绝失败的代码提交来展示。
*   **类似生产的环境:**为了提高效率和效果，开发和测试环境应该尽可能地反映生产环境。他们应该遵循 PRQ 法则，我喜欢这样称呼它——像生产一样，可重复，快速。具体来说，建立新环境应该是快速而容易的，开发人员只需按一下按钮，就可以部署新环境来满足他们的开发和测试需求。这样做允许开发人员快速失败，打破和重新创建环境而不用担心，因为他们知道他们每次都可以轻松地重新创建相同的环境。我经常推荐使用诸如 Jenkins 这样的工具来帮助这个过程；如果开发人员和 IT 运营人员使用相同的工具，那么简化 CI/CD 流程和实现 DevOps 的承诺就会容易得多。
*   **一键式推广:**正如我前面提到的，一个架构良好的 CI/CD 管道可以一键式推广到生产。这确保了将变更无缝地转移到整个生产环境中，尽可能减少开发和运营之间的冲突。为此，这种摩擦的减少应该发生在过程的所有步骤中，从一开始就使用高效的代码交付管道来平衡安全性和敏捷性。云基础设施与容器技术和自动化相结合，可以轻松优化跨团队和整个开发运维之旅的流程。
*   **全自动部署:**高效 CI/CD 渠道的最后一个因素是全自动部署。任何由开发人员做出并被 QA 接受的配置更改都应该自动应用。以这种方式持续集成有助于避免系统停机，并且大大减少了人为错误。还应持续监控部署，以便 IT 部门最先了解潜在的问题。这有助于将问题扼杀在萌芽状态，允许更快的回滚和将代码返回到开发中，以修复任何可能无法正常运行的问题。先于客户发现问题有助于确保客户满意度和声誉。

## 管道的好处

除了这些好处之外，当有效地结合时，这些成分最小化了本地测试、QA 和生产过程的时间和成本；减少发现问题及其原因所需的时间；并加速生产就绪代码的交付。我们可以在整个 CI/CD 渠道中看到这一点:

*   开发人员对过程有更大的控制权，并且可以通过快速提出新环境、针对新环境进行测试并在需要时轻松地重新开始来更快地响应市场需求。此外，开发人员可以快速适应新环境，这种方法已被证明可以减少故障和解决故障的时间。
*   运营收益，因为自动化减少了 CI/CD 流程中的摩擦，减少了重复的手动工作，减少了出现“粗手指”错误的机会，也减少了在流程中引入低效率的机会。
*   此外，更少的手动重复性工作为流程中的每个人提供了更多的时间来进行战略工作，这为组织提供了直接的底线价值。

CI/CD 是成功开发运维的支柱，根据 CA 的[研究，应用开发运维的组织发现新应用的上市时间减少了 18 %,交付新软件的时间增加了 21 %,否则他们无法完成。掌握高效 CI/CD 渠道的团队向市场交付更快、更高质量的应用，带来 19%的收入增长。将这些要素混合在一起会产生一个高效、简化的 CI/CD 渠道，这是 DevOps 成功的一个基本支柱，当它们混合在一起时，会带来直接的业务优势。](http://rewrite.ca.com/content/dam/rewrite/files/White-Papers/devops-winning-in-application-economy-2.pdf)

## 关于作者/Aater Suleman

**![Aater Suleman](img/16ee5f19864bbc599a071b8a01303c3e.png) Aater Suleman** ，Flux7 的首席执行官&联合创始人，是服务器和分布式系统性能优化方面的业界资深人士。他在奥斯汀的德克萨斯大学获得博士学位，目前还在那里教授计算机系统设计和体系结构。作为 UT-Austin 的一名教师，Suleman 先生专注于优化涉及 AWS 云的 DevOps 架构。他与 Flux7 顾问团队一起工作于开发流程的每一步，从使用 vagger 和 Docker 创建本地开发人员环境，到使用 Jenkins 或 RunDeck 进行持续集成和持续交付，到使用 Chef/Puppet/Ansible 进行配置管理，再到使用 Capistrano/Fabric/bash 创建用于从 Git 部署新代码的高效系统。他的背景是作为一名架构师，他在硬件和软件方面都有经验。这种结合为开发和运营带来了独特的视角和广阔的视野。