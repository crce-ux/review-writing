# scripts/

**这里是运行版。正本在 [`research-workflow`](https://github.com/crce-ux/research-workflow) 的 `scripts/`**——开发与测试都在那边。

改脚本请改总仓，再同步过来；**不要只改这里**。

| 脚本 | 干什么 | 服务于 |
|---|---|---|
| `check_review_article.py` | **R1 自称与配置自洽**（标题/摘要自称系统综述 → 必须有方法学要素，硬）+ R2 未定项计数（软） | 综述成文 |
| `check_ref_citations.py` | 正文 `[n]` ↔ 文末编号表 **双向核对**（质量核查④） | 综述定稿 |
| `check_skill_structure.py` | 结构校验（官方 Agent Skills 规范） | 自检 |
| `selfcheck.py` | 一条命令自检：结构 + 语法 + 依赖 | 自检 |

### ⚠️ 部署说明（**防漂移**）

`check_ref_citations.py` **在三个 skill 里各有一份运行版**（本 skill / `ai-academic-writing` / `text-self-review`）——
正本都是同一个（`research-workflow/scripts/checks/`）。**改完三处都要同步，用 `cmp` 校验。**

`check_review_article.py` 是本 skill 专有。

### 依赖

全部只用标准库。

## 自检

```bash
python scripts/selfcheck.py --strict
```
