# Tour of Light Point · 光点之旅

> 《光点之旅》（Tour of Light Point，简称 **TOLP**）的开源游戏仓库。

本仓库包含《光点之旅》的完整游戏工程源码，基于 **GDevelop** 引擎开发，采用 **MIT License** 开源发布。任何人都可以查阅、学习、修改、分发本项目的代码与工程资源。

- **开发商**：MogroWang Studio
- **游戏引擎**：[GDevelop](https://gdevelop.io/)（工程版本 5.6.287）
- **许可证**：MIT
- **发行渠道**：GitHub Releases（提供可由 TOLP Launcher 直接运行的游戏文件）

---

## 关于《光点之旅》

《光点之旅》是由 MogroWang Studio 制作的一款独立游戏。项目以「光点」为核心意象，围绕探索与旅程展开。

> 说明：本 README 仅描述仓库与开发方式；关于玩法、剧情与美术设定的详细介绍，请见官方发布页与游戏内说明。

---

## 技术栈

| 项目 | 说明 |
| --- | --- |
| 游戏引擎 | GDevelop 5（工程文件版本 5.6.287） |
| 目标平台 | GDevelop JS Platform（Web / 桌面封装） |
| 工程格式 | 分文件夹工程（`folderProject`），主文件 `TOLP.json` |
| 基准分辨率 | 1920 × 1080 |
| 帧率策略 | 最高 60 FPS，最低 20 FPS |
| 渲染设置 | MSAA 抗锯齿、线性缩放、运行时自适应分辨率 |
| 版本管理 | Git（`.gitattributes` 统一 LF 换行规范化） |

---

## AI 协作开发模式

本项目**拥抱 AI 技术**，但 AI 不是唯一作者。我们采用的是一条明确的人机协作流水线：

1. **AI 承担高效率的重复性工作** —— 素材整理、样板代码与事件表（Events Sheet）初稿、文档撰写、重构建议等。
2. **人类负责创意与设计决策** —— 玩法框架、关卡节奏、视觉风格、叙事表达、数值平衡等核心设计由人工主导。
3. **代码审查不可跳过** —— AI 产出的每一份代码、事件逻辑与工程改动，都必须经过人工审查后方可合入主分支。审查关注可维护性、逻辑正确性、性能开销与引擎规范一致性。

我们的立场很明确：**AI 提升产能，人工守住质量**。仓库中的每一次提交，都代表有人为其正确性负责。

---

## 仓库结构

```
TOLP/
├── TOLP.json              # GDevelop 工程主文件（项目配置、全局对象、变量）
├── layouts/               # 场景（Layout）定义，按文件夹拆分存储
├── LICENSE                # MIT 许可证
├── README.md              # 本文件
└── .gitattributes         # 换行符与文本文件规范化规则
```

工程采用 GDevelop 的 **folder project** 模式：场景、外部事件、资源等可以按文件夹拆分，便于多人协作与版本控制时降低合并冲突。

---

## 本地运行与开发

### 前置条件

- 安装 [GDevelop](https://gdevelop.io/download) 桌面版，建议版本 **5.6.x 或更新**（旧版本可能无法正确读取 5.6.287 格式的工程）。

### 打开工程

1. 克隆仓库：

   ```bash
   git clone https://github.com/MogroWangStudio/TOLP.git
   cd TOLP
   ```

2. 使用 GDevelop 打开根目录下的 `TOLP.json`。
3. 在 GDevelop 内点击「预览」（Preview）即可本地试玩。

### 直接获取可运行的游戏

无需配置开发环境。请前往本仓库的 **Releases** 页面下载游戏文件，并通过 **TOLP Launcher** 启动。

---

## Release 与 TOLP Launcher

本项目的 GitHub Releases 将发布**可由 TOLP Launcher 直接运行的游戏文件**。

- 每个 Release 对应一个可运行的构建版本，建议下载最新的稳定版本。
- 游戏文件的目录结构与命名遵循 TOLP Launcher 的约定，请勿随意改动文件夹层级或主入口文件名，否则可能导致启动失败。
- 若需要参与开发而非游玩，请按上一节从源码运行。

---

## 参与贡献

欢迎提交 Issue 与 Pull Request：

1. 提交前请先搜索现有 Issue，避免重复。
2. 功能性改动建议先开 Issue 讨论设计方向，再提交代码。
3. 请保持工程内命名风格与结构约定一致，不要提交与本次改动无关的格式化差异。
4. 保留 `.gitattributes` 的 LF 规范化设置，避免整文件换行符变更造成的噪音 diff。
5. 所有 PR 都需通过人工代码审查后方可合入。

---

## 开发团队

**MogroWang Studio** —— 独立游戏开发团队，负责《光点之旅》的设计、开发与发行。

- GitHub 组织：[@MogroWangStudio](https://github.com/MogroWangStudio)

---

## 许可证

本项目以 [MIT License](./LICENSE) 开源发布。

Copyright (c) 2026 MogroWang

你可以自由使用、修改、分发本项目，包括商业用途，但需保留原始版权声明与许可声明。软件按「现状」提供，不附带任何形式的担保。

---

<sub>Tour of Light Point · 光点之旅 — Made with GDevelop by MogroWang Studio</sub>
