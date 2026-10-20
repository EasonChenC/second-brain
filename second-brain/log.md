# 操作日志

> 追加式。每次 ingest / query / lint 都记一笔。
>
> **格式约定**：每条以 `## [YYYY-MM-DD] 动作 | 标题` 开头 ——
> 这样可以用最简单的工具取最近几条：`grep "^## \[" log.md | tail -5`

## [2026-10-14] init | 建库

- 按 [[wiki/sources/LLM Wiki（Karpathy 架构说明）]] 的最小方案初始化目录：
  `raw/` + `raw/assets/` + `wiki/{sources,concepts,entities,tools,synthesis}`
- 写入 `agents.md`（操作手册 = 这套系统的 schema）、`index.md`、本日志

## [2026-10-14] ingest | LLM Wiki（Karpathy 架构说明）

- 来源：https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- 新建：`wiki/sources/LLM Wiki（Karpathy 架构说明）`
- 新建：`wiki/concepts/LLM Wiki`
- 新建：`wiki/entities/Andrej Karpathy`
- 新建：`wiki/synthesis/RAG 与 LLM Wiki`
- 源文件留在 `raw/`（raw 不可变，不移动）

## [2026-10-14] query | 什么时候该给这个库加检索

- 问题：「我需要给这个库加向量检索吗？什么时候该加？」
- 查了 `index.md` → 读 `wiki/concepts/LLM Wiki` 与 `wiki/sources/LLM Wiki（Karpathy 架构说明）`
- 答案归档为新页面：`wiki/synthesis/什么时候该给这个库加检索`
- 结论：约 100 来源 / 数百页之前，`index.md` 够用，不需要向量检索基础设施
