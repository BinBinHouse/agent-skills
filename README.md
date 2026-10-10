# Agent Skills

我的 AI Agent Skills 工作流合集。每个 Skill 都有独立目录、使用说明和示例，可按需安装到支持 Agent Skills 的工具中。

## 📚 Skills

| Skill | 简介 | 版本 |
| --- | --- | --- |
| **[PPT 美化工作流](skills/ppt-beautification-workflow/README.md)** | 美化已有单页 PPTX 或截图，复用母版，生成可编辑 PPTX，并进行图标与渲染检查。 | v1.2 |

点击技能名称即可查看完整功能、使用方法及实际案例。后续新增 Skill，会在这里继续添加。

## 🚀 安装使用

克隆仓库：

```bash
git clone https://github.com/BinBinHouse/agent-skills.git
```

以支持 `~/.agents/skills/` 目录的 Agent 环境为例，安装其中的 PPT 美化 Skill：

```bash
mkdir -p ~/.agents/skills
cp -r agent-skills/skills/ppt-beautification-workflow ~/.agents/skills/
```

其他 AI 客户端可使用自己的 Skill 导入功能，或将目标 Skill 的整个目录放入它要求的位置。工作流能否生成图片、编辑 PPTX 和渲染预览，取决于对应 Agent 的工具能力。

## 📁 仓库结构

```text
agent-skills/
├── README.md                         # 技能索引和安装方法
└── skills/
    └── ppt-beautification-workflow/
        ├── SKILL.md                  # 核心工作流
        ├── README.md                 # 功能、用法与案例
        ├── references/               # 图标规范、质量检查
        └── examples/                 # 实际案例和可编辑 PPTX
```

每个 Skill 自包含，案例和辅助文件均存放在对应 Skill 目录下。