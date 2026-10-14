# review-writing

[![Skill self-check](https://github.com/crce-ux/review-writing/actions/workflows/structure.yml/badge.svg)](https://github.com/crce-ux/review-writing/actions/workflows/structure.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**把证据表写成一篇有论点的综述——不是一堆摘要的合集。**

> 🔴 **两句总纲**
> **名头与配置必须自洽**（自称系统综述就得有 PRISMA）。
> **把框架拿掉，剩下不该是一堆摘要。**

```
检索 → 证据表 ──→ ⬅ 综述成文 ──→ 引用审查
(literature-pipeline)           (citation-reviewer)
```

---

## 一、先定性质 ⭐

| 名头 | 方法学透明性 | 你在干什么 |
|---|---|---|
| **叙述性综述** | 建议写「方法与范围」 | **立一个论点** |
| **系统综述** | 🔴 必须有：检索策略 / 纳排 / PRISMA / 去重 | 回答一个**可穷尽**的问题 |
| **范围综述** | 🔴 必须有：检索 + PRISMA-ScR | **绘地图**，不下结论 |

> ⚠️ **名头决定审稿人拿哪把尺子量你。**
> 写「系统综述」却给不出 PRISMA，**比写「叙述性综述」丢分更多**——承诺了没兑现。
> **拿不准就往下写。**

---

## 二、论点驱动，不是文献罗列

**反面**：A 说 X（2021）。B 说 Y（2022）。C 也做了（2023）。

**自检**：**把框架拿掉，剩下的是不是一堆摘要？** 是 → 那是 annotated bibliography。

**三条**：每段第一句是**论断** · 证据按**支持/反证/存疑**分层 · **矛盾正面处理**。

---

## 三、三种结构（选一，不要混）

**时间序**（怎么长出来的）· **主题式**（按维度切，最常用）· **论证式**（立论→反论→综合，最值钱）。

---

## 四、机检

```bash
python scripts/check_review_article.py <综述.md | 目录>   # 自称与配置自洽（R1 硬）
python scripts/check_ref_citations.py --doc <综述.md>      # 正文 [n] ↔ 文末编号表（核查④）
```

| | 查什么 | 性质 |
|---|---|---|
| **R1** | 标题（或摘要自我描述）自称「系统综述 / 荟萃分析 / 范围综述」→ 必须有方法学要素 | 硬 |
| **R2** | 「待核 / 未定来源」标注的行数 | 软，只报数 |

> ⚠️ R1 **不扫摘要里出现的「荟萃分析」**——那是引用别人（「网络荟萃分析显示…」）。
> 实测：不加这条限制，20 篇真稿**误报 3 篇**。

---

## 自检

```bash
python scripts/selfcheck.py --strict
```

---

## 边界

| | 管什么 |
|---|---|
| **本 skill** | **怎么写**一篇综述 |
| `literature-pipeline` | 检索 + 证据表 |
| `ai-academic-writing` | 表达层 / 内容层（去 AI 味等） |
| `citation-reviewer` | 成文之后的引用审查 / 排版 |
| `peer-review` | 审**别人**的稿 |

---

## 来源

R1 那条规则不是想出来的——来自一份**真实核稿报告**（2026-08-08，
《精神分裂症患者体重管理及代谢干预》质量评价）的「高优先问题 1」。

---

## 许可

MIT。
