# 远程存款捕获:方便您的移动测试

> 原文：<https://devops.com/remote-deposit-capture-mobile-testing-convenience/>

“多少人的生命在等待中逝去！”拉尔夫·沃尔多·爱默生写道。

任何可以数字化的杂务都是受欢迎的。兑现支票怎么样？

兑现支票需要时间。你必须去银行，排队等候下一个可用的出纳员或自动取款机。如果你晚上去 ATM 机，你就要担心是谁潜伏在外面的阴影里。

这真的有必要吗？

7000 多家银行已经解决了这个问题，为我们节省了时间和麻烦。你现在可以拿一张支票，放在桌子上，用智能手机点击一张照片，它就会作为存款出现在你的账户上。

使用远程存款捕获，移动应用程序现在可以节省您去银行的时间。但完成这一壮举绝非易事。

## 移动银行的移动测试是一件严肃的事情

我们处理的是你的血汗钱。只需要一个小小的错误，就有人不得不花三个小时和银行经理争论为什么他们的存款只有上周的三分之一。

然后他们在社交媒体上告诉他们的朋友 A 银行是如何取走他们所有的钱的。然后，银行 A 的客户决定将他们的资金转移到银行 b 会更好。对于银行业来说，移动测试可能意味着为客户提供生活质量升级和失去业务之间的差异。

对于客户和金融机构来说，移动测试流程必须完美。为此，我们必须克服三大挑战:

### 挑战#1:实现移动测试自动化

银行的测试覆盖范围比大多数应用程序要大得多。如果没有来自基于云的移动实验室的自动化过程，这是不可能实现的，该实验室由数百个具有各自版本的设备和同时运行测试的移动操作系统组成。

挑战在于，对设备外部的项目(支票本身)进行测试，消除了自动化的可能性。我们如何安装一个机器人来将支票放在桌子上，从它在实验室的位置拉出一个移动设备，并在拍照前将它放在离支票恰到好处的距离？

解决方案是创建一个包含 100 多种最常用检查的存储库。每张支票都有自己的大小、颜色和格式。测试人员从存储库中选择一张特定的支票，并将支票的图像文件上传到手机的相机应用程序，“欺骗”它认为它正看着支票。使用手机上的缩放功能，测试人员可以选择模拟支票与手机的距离，确定手机与支票的距离，以记录准确的数据。

### 挑战#2:在不同的设备和版本上执行移动测试，以确保每张图片都有足够的质量来正确读取数据。

一些手机摄像头比其他的更好用。有些版本的智能手机比其他版本的好用。银行使用的移动测试工具必须能够在所有操作系统、设备和版本上运行。否则，银行将不得不购买多种测试工具，并雇佣额外的员工来操作每种工具。任何增加复杂性的事情都会增加出错的可能性。

### 挑战#3:验证正在读取的数据是支票上显示的内容。

一旦拍摄了照片，手机应用程序就会检索以下信息:日期、谁在开支票、支票开给谁、支票号码、付款人的银行和银行账户，最重要的是，金额。没有出错的余地。测试的最佳方式是进行数百次检查，所有检查的信息都存储在数据库中，并通过智能手机、版本和移动操作系统的众多组合对检查进行拍照，记录下它确定每张照片包含的信息。

手机记录的数据将与“真实答案”数据库进行核对。移动测试过程会一直持续下去，直到应用程序在每次执行中的每个细节都尽善尽美。

一旦这些挑战得到解决，存入支票这一艰巨的杂务就变成了一种方便，你可以带着它去银行，也可以不去。