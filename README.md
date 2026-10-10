# Agent Skills

我的 AI Agent Skills 工作流合集。每个 Skill 都放在 `skills/` 下的**独立目录**中，包含自己的 `SKILL.md`、使用说明和按需提供的示例素材。

这个仓库用于**集中管理、安装和更新多个 Skill**。仓库首页只提供索引与通用安装方法；详细使用流程、测试案例和注意事项，请进入对应 Skill 查看。

## 📚 Skill 列表

| Skill | 功能简介 | 版本 | 详细说明 |
| --- | --- | --- | --- |
| **[PPT 美化工作流](skills/ppt-beautification-workflow/)** | 对已有单页 PPTX 或 PPT 截图先进行美化，再重建可编辑 PPT；支持复用母版、图标补全及渲染检查 | **v1.2** | [使用方法与案例](skills/ppt-beautification-workflow/README.md) · [SKILL.md](skills/ppt-beautification-workflow/SKILL.md) |

以后新增 Skill，只需在 `skills/` 中新增同级目录，并在本表增加一行，无需改变其他 Skill 的内容。

## 🚀 获取与安装

本仓库目前是 **Private**，需要对仓库有访问权限的 GitHub 账号才能拉取。

```bash
git clone git@github.com:BinBinHouse/agent-skills.git
```

以支持扫描 `~/.agents/skills/` 的 Agent（例如相应配置的 Codex）为例，安装一个指定 Skill：

```bash
mkdir -p ~/.agents/skills
cp -r agent-skills/skills/ppt-beautification-workflow ~/.agents/skills/
```

其他客户端请根据自身文档选择 Skills 安装目录或上传 `SKILL.md` 所在文件夹。**安装了工作流不代表自动具有图片生成、PowerPoint 编辑或渲染能力**；具体能力取决于目标 Agent 提供的工具。

## 📁 组织原则

```text
agent-skills/
├── README.md
└── skills/
    └── ppt-beautification-workflow/
        ├── SKILL.md
        ├── README.md
        ├── references/
        └── examples/
```

- **仓库首页**：仅列出 Skill、用途与安装方式。
- **各 Skill/README.md**：功能、调用方法、示例、适用范围与注意事项。
- **各 Skill/SKILL.md**：Agent 实际执行指令。
- **references/**：仅该 Skill 使用的额外规范。
- **examples/**：仅该 Skill 使用的案例图片和输出文件。

## 🔒 可见性与许可

本仓库目前为 **Private**，尚未指定开源许可证。仓库中的业务案例或第三方素材在公开前应单独检查内容和授权。