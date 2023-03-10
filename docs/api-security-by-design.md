# API 安全设计

> 原文：<https://devops.com/api-security-by-design/>

“API 并不新鲜，”Secure Code Warrior 联合创始人兼首席技术官马蒂亚斯·马杜(Matias Madou)说，但它们最近得到了更广泛的应用。

它们曾经是本地机制，现在越来越多地以分布式方式使用，部分原因是应用程序架构的变化。另一个原因是，用户越来越有可能从组织外部访问系统，无论他们是客户、供应商还是在家工作的员工。

潜在地，任何人和任何事都可以访问一个 [API](https://devops.com/?s=API) ，因此开发人员和架构师应该假设 API 是公开的，并相应地处理请求。

这意味着解决诸如认证和授权之类的问题，并且通常确保 API 公开的唯一数据是应该公开的数据。

“所以假设每个 API 调用都是恶意的,”马斗建议道。

## 从头开始

实现 API 安全性是从设计和架构开始的，因此立即开始编写代码是一个错误。不幸的是，从一张完全空白的石板开始并不常见，一些代码可能已经存在了。在这种情况下，设计为可能的弱点做好准备尤为重要。

Madou 说，如果你想要安全的 API，那么就要确保项目中的每个人——架构师、开发人员、测试人员等等——都“非常了解安全”。

当公司或其竞争对手遇到问题时，通常会引发提高技能的需求。

他说，因此团队应该努力识别任何现有的问题，意识到他们需要主动避免潜在的问题，并接受适当的培训。

问题是，“安全和开发者通常不是最好的朋友，”马斗说。因此，开发人员倾向于认为安全是他们的安全同事的责任。但是应该有一个共同的目标:制作可靠安全的软件。

“安全需要帮助开发者，”他说。实现这一点的一个方法是任命一个“安全冠军”作为安全和开发团队之间的桥梁。嵌入式安全人员可以帮助开发人员认识到安全是一个使能因素，而不是一个阻碍因素。

## 需要帮助的时候就帮忙

将来自安全团队的交流嵌入到开发人员的工作流中是该过程的另一部分。松弛是一种可能的渠道。开发人员讨论问题时，安全人员需要在场。然后，他们可以利用机会说这样的话，“看起来你和 SQL 注入之间有问题。这里有一些可能会有帮助的培训材料。”

开发人员生活在他们的 IDE 中，所以集成应该发生在那里。但是设计这样的系统是为了帮助开发者，而不是控制他们。“开发者是人，不是被机器控制的机器人，”马斗警告说。

另一个考虑是避免不必要的打扰开发人员是很重要的。因此，这样的系统应该预测开发人员将要做什么，并提供适当的指导。

例如，如果有人编写了一个数据库连接，系统可以提供安全检索信息的语句。然后，开发人员可以复制并粘贴它们，而不是每次都从头开始。每次使用新代码都有引入漏洞的风险。

“制造这些系统很棘手，”马杜承认，但他预测，在未来几年，它们将变得越来越普遍。