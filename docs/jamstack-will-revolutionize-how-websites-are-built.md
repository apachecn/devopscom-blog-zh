# Jamstack 将彻底改变网站的构建方式

> 原文：<https://devops.com/jamstack-will-revolutionize-how-websites-are-built/>

Today, every organization wants a website that loads quickly and looks sharp. The reasons go much deeper than cosmetic motivations, though—even a slight delay in loading can cause users to exit a page prematurely and site performance plays an important role in search engine rankings. Meanwhile, threats like [ransomware](https://webinars.devops.com/comprehensive-ransomware-protection-and-recoverability-for-cloud-native-applications) and phishing are everywhere and are constantly evolving, requiring organizations to look for more ways to improve site security and protect user data from bad actors. Then, of course, there’s the need to quickly and easily scale websites to meet sudden spikes in demand. The need to adapt quickly has become especially apparent over the last two years as we have come to rely on the internet in new and profound ways compared to pre-pandemic times. Fortunately, a relatively new but popular approach to web development—[Jamstack](https://jamstack.wtf/)—is taking websites to a nearly infinite level of [scalability](https://devops.com/five-donts-when-scaling-devops/) and performance, serving up only what you need, when you need it. To understand the value that Jamstack brings today, it’s helpful to take a look at how we got here.    Throughout the history of the internet, web and database servers were the primary infrastructure for site hosting. When websites got more complicated, another layer, called the application tier, would take on more complex aspects of the site (like an API, for example). As traffic increased, web servers were scaled out to add capacity with the help of load balancers. Scaling in this manner wasn’t always easy or cost-effective, given how unpredictable consumer demand and spikes in traffic often are. Later, content delivery networks (CDNs) came into the picture, taking a load off web servers by pushing static content to the edge. But, for most traffic, the origin servers would still have to be ready to serve site visitors. In this approach, website development and management were often costly and difficult to scale, and sites faced constant security risks.    Enter Jamstack. With Jamstack, all site content sits on a CDN, ready to be served. Web pages are pre-rendered instead of being rendered in real-time (as was the case in pre-Jamstack days). As such, content is closer to the end user, pages load faster and sites can easily scale up or down to handle unexpected shifts in traffic.    Jamstack represents an exciting and fundamental shift in how we have traditionally approached web development—one that is inclusive of the needs for performance, security, availability and scalability and at a much lower cost to the developer. It’s no surprise that Jamstack has taken the web development world by storm over the last couple of years; in 2020, the number of sites developed with Jamstack jumped[85%](https://almanac.httparchive.org/en/2020/jamstack) from the year prior. Here, I’ll share some basic tips for getting the most out of Jamstack.  

### 向静态网站添加动态功能

Jamstack 从静态网站的概念开始——尽可能多地预先构建网站——并融入动态元素，以更少的攻击媒介实现快速网站。这个词在 2015 年被创造为 JAMstack ，来源于:

*   J = JavaScript，网站的编程语言
*   A = APIs，在静态页面上启用动态内容
*   M =标记，它是 HTML 和 CSS 代码，为浏览器提供格式化指令

通过结合这三个要素， Jamstack 允许开发者快速创建和维护能够高效服务于用户的网站。静态网站可以很好地呈现移动、网页和视频，而动态特性则依赖于 API。通过预先建立尽可能多的网站，然后使用 CDN 将页面发送给世界各地的用户，可以实现高页面速度。当用户访问网站时，他们会看到由 CDN 提供的预渲染页面，无需专用服务器。    值得注意的是，页面的静态性质并不要求内容是静态的。利用第三方 API 可以实现动态内容，如搜索、支付处理和实时数据。这种模块化方法考虑到了灵活性并避免了供应商锁定——随着技术的变化和新工具的出现，更换不同的 API 变得很容易。与无服务器功能集成的能力也使 Jamstack 站点变得更加动态。    不需要 web 应用服务器和数据库服务器， Jamstack 页面随着访问者的增加而扩展，改善了访问者的体验和组织的底线。    本质上，一个 Jamstack 站点是没有后端的，需要开发者来管理。页面的静态性质意味着网站和数据库之间没有链接，这减少了安全攻击面。由于所有的站点元素都是从 CDN 或 API 交付的，潜在的攻击者 无法 侵入网络应用服务器或数据库服务器。    当组织使用这种方法创建网站时，不需要维护服务器，也不需要创建临时环境，因此不需要复杂的 DevOps 资源。Jamstack 的 简单性意味着比传统的站点有更少的移动部件和更少的出错空间。由于前端和后端之间的这种解耦， Jamstack 站点启动起来更快，也更可靠。    静态设置的另一个优点是恢复到页面的早期版本很简单。通过原子部署的概念，这是可能的，在原子部署中，整个站点一次更新，创建一个新版本。有了 Jamstack ，开发者可以更加自由地进行实验，避免传统网站令人厌倦的反复试验——如果有些东西没有按照预期呈现，将整个网站切换回以前的版本是没有痛苦的。  

### 组装一个jam stackT2 工具包

Jamstack 的 工具、流程和最佳实践正在快速发展，深入研究的一个重要部分是保持开放的态度，进行实验并跟踪新的发展。开始很简单，因为 Jamstack 与现有工作流相集成，许多组织已经与关键技术的供应商建立了关系，从而加快了决策过程。这些技术包括:

*   CDN:从靠近用户的位置交付页面，这是实现快速性能的一个要求。
*   静态网站生成器(SSG):使用原始数据和模板生成网站——自动化编码页面的过程，并确保它们是预先构建好的，可供用户使用。
*   内容管理系统(CMS):充当内容存储库。一个 Jamstack 网站的 CMS 被描述为“ [headless](https://devops.com/?s=headless) ”，这意味着内容存储在代码库之外，并通过 API 交付，以便在不同设备上无缝显示。

### 扩展jam stackT2 的值

我们还处于早期的 Jamstack 的 成熟期，并不是所有的部署都同样有效。例如，一些 Jamstack 平台托管在与 CDN 耦合的集中式数据中心之外，相对于直接从边缘交付站点，这降低了性能。一些 Jamstack 主机也收取更多费用来增加开发者席位，这阻碍了大型团队之间的合作，并可能导致不可预测的定价。

无论如何，jam stack 是近几年来对开发者来说最好的技术解决方案之一，它必将影响 web 开发的未来。它不仅使网站更快、更安全、更容易扩展，而且它建立在开发人员已经知道并喜欢的许多工具之上——使他们能够实现最大的生产力。