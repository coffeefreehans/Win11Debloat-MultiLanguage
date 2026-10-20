# Win11Debloat 多语言版本

[English](README.md) | [简体中文](README_zh.md)

> [!NOTE]
> **原项目声明与改进说明**
> - 本项目基于原开源项目 **[Win11Debloat (by Raphire)](https://github.com/Raphire/Win11Debloat)** 进行修改与扩展。感谢原作者 [Raphire](https://github.com/Raphire) 的杰出工作！
> - **主要新增与优化**：
>   1. **右上角添加语言切换/翻译按钮**：在主界面右上角添加了多语言下拉切换框，默认自动选中系统当前语言，支持各语言即时动态无缝切换。
>   2. **项目全量中文化**：补全缺失键值，提供全量高质量中文界面与中文文档。
>   3. **界面结构优化**：精简了标题栏冗余设置按钮，界面更加简洁整洁。

[![GitHub Release](https://img.shields.io/github/v/release/Raphire/Win11Debloat?style=for-the-badge&label=Latest%20release)](https://github.com/Raphire/Win11Debloat/releases/latest)
[![Join the Discussion](https://img.shields.io/badge/Join-the%20Discussion-2D9F2D?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Raphire/Win11Debloat/discussions)
[![Static Badge](https://img.shields.io/badge/Documentation-_?style=for-the-badge&logo=bookstack&color=grey)](https://github.com/Raphire/Win11Debloat/wiki/)

Win11Debloat 多语言版本 是一个轻量级、简单易用的 PowerShell 脚本工具，无需安装即可快速清理和自定义你的 Windows 体验！你可以用它来卸载预装软件、禁用遥测、移除恼人的界面元素等。无需繁琐地逐项查找系统设置或挨个卸载应用，Win11Debloat 让这一切变得轻松快捷！

该脚本还包含了许多系统管理员和高级用户喜爱的功能，例如强大的命令行界面、支持 Windows 审核模式（Audit Mode）以及为其他 Windows 用户应用更改的功能。你还可以轻松导出和导入偏好设置，以便在所有设备上快速应用相同的配置。详情请参考我们的 [Wiki 文档](https://github.com/Raphire/Win11Debloat/wiki)。

![Win11Debloat 界面](/Assets/Images/menu.png)

#### 这个脚本对你有帮助吗？欢迎请作者喝杯咖啡以支持项目开发：

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M5C6UPC)

## 使用方法

> [!Warning]
> 我们已倾注大量心血确保该脚本不会意外损坏任何系统功能，但使用风险仍需自负！如果遇到任何问题，请在此处提交 [反馈](https://github.com/Raphire/Win11Debloat/issues)。

### 快捷方法

通过 PowerShell 自动下载并运行脚本：

1. 打开 PowerShell 或 Windows 终端（Windows Terminal）。
2. 将以下命令复制并粘贴到 PowerShell 中执行：

```PowerShell
& ([scriptblock]::Create((irm "https://debloat.raphi.re/")))
```

3. 等待脚本自动下载并启动 Win11Debloat。
4. 仔细阅读并根据屏幕提示操作。

此方法支持命令行参数来自定义脚本行为。请点击 [此处](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters) 了解更多信息。

### 常规方法

<details>
  <summary>手动下载并运行脚本</summary><br/>

  1. [下载脚本最新版本](https://github.com/Raphire/Win11Debloat/releases/latest)，并将 .ZIP 压缩包解压到你想要的位置。
  2. 进入解压后的 Win11Debloat 文件夹。
  3. 双击 `Run.bat` 启动脚本。注意：如果控制台窗口立即闪退且没有任何反应，请尝试下面的高级方法。
  4. 接受 Windows UAC 提示，以管理员身份运行脚本（这是脚本正常工作所必需的）。
  5. 仔细阅读并根据屏幕提示操作。
</details>

### 高级方法

<details>
  <summary>手动下载并通过 PowerShell 运行脚本（推荐高级用户使用）</summary><br/>

  1. [下载脚本最新版本](https://github.com/Raphire/Win11Debloat/releases/latest)，并将 .ZIP 压缩包解压到你想要的位置。
  2. 以管理员身份打开 PowerShell 或 Windows 终端。
  3. 输入以下命令临时解除 PowerShell 执行策略限制：

  ```PowerShell
  Set-ExecutionPolicy Bypass -Scope Process -Force
  ```

  4. 在 PowerShell 中导航到解压文件的目录，例如：`cd c:\Win11Debloat`
  5. 运行脚本：

  ```PowerShell
  .\Win11Debloat.ps1
  ```

  6. 仔细阅读并根据屏幕提示操作。

  此方法支持命令行参数来自定义脚本行为。请点击 [此处](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters) 了解更多信息。
</details>

## 功能概览

以下是 Win11Debloat 提供的关键功能和特性概览。访问 [Wiki 文档](https://github.com/Raphire/Win11Debloat/wiki) 获取更多详细信息。

> [!Tip]
> Win11Debloat 所做的所有更改都可以轻松还原，且几乎所有被卸载的应用都可以通过 Microsoft Store 重新安装。有关还原更改的详细说明，请参阅 [Wiki 还原指南](https://github.com/Raphire/Win11Debloat/wiki/Reverting-Changes)。

#### 软件卸载

- 批量卸载各种 Windows 预装内置应用。点击 [此处](https://github.com/Raphire/Win11Debloat/wiki/App-Removal) 了解详情。

#### 隐私与推荐内容

- 禁用遥测、诊断数据收集、活动历史记录、应用启动跟踪以及针对性个性化广告。
- 禁用 Windows 系统中、锁屏界面以及 Microsoft Edge 中的提示、技巧、推荐和推广广告。
- 禁用 Windows 定位服务、应用位置访问权限以及“查找我的设备”位置跟踪。
- 隐藏“设置 > 主页”上的 Microsoft 365 广告，或完全隐藏该主页。

#### AI 功能

- 禁用并移除 Microsoft Copilot、Windows Recall 和 Click to Do 功能。
- 阻止 AI 后台服务（WSAIFabricSvc）自动启动。
- 禁用 Edge、Chrome、画图（Paint）和记事本（Notepad）中的 AI 功能。

#### 系统优化

- 禁用用于分享和移动文件的浮动拖放栏（Drag Tray）。
- 恢复 Windows 10 经典右键上下文菜单。
- 关闭鼠标提高指针精确度（禁用鼠标加速）。
- 禁用连续按 Shift 键触发的粘滞键快捷方式。
- 禁用存储感知（Storage Sense）自动磁盘清理。
- 禁用快速启动以确保彻底关机。
- 禁用 BitLocker 自动设备加密。
- 禁用现代待机（Modern Standby）期间的网络连接以降低电量消耗。

#### Windows 更新

- 阻止 Windows 在更新可用时立即自动获取更新。
- 阻止已登录状态下因系统更新而强制自动重启。
- 禁用与其他电脑共享已下载更新的“传递优化”（Delivery Optimization）。
- 阻止 Windows 自动静默安装设备配套应用（如 LG Monitor App、Alienware Command Center 等）。

#### 外观个性化

- 为系统和应用程序启用深色模式（Dark Mode）。
- 禁用窗口透明、动画效果和视觉动效。
- 隐藏桌面 Windows 聚焦的“了解此图片”快捷图标，或完全关闭桌面聚焦背景。

#### 开始菜单与搜索

- 自定义开始菜单：清理已固定的预装图标、隐藏“推荐”区域、自定义“所有应用”列表样式。
- 禁用开始菜单中的手机连接（Phone Link）移动设备集成。
- 禁用 Windows 搜索中的必应（Bing）网页搜索、Copilot 集成以及 Microsoft Store 推荐应用。

#### 任务栏

- 切换任务栏对齐方式（居中 / 靠左）。
- 自定义或隐藏任务栏按钮（搜索栏、任务视图等）。
- 禁用任务栏与锁屏界面的小组件（Widgets）。
- 在任务栏右键菜单中启用“结束任务”（End Task）选项，快速强制关闭应用。
- 启用“最后活动点击”（Last Active Click）行为：重复点击任务栏图标可在该程序的不同窗口间轮流切换。
- 自定义任务栏按钮的合并与显示方式。

#### 文件资源管理器

- 更改文件资源管理器默认打开位置（主页 / 此电脑 / 下载 / OneDrive）。
- 显示已知文件类型的扩展名。
- 显示隐藏文件、隐藏文件夹及系统驱动器。
- 从导航窗格中隐藏“主页”、“图库”或“OneDrive”项目。
- 隐藏导航窗格中重复显示的可移动磁盘驱动器，仅保留“此电脑”下的条目。
- 将常用文件夹（桌面、下载等）重新添加回文件资源管理器的“此电脑”中。
- 调整盘符显示位置（盘符前置 / 后置）或隐藏盘符。

#### 多任务处理

- 禁用窗口贴靠（Window Snapping）。
- 禁用拖动或贴靠窗口时的贴靠辅助（Snap Assist）和贴靠布局（Snap Layout）推荐。
- 自定义贴靠窗口或按 Alt+Tab 时是否显示浏览器标签页。

#### Windows 可选功能

- 开启 Windows 沙盒（Windows Sandbox）：轻量级隔离桌面环境，安全测试未知软件。
- 开启适用于 Linux 的 Windows 子系统（WSL）：直接在 Windows 上运行原生 Linux 环境。

#### 其他功能

- 禁用 Xbox Game Bar 集成及游戏/录屏后台。在卸载 Xbox Game Bar 后还可阻止弹出 `ms-gamingoverlay`/`ms-gamebar` 报错。
- 移除 Brave 浏览器中的推广内容（AI、加密货币、新闻等）。

#### 高级特性

- 支持[为其他 Windows 用户应用更改](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#running-as-another-user)（不仅限当前用户）。
- 提供 [Sysprep 模式](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#sysprep-mode) 以将更改应用到 Windows 默认用户配置文件（Default Profile），确保之后新建的所有新用户都会自动应用该配置。

## 贡献

我们非常欢迎各种形式的贡献！请参阅我们的 [贡献指南](https://github.com/Raphire/Win11Debloat/blob/master/.github/CONTRIBUTING.md) 了解如何开始参与开发。

## 开源协议

Win11Debloat 采用 MIT 许可证开源。详情请参阅 LICENSE 文件。
