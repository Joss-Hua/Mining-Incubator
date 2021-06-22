
# How to join the Filecoin Miner Incubation Center

## 申请流程

### 1.申请审核

Filecoin矿工孵化中心第一阶段为2021/07/25 - 2021/09/30，提供了15个名额。请于07/18前填写并提交[申请表](http://venusteam.mikecrm.com/1lmpQtj)，申请表内容应详细且真实，以便尽快审核。值得注意的是，我们将与每一个提交申请的矿工取得联系（通过您提供的联系方式）并反馈结果，一旦通过申请，您的节点将在2021/07/25之后尽快接入孵化中心，您并不需要等待其他矿工的审核结果。关于Filecoin矿工孵化中心的更多信息请查看[这里](./README.md)。

### 2.接入相关接口
xxx

### 3.网关xxx
xxx

### 4.xxx
xxx

## 相关文档
以上流程所使用的程序来自开源的[Lotus](https://github.com/filecoin-project/lotus/releases)及[Venus](https://github.com/filecoin-project/venus/releases)代码，部署或接入过程可能会碰到多种问题，比如组件、网络、网关、参数、命令、硬件等。

矿工可以进一步了解[Venus常用命令](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Commands.md)、[venus-messager如何使用](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/How%20to%20use%20venus%20messager.md)、[Venus远程钱包](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Venus%20wallet.md)、[Venus多签钱包](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Multisig-Wallet.md)以及[venus-wallet如何使用](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/How-To-Use-Wallet.md)等，如需[更多文档](https://github.com/filecoin-project/venus-docs)可提交PR或Issue，共同完善。同时，Venus提供了[常见问题指南](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Troubleshooting-%26-FAQ.md)可以帮组你解决一些问题。

</br>

## 必要资源
您需要通过[venus-sealer](https://github.com/filecoin-project/venus-sealer)做数据封装相关任务的管理，通过[venus-woker](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Venus-Worker.md)与venus-sealer的配合将更好的执行封装任务。

理论上[venus-wallet](https://github.com/filecoin-project/venus-wallet)可以运行在共享组件部分，但基于矿工的安全性需求，venus-wallet可以由矿工独立部署，就像图1那样。

</br>

## 人员支持
接入孵化器的操作过程如果遇见更多问题，可联系[Venus Team](https://filecoinproject.slack.com/archives/CEHHJNJS3) - [@hunjixin](https://filecoinproject.slack.com/team/USSCQ7WGM)、[@moliujian](https://filecoinproject.slack.com/team/UP4KR85FT)，我们将尽多的给予咨询、指导等支持。
