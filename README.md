# AI MATRIX 产品交付工作流 Skill

这是一个面向产品经理和产品设计协作的 Codex Skill，用于把 AI MATRIX 需求稳定推进到：

```text
范围确认 -> PRD -> HTML 原型 -> Figma 原型 -> 回读交付
```

它保留规格驱动工作的阶段基线和确认门禁，但默认不扩展到研发、测试和发布。

## 适用范围

- AI运维平台
- AI数据中台
- AI服务中台（AI Service Center）
- 数智管理基座
- AI MATRIX 跨平台全局规则

Skill 同时提供产品边界、文件归档、需求池、PRD 追踪、HTML-first 原型和 Figma 官方 MCP 交付规范。

## 安装

```bash
git clone https://github.com/Aidennnnnn-nn/ai-matrix-product-workflow.git \\
  ~/.codex/skills/ai-matrix-product-workflow
```

重新打开 Codex 会话后即可自动识别，也可以显式调用：

```text
使用 $ai-matrix-product-workflow 梳理这批需求的产品归属，并输出 PRD 草稿。
```

```text
使用 $ai-matrix-product-workflow 根据已确认 PRD 输出可评审的 HTML 原型。
```

```text
使用 $ai-matrix-product-workflow 将已确认 HTML 写入目标 Figma 文件并完成回读。
```

## 文件结构

```text
ai-matrix-product-workflow/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── 产品边界与归档规则.md
    ├── PRD与原型阶段门禁.md
    └── Goodwe_UI与Figma交付规范.md
```

## 使用原则

- 当前项目的 `AGENTS.md` 和用户最新指令优先于公共 Skill。
- PRD 未确认，不进入 HTML。
- HTML 未确认，不写入 Figma。
- Figma 使用官方 MCP，保留原生可编辑结构。
- 默认不生成技术方案、研发任务、生产代码、测试和发布材料。
- 公共仓库不保存组织内部链接、账号信息或本机绝对路径。

## 依赖

- 支持 Skills 的 Codex 环境。
- Figma 阶段需要已配置并可用的 Figma 官方 MCP。
- 若环境中同时提供 PRD、Figma 或 HTML 原型 Skill，本 Skill 会按阶段调用它们，但产品边界和门禁仍以本 Skill 为准。
