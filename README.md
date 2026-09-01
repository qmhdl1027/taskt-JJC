# taskt

> 📦 **JJC 定制版**：本仓库为 **JJC** 维护的定制版本，基于上游 [`saucepleez/taskt`](https://github.com/saucepleez/taskt) 同步，并补全了中文文档与快速上手指南，方便中文用户使用。

![taskt](https://i.imgur.com/gBpKDg0.png)

**taskt**（原名 sharpRPA）是一款真正免费、易用且开源的**流程自动化（RPA）客户端**，基于 .NET Framework 与 C# 开发。你无需编写应用程序代码，即可通过拖拽式设计器构建并运行流程自动化。

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/saucepleez/taskt)

| 分支 | 构建状态 |
| --- | --- |
| master | [![Build Status](https://dev.azure.com/taskt/taskt/_apis/build/status/saucepleez.taskt?branchName=master)](https://dev.azure.com/taskt/taskt/_build/latest?definitionId=1&branchName=master) |
| development-branch | [![Build Status](https://dev.azure.com/taskt/taskt/_apis/build/status/saucepleez.taskt?branchName=development-branch)](https://dev.azure.com/taskt/taskt/_build/latest?definitionId=1&branchName=development-branch) |

![taskt-main-screen](https://i.imgur.com/tHTy6eh.gif)

---

## 📖 项目简介

taskt 让你能够自动化枯燥重复的工作，通过打造一支「数字员工」队伍来执行基于规则的自动化任务。**没有 API？没问题！** 内置「所见即所得」的机器人设计器，包含数十种自动化命令；同时附带元素录制器与屏幕录制器，可记录并回放脚本化自动化流程。

![Click. Configure. Done.](https://i.imgur.com/gzYEdRG.png)

---

## ✨ 功能特性

- 🆓 **完全免费 & 开源**：基于 Apache 2.0 协议，个人与商业用途均可免费使用
- 🖱️ **拖拽式设计器**：所见即所得，无需编写代码即可设计自动化流程
- 🎥 **录制回放**：内置元素录制器与屏幕录制器，可记录并回放操作
- 🌐 **网页 & 桌面自动化**：模拟人工操作，覆盖 Web 与桌面应用
- 🧩 **.NET 扩展**：可直接调用现有 .NET DLL 与服务，支持「自定义代码」命令在运行时编译
- 📊 **丰富命令**：启动 / 停止进程、运行 VB 与 PowerShell 脚本、操作 Excel、OCR 识别（需安装 OneNote）等
- 🖥️ **服务端编排（可选）**：通过 tasktServer 远程发布与执行任务，监控机器人健康状态
- 🔧 **流程管理**：可启动 / 停止进程、启动 VB 与 PowerShell 脚本、操作 Excel 工作簿等

---

## 🛠️ 安装步骤

### 系统要求

#### 最低配置
- Windows 7 / 8.1 / 10 / 11 / Server 2012 / 2016 / 2019（32 位与 64 位）
- 内存 1 GB
- 磁盘空间 200 MB
- 1 vCPU
- **.NET Framework 4.8**
- ⚠️ Windows 7、8.1、Server 2012、Server 2016 已不再受到官方支持

#### 推荐配置
- Windows 10 / 11 / Server 2019（32 位与 64 位）
- 内存 4 GB
- 磁盘空间 1 GB
- 2 CPU
- **.NET Framework 4.8**

### 安装方式

1. **安装 .NET Framework 4.8**
   前往 [微软官网](https://dotnet.microsoft.com/download/dotnet-framework/net48) 下载并安装 .NET Framework 4.8（若系统已自带可跳过）。

2. **下载 taskt**
   点击 [此处](https://github.com/qmhdl1027/taskt-JJC/releases/latest) 获取最新已签名版本。

3. **解压运行**
   将压缩包解压到任意文件夹，双击 `taskt.exe` 即可启动。
   - 首次启动会询问是否创建 `scripts` 文件夹用于存储脚本
   - 同时会复制并部署示例文件，方便快速体验

---

## 🚀 快速开始

1. 双击 `taskt.exe` 启动程序
2. 在左侧命令面板中，拖拽需要的自动化命令到中间的设计画布
   ![Configuring Tasks](https://i.imgur.com/ufvgfn2.gif)
3. 选中命令，在右侧属性面板中配置参数（如元素定位、输入文本等）
   ![How does taskt work?](https://i.imgur.com/TxrH6YH.png)
4. 点击「运行」，taskt 将按脚本顺序自动执行
   ![Recorder](https://i.imgur.com/EpiwkPj.gif)
5. 可使用元素录制器 / 屏幕录制器，直接录制操作生成脚本

> 💡 完整命令列表可点击 [此处](https://github.com/rcktrncn/taskt-wiki/blob/master/automation-commands.md) 查看。

---

## 💡 taskt 能做什么？

taskt 可在 **Web 与桌面应用**上执行自动化，模拟人工操作。无论是表单数据录入、报表生成，还是批量文件处理，都能轻松应对。
![What can taskt do?](https://i.imgur.com/FTMRTi8.png)

- 启动 / 停止进程
- 运行 VB 与 PowerShell 脚本
- 直接操作 Excel 工作簿
- OCR 文字识别（需安装 OneNote）
- 调用现有 .NET DLL 与服务，运行时编译自定义代码

---

## 🖥️ 服务端组件（可选）

> **当前处于 ALPHA 阶段**

通过可选的 [tasktServer](https://github.com/saucepleez/tasktServer) 组件，你可以远程发布与执行任务，监控机器人整体健康状况，并查看机器人工作效率指标。
![tasktServer](https://camo.githubusercontent.com/34e5fd47f19e4d93dcd44e38e3205d299a9d0827/68747470733a2f2f692e696d6775722e636f6d2f644649454d77792e706e67)

---

## 🔧 从源码构建

如需自行编译，从 `master` 分支获取最新代码：

```bash
git clone https://github.com/qmhdl1027/taskt-JJC
cd taskt-JJC
# 使用 Visual Studio 打开解决方案并编译
# 或直接通过 MSBuild 构建
```

---

## 💰 费用与协议

taskt 对**个人与商业用途均免费**。基于 **Apache 2.0** 协议开源，详见 `LICENSE.md`。

作为一个社区驱动的项目，taskt 的目标是让无论大小的用户都能构建并部署流程自动化。

---

## 🤝 参与贡献

欢迎提出功能建议或报告 Bug / Issue：
[![Open New Issue](https://img.shields.io/badge/Open-New%C2%A0Issue-blue.svg)](https://github.com/qmhdl1027/taskt-JJC/issues/new)
[![Chat on Gitter](https://img.shields.io/badge/Chat-On%C2%A0Gitter-green.svg)](https://gitter.im/taskt-rpa/Lobby)

---

⭐ 如果对你有帮助，欢迎 Star 支持！
