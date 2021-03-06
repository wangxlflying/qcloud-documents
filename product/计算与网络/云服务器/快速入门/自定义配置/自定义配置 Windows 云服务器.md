## 操作场景

本文档介绍 Windows 云服务器的自定义配置方法。
不同于快速配置，自定义配置选项齐全，您可根据需求选择合适的配置。

## 前提条件

 1. 注册账号与选型
新用户需在腾讯云官网进行 [注册](https://cloud.tencent.com/register?s_url=https%3A%2F%2Fcloud.tencent.com%2F)。注册指引可参考 [如何注册腾讯云](https://cloud.tencent.com/doc/product/378/9603) 。
 2. 登录腾讯云官网，选择【云产品】-【计算与网络】-【云服务器】，单击【立即选购】按钮，进入 [云服务器购买页面](https://buy.cloud.tencent.com/buy/cvm) 。
 3. 单击【自定义配置】，进入自定义配置界面。
>! 腾讯云提供**快速配置**和**自定义配置**两种方式，本部分以自定义配置为例说明。相比与快速配置方案，自定义配置提供您更丰富的镜像平台，以及存储、带宽以及安全组等高级设置。若您需要快速配置，可参考[快速配置 Windows 云服务器](https://cloud.tencent.com/document/product/213/2764) 文档进行配置。

![](https://main.qcloudimg.com/raw/d97e1d70d3c71001bbfba4e76a3b153d.png)

## 选择地域与机型
![选择地域与机型](https://main.qcloudimg.com/raw/17ffe6b77c5389a42bb11817de4cc206.png)
 1. **选择计费模式**：包年包月或按量付费（无法购买按量付费云服务器的用户请先进行 [实名认证](https://console.cloud.tencent.com/developer/infomation) ）。更多信息请看 [计费模式说明](https://cloud.tencent.com/document/product/213/2180) 。

 2. **选择地域和可用区**：当您需要多台云服务器时，选择不同可用区可实现容灾效果。
 3. **选择网络类型**
 腾讯云提供基础网络或私有网络两种可选。
  - 基础网络：适合新手用户，同一用户的云服务器内网互通。
  - 私有网络：适合更高阶的用户，不同私有网络间逻辑隔离。

	> **注意：**
	> Windows 云服务器无法作为 [公网网关](/doc/product/215/%E7%BD%91%E5%85%B3#1.-公网网关) 使用，需要公网网关的用户请参考 [Linux 云服务器快速入门](/doc/product/213/2936)。
 4. **选择机型和配置**
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;根据底层硬件的不同，腾讯云目前提供了 **系列 1** 和 **系列 2** （下文也称为 **上一代实例** 和 **当前一代实例** ）两种不同的实例系列，不同的实例系列提供如下实例类型：
- 上一代实例类型：标准型S1，高IO型I1，内存型M1
- 当前一代实例类型：[标准型S2](/doc/product/213/7154)，[高IO型I2](/doc/product/213/7155)，[内存型M2](/doc/product/213/7156)，[计算型C2](/doc/product/213/7157)，[GPU型G2](/doc/product/560)，[FPGA型FX2](/doc/product/565) 

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;为获得最佳性能，我们建议您在新建实例时使用当前一代实例类型。实例类型详细说明，请参见 [实例类型概述](/doc/product/213/7153) 。
> **注意：**
> 不同的地域与可用区下的系列、机型会有所不同。

 5. 单击【下一步：选择镜像】按钮，进入选择镜像页面。

## 选择镜像
![](https://main.qcloudimg.com/raw/7535d02d2b49c8ebb02cf68a70f6ba55.png)
 1. **选择镜像提供方**
腾讯云提供公共镜像、自定义镜像、共享镜像、服务市场，您可参考 [镜像类型](/doc/product/213/4941) 文档进行选择。
对于刚开始使用腾讯云的用户，推荐选择公共镜像，其中包含了正版 Windows 操作系统，后续运行环境自行搭建。
 2. **选择操作系统**：选择 Windows Server 。
 3. **选择镜像版本**
  -  系统内含正版激活，无需额外付费（北美地域除外）。 
  -  适合于运行 Windows 下开发的程序，如 .NET。 
  -  支持 SQL Server 和其他更多数据库（需自行安装）。 
 4. 单击【下一步：选择存储与带宽】按钮，进入选择存储与带宽页面。

## 选择存储与带宽

![存储与带宽](https://main.qcloudimg.com/raw/f98d0da08960cc495258247bcc2c588f.png)
 1. **选择硬盘类型和数据盘大小**
腾讯云提供云硬盘和本地硬盘两种类型。（均默认 50GB 系统盘，系统盘大小任选）
- 云硬盘：采用一盘三备的分布式存储方式，数据可靠性高
- 本地硬盘：处在云服务器所在的物理机上的存储设备，可以获得较低的时延，但存在单点丢失风险。具体对比可以参考 [产品分类](/doc/product/362/2353#.E5.90.84.E7.A7.8D.E5.9D.97.E5.AD.98.E5.82.A8.E8.AE.BE.E5.A4.87.E7.9A.84.E5.AF.B9.E6.AF.94) 。
 2. **选择公网带宽**
 腾讯云提供  按带宽计费  或  按使用流量计费  两种可选。
  - 按带宽计费：选择固定带宽，超过本带宽时将丢包。适合网络波动较小的场景。
  - 按使用流量计费：按实际使用流量收费。可限制峰值带宽避免意外流量带来的费用，当瞬时带宽超过该值时将丢包。适合网络波动较大的场景。
 3. **选择服务器数量**
 4. 选择购买时长与续费方式（仅限包年包月云服务器）。
 5. 单击【下一步：设置安全组和主机】按钮，进入设置安全组和主机页面。

## 设置安全组和主机
![安全组和主机](https://main.qcloudimg.com/raw/642185957e6634f7d3447ebe16c93c56.png)
1. 选择安全组（**确保登录端口 3389 开放**，更多信息见 [安全组](/doc/product/213/%E5%AE%89%E5%85%A8%E7%BB%84)） 。
2. 自定义实例名称：您可选择创建后命名，也可立即命名。
3. 登录信息设置：您可设置密码，也可自动生成。设置的密码可在创建后修改，自动生成的密码将会以站内信方式发送。
4. 单击【高级设置】，可以对主机做更多配置。
![高级设置](https://main.qcloudimg.com/raw/6bec334746e6daab20d01eb969f51b7a.png)
 - 主机名：用户可以自定义设置云服务器操作系统内部的计算机名，云服务器成功生产后可以通过登录云服务器内部查看。
 - 置放群组：根据需要可以将实例添加到置放群组中，提高业务的可用性。具体可参考 [置放群组](https://cloud.tencent.com/document/product/213/15486) 进行设置。
 - 标签：设置标签之后可以对云服务器实现资源的分类管理。具体可参考 [标签](https://cloud.tencent.com/document/product/213/19548) 进行设置。
 - 自定义数据：指定自定义数据来配置实例，既当实例启动的时候运行配置的脚本，如果一次购买多台云服务器，自定义数据会在所有的云服务器上运行。Linux 操作系统支持 Shell 格式，Windows 操作系统支持 PowerShell 格式，最大支持 16KB 原始数据。具体可参考 [自定义数据](https://cloud.tencent.com/document/product/213/17525)。

 > **注意：**
 > 此项配置仅支持windows公有镜像，具体可参考 [cloudbase-init](https://cloud.tencent.com/document/product/213/19670#cloudbase-init)。

5. 单击【立即购买】按钮，完成支付后即可进入 [控制台](https://console.cloud.tencent.com/cvm) 查收您的云服务器。
云服务器创建好后将会收到站内信，内容包括实例名称、公网 IP 地址、内网 IP 地址、登录名、初始登录密码等信息。您可以使用这些信息登录和管理实例，也请尽快更改您的 Windows 登录密码保障主机安全性。

## 登录及连接实例

配置及购买实例后，您购买的实例会显示在控制台的实例列表中，选择您需要登录的实例，单击右侧【登录】，腾讯云推荐您使用RDP方式登录云服务器。如下图所示：
![](https://main.qcloudimg.com/raw/96689027b98d8fc6bfb00036de7a87f8.png)
如果您想通过其他方式登录，请参考[连接及登录 Windows 实例](https://cloud.tencent.com/document/product/213/5435)。

## 格式化与分区数据盘

这里以 Windows 2012 R2 为例进行格式化说明。

### 前提条件
 - 已购买数据盘的用户，需要格式化数据盘才可使用。未购买数据盘的用户可以跳过此步骤。
 - 请确保您已登录到云服务器。

### 格式化数据盘

 1. 通过步骤三介绍的方法登录 Windows 云服务器。
 2. 单击【开始】-【服务器管理器】-【工具】-【计算机管理】-【存储】-【磁盘管理】。
 3. 在磁盘1上右键单击，选择【联机】：
	![](//mc.qcloudimg.com/static/img/1217193557509925a622dcdb81aa2e35/image.png)
 4. 右键单击，选择【初始化磁盘】：
	![](//mc.qcloudimg.com/static/img/94ab92867d77ea69bc803a0b20f2b941/image.png)
 5. 根据分区方式的不同，选择【GPT】或【MBR】，单击【确定】按钮：

### 磁盘分区（可选）

 1. 在未分配的空间处右击，选择【新建简单卷】：
	![](//mc.qcloudimg.com/static/img/a6ca720af2082d7a470ece17a8e13f5d/image.png)
配置及购买CVM实例后，您购买的实例会显示在控制台的实例列表中，选择您需要登录的实例，单击右侧【登录】。

 2. 在弹出的“新建简单卷向导”窗口中，单击【下一步】：
	![](//mc.qcloudimg.com/static/img/10fdcd70b510a57919c6a40cf43452a7/image.png)
![](https://main.qcloudimg.com/raw/876fcf96c4d24635906bd311f223a8a2.png)

 3. 输入分区所需磁盘大小，单击【下一步】：
	![](//mc.qcloudimg.com/static/img/05c8d1425a0208597b1d2c75a9c811b6/image.png)
根据您实例的类型，可以参考以下连接中的方式远程登录CVM实例。
- [连接及登录Windows实例](https://cloud.tencent.com/document/product/213/5435)。

 4. 输入驱动器号，单击【下一步】：
	![](//mc.qcloudimg.com/static/img/737ed569049ad617715efb06fe44e7b2/image.png)

 5. 选择文件系统，格式化分区，单击【下一步】：
	![](//mc.qcloudimg.com/static/img/896cb3f2705fb9fcd04c236b8fb9ec59/image.png)

 6. 完成新建简单卷，单击【完成】：
	![](//mc.qcloudimg.com/static/img/1e257b9c76d80f30b34f612496b8007b/image.png)

 7. 在【开始】中打开【这台电脑】，查看新分区：
	![](//mc.qcloudimg.com/static/img/1cbb4ad1c3c01852a00a1415526a3e12/image.png)

**至此，您已完成 Windows 系统的云服务器的创建和基础配置。**
