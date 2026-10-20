---
type: tool
title: Obsidian
sources: ["LLM Wiki（Karpathy 架构说明）"]
updated: 2026-10-16
---

# Obsidian

**是什么**：一个 markdown 的组织器和阅读器。**本质就是个文件夹** ——
你的笔记就是磁盘上一堆 `.md` 文件，Obsidian 只是给你一个好看的读写界面 + 链接/检索能力。
免费。官网 https://obsidian.md/

## 在这套系统里的位置

它不是"笔记软件"，是**你观察 AI 在做什么的可见层**。

Karpathy 的类比：**Obsidian 是 IDE，LLM 是程序员，wiki 是代码库。**
实践方式就是——**LLM agent 开在一边，Obsidian 开在另一边**，LLM 根据对话改文件，
你在 Obsidian 里实时看结果：点链接、看关系图、读被更新的页面。

## 用得到的功能

| 功能 | 干什么 |
|---|---|
| **Graph view（关系图）** | 看 wiki 的形状 —— 什么连着谁、哪些是枢纽、哪些是孤儿。用得越久越密 |
| **Web Clipper** | 浏览器插件，网页转 markdown，**能自动抓 YouTube 完整字幕**。官网 https://obsidian.md/clipper |
| **附件本地化** | 设置 → Files and links → 把附件目录指到 `raw/assets/`；再给"下载当前文件的附件"绑快捷键（如 Ctrl+Shift+D），剪藏完按一下，图片全落地。这样 LLM 能直接看图，而不是依赖可能失效的外链 |
| **Marp** | 插件，用 markdown 做幻灯片，可以直接从 wiki 内容生成演示 |
| **Dataview** | 插件，对页面 frontmatter 跑查询，生成动态表格/列表（前提是 LLM 给页面写了 YAML frontmatter） |

## 一个重要的观察

**整个库就是一堆 markdown 文件组成的 git 仓库。** 版本历史、分支、协作全都免费得到 ——
这是"知识存成纯文本"而不是存进某个 SaaS 的最大回报。

## 关于这个库

这个库就是标准的 Obsidian vault 格式。**不装 Obsidian 也能用**（agent 直接读写 markdown 就行）；
装了之后「打开文件夹作为库」指到库根目录即可，`[[...]]` 链接和关系图立刻能用。

## 相关页面

- [[wiki/concepts/LLM Wiki]]
