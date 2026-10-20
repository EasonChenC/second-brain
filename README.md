# 第二大脑 · Second Brain

一套由 LLM 持续维护的常驻知识库。**让 AI 把每一份新材料编译成互相链接的 wiki 页面**，长期累积成一张可读、可查、可回溯的知识网络。

设计来自 Andrej Karpathy 的 [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
概念：不去原始文档里现查，而是维护一份一直在进化的 wiki。

---

## 三层结构

| 层 | 目录 | 内容 | 谁写 |
|---|---|---|---|
| **原始层** | `second-brain/raw/` | 网页、文章、视频转写的原样副本，**不可变** | 人（剪藏工具） |
| **Wiki 层** | `second-brain/wiki/` | 摘要、概念、实体、工具、综述 | **只有 AI 写**，人只读 |
| **Schema 层** | `second-brain/agents.md` | 结构约定与工作流 | 人和 AI 共同演进 |

---

## 目录

```
第二大脑/
├── README.md                    ← 本文件
├── second-brain/                ← 知识库本体
│   ├── raw/                     ← 原始素材（不可变）
│   │   └── assets/              ← 本地图片等附件
│   ├── wiki/
│   │   ├── sources/             ← 每个来源一页：它是什么、讲了什么
│   │   ├── concepts/            ← 概念 / 主题
│   │   ├── entities/            ← 人物、公司、组织
│   │   ├── tools/               ← 工具、产品
│   │   └── synthesis/           ← 综述、对比、阶段性结论
│   ├── index.md                 ← 全库目录（内容导向，先读这个）
│   ├── log.md                   ← 操作日志（时间导向，只追加）
│   └── agents.md                ← 操作手册 = schema
└── obsidian插件模版/            ← 配套工具
    ├── Obsidian-1.14.4.exe      ← 阅读器（未入库，见 .gitignore）
    └── 网页内容获取-clipper.json ← Web Clipper 配置：一键剪藏到 raw/
```

