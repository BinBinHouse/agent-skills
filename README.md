# Agent Skills · 我的 AI 工作流合集

> 可复用、可安装、可迭代的 Agent Skills。当前收录 **PPT 美化工作流 v1.2**，专注已有 PPT 单页的美化与可编辑重建，而非自动撰写整套 PPT。

## ✨ PPT 美化工作流 v1.2

**输入：** 一页现有 PPTX，或一张 PPT 截图。  
**输出：** 美化效果图 → 经确认的**可编辑 PPTX** → 实际渲染预览，必要时另附单独高清图标。  
**模式：** “美化重构”与“等比例还原”不同，提示词要说明想要哪一种。

### 真实案例：远景模式

| 美化前：原始页面截图 | 美化后：从可编辑 PPTX 实际导出的预览 |
| :---: | :---: |
| ![原始页面截图](examples/vision-mode/before.png) | ![美化后PPTX的实际渲染效果](examples/vision-mode/after.png) |

[查看案例说明](examples/vision-mode/README.md) · [下载可编辑 PPTX](examples/vision-mode/vision-mode-editable.pptx) · [查看原始图片](examples/vision-mode/before.png) · [查看美化后图片](examples/vision-mode/after.png)

> 案例反映一次具体测试的成果，不保证任何模型均可自动输出完全一致的视觉效果。使用时必须具备 PPTX 编辑/导出能力；高质量图标和效果图可能需要图像生成能力。

### 🎯 特点

- **单页聚焦**：一次处理一页；可以上传多页 PPTX 并指定某页，但不会未经要求把全套重新做一遍。
- **内容锁定**：优先保留数字、原文技术术语、产品名称和核心逻辑。
- **PPTX 优先**：读取真实文字和母版/版式信息；只有图片也可以重建。
- **边角装饰不硬裁**：左上标题方块、页眉分隔线、右上波浪角饰，优先从 PPTX 复用或用原生形状重绘，禁止截图裁角贴回。
- **可编辑优先**：正文、卡片、流程和数值尽量使用原生 PowerPoint 对象；机器人等复杂插画可保留为可替换的独立图片。
- **图标后置**：先确认底板，再按透明背景或真实 RGB 生成统一规格的图标。
- **渲染核验**：检查交付 PPTX 的实际导出预览，及时修复溢出、遮挡和色差。

### 💬 推荐用法

**希望美化而不是简单复刻**

> 使用 `ppt-beautification-workflow` **美化**我上传的这一页 PPT。保留关键内容及现有标题/母版风格；**先输出一张美化效果图**，我确认后再制作**可编辑 PPTX**。禁止从原截图中裁切左上角和右上角模板装饰。最后提供实际渲染 PNG 预览。

**希望尽量按原图还原**

> 使用 `ppt-beautification-workflow` 将这一页 **等比例还原** 为可编辑 PPTX，尽量保持原有布局，不要额外美化。背景装饰优先重绘或复用 PPT 母版，而非边角截图拼贴。

**上传 PPTX 并复用母版**

> 我上传了一套 PPTX，**只美化第 5 页**。优先复用其中的主题、母版、标题样式和已有装饰，保留真实文字。先看视觉效果图，再生成单页可编辑 PPTX。

### 📥 安装

先把本仓库下载到本地。示例：

```bash
git clone https://github.com/BinBinHouse/agent-skills.git
mkdir -p ~/.agents/skills
cp -r agent-skills/skills/ppt-beautification-workflow ~/.agents/skills/
```

以上路径适用于扫描 `~/.agents/skills/` 的 Agent，例如符合相关配置的 Codex 环境。其他客户端请使用其文档指定的 Skills 目录。Skill 文件可跨客户端复用，**但能否生成 PPT、使用 ImageGen、自动验证渲染取决于实际工具权限**。

### 🧰 客户端兼容

| 客户端 | 说明 |
|---|---|
| ChatGPT Work | 可通过已安装的 Skills 选择器调用；和 `@Presentations` 的 Template Gallery 是两类入口 |
| Codex | 支持 Agent Skills；还需要相应文件和图片处理工具 |
| Claude Code | 支持 Agent Skills；功能取决于环境和工具 |
| GitHub Copilot / VS Code | 兼容 Agent Skills 的版本或模式可以使用 |
| 其他支持 `SKILL.md` 的 Agent | 按其目录和工具支持情况使用 |

**中文 `SKILL.md` 不需要强制翻译**，但不同模型的最终美化效果不保证相同。

### 📁 目录

```text
agent-skills/
├── README.md
├── skills/
│   └── ppt-beautification-workflow/
│       ├── SKILL.md
│       ├── README.md
│       └── references/
│           ├── icon-spec.md
│           └── qa-checklist.md
├── examples/
│   └── vision-mode/
│       ├── README.md
│       ├── before.png
│       ├── after.png
│       └── vision-mode-editable.pptx
└── docs/
    └── RELEASE_CHECKLIST.md
```

### 🔏 开源与素材声明

此项目尚未指定开源许可证，请在公开发布前确认 License。`examples/vision-mode` 包含演示中使用的技术和业务描述及插画，**发布者必须先确认内容适合公开且已获得素材使用/再分发授权**。在未完成审查前，请先使用私有仓库。

[查看详细工作流](skills/ppt-beautification-workflow/SKILL.md)