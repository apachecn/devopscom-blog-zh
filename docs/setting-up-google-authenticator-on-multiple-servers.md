# 在多台服务器上设置 Google 认证器

> 原文：<https://devops.com/setting-up-google-authenticator-on-multiple-servers/>

Google Authenticator 非常棒。它允许我作为管理员在我的 UNIX 机器中设置和配置多因素身份认证，而不必花钱购买 YubiKey 或 RSA 令牌等工具。它很容易在任何类型的手机上设置——不需要专门的硬件或加密狗。它也很酷，因为你不需要从服务器到外部世界的网络访问。因为 Google Authenticator 是基于时间的，所以它不需要发送 SMS 或向中央服务器发出呼叫来获取当前的有效令牌。

不过，有点痛苦的是，我的每台服务器都需要不同的 Google Authenticator 令牌。标准设置会让您在每台服务器上运行 google-authenticator 命令，并拥有与服务器一样多的令牌。显然，这很快就变得笨拙和站不住脚。

相反，我想让一个令牌用于多个服务器。下面是我如何在每个系统上安装和配置 Google Authenticator。

### 第一台机器

在我的第一台机器上，我将[安装](https://support.google.com/accounts/answer/1066447?hl=en) Google Authenticator 并创建一个密钥——这正是我通常使用的流程。

**1:** 安装谷歌认证器。这是有据可查的。例子可以在[不可信连接](http://www.untrustedconnection.com/2013/06/dual-factor-ssh-google-authenticator.html)和[如何极客](https://www.howtogeek.com/121650/how-to-secure-ssh-with-google-authenticators-two-factor-authentication/)看到。我不会走每一步，因为这部分因操作系统而异；然而，其余的步骤是相同的。

![](img/f8159cb450ed218b3875553d798a9075.png)

**2:** 重启 ssh 服务

$ sudo 重启 ssh

**3:** 运行 google-authenticator 命令为你的账户生成一个密钥，你会把它存储在你的手机里。这些信息将存储在一个配置文件中，我们稍后会用到这个文件。我不需要评论你实际上必须把密钥输入到你的手机里，是吗？

![](img/3d0c39f357ee23a3932584a5d81ffb41.png)

转一转。从另一个 shell 继续尝试。

![](img/5f605c11a2d80cb1d8acb45738980cf5.png)

**5:** 我们来看看配置文件。我们将把这些内容复制到我们希望拥有相同密钥的其他机器上。

![](img/e4ad5868e03e462e364f88ceb4ca84bb.png)

### 在其他机器上安装 Google 验证器

对于所有其他机器，我将照常安装 Google Authenticator，但我将使用第一台机器上的密钥。这将允许我使用我在第一台机器上存储的相同密钥登录到每台机器。

**1:** 安装谷歌认证器。还是那句话，其他地方对此有详细描述。我们将安装程序，但不创建任何密钥

![](img/6bb994cd50c69e263431dccc7b6f816c.png)

**2:** 创建配置文件，并添加我们从另一台机器获得的内容。

![](img/48e404f60d54e65bb8056d1459aad6e6.png)

**3:** 设置配置文件的权限。

![](img/92dfcc06f460278a07da6139a5e8b95e.png)

**4:** 重启 ssh 服务。

![](img/946dbfcf1fa5111715d49b6690a926d6.png)

**5:** 测试登录。

![](img/6e90409174a476a7cbc4e2d5c7ae8d74.png)

瞧啊。我的服务器共享密钥！快乐的一天。

— [Rajat Bhargava](https://devops.com/author/rajatb73/)