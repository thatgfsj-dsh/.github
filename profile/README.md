<a name="readme-top"></a>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/thatgfsj-dsh/.github/main/profile/assets/banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/thatgfsj-dsh/.github/main/profile/assets/banner-light.svg">
    <img alt="thatgfsj-dsh — DeepSeek Harness 插件与技能" src="https://raw.githubusercontent.com/thatgfsj-dsh/.github/main/profile/assets/banner-light.svg" width="100%">
  </picture>
</p>

<h1 align="center">thatgfsj-dsh</h1>

<p align="center">
  Thatgfsj 的 DeepSeek Harness 插件与技能组织。把分散在个人账号的 DSH 插件收在一起，方便安装、检索与协作。
</p>

<p align="center">
  <a href="https://github.com/thatgfsj-dsh?tab=repositories"><img alt="DSH plugins & skills" src="https://img.shields.io/badge/DSH-plugins%20%26%20skills-b45309?style=flat-square"></a>
  <a href="#迁移状态"><img alt="status: migrating" src="https://img.shields.io/badge/status-migrating-d08a35?style=flat-square"></a>
</p>

<p align="center">
  <a href="#关于">关于</a> ·
  <a href="#核心-skills">核心 skills</a> ·
  <a href="#插件">插件</a> ·
  <a href="#安装">安装</a> ·
  <a href="#迁移状态">迁移状态</a> ·
  <a href="#相关">相关</a>
</p>

---

## 关于

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（DSH）是可扩展的 agent harness。这个组织用来收纳 Thatgfsj 维护的 DSH 插件与技能：输入预测、情绪可视化、Android 实例、安装迁移、上下文压缩、Trae API 适配等。

目标很简单：**插件有独立仓库、独立 README、可单独安装**；不再散落在个人账号的时间线里。

## 核心 skills

技能（`SKILL.md`）和插件是两类东西：插件是运行时加载的代码，技能是教 agent 做事的一套可复用流程与知识。装进用户级技能目录 `~/.dsh/skills` 后，agent 会按需加载对应技能。

| 技能包 | 用途 |
|---|---|
| [dsh-plugin-skills](https://github.com/thatgfsj-dsh/dsh-plugin-skills) | DSH 插件构建 / 魔改指南 + 技能编写指南；按适配的 dsh 版本分目录（当前 `0.2.2-rc.1`），附带由本机安装产物生成的内部结构地图（服务 / 事件 / slot / 包） |

安装：

```sh
git clone https://github.com/thatgfsj-dsh/dsh-plugin-skills.git
cd dsh-plugin-skills
bash scripts/install.sh --dry-run   # 看会装哪个版本、装什么
bash scripts/install.sh             # 默认装与本机 `dsh --version` 同名的版本目录
```

装完新开一个会话，即可在技能目录里看到 `dsh-plugin-construction` 与 `dsh-skill-authoring`；选版本 = 选与你的 `dsh --version` 一致的目录。

## 插件

| 插件 | 用途 | 语言 |
|---|---|---|
| [dsh-phone](https://github.com/thatgfsj-dsh/dsh-phone) | 在后端跑 Android 实例，经浏览器右侧栏呈现，注册 9 个 `phone_*` 工具 | TypeScript |
| [dsh-emotion-analyzer](https://github.com/thatgfsj-dsh/dsh-emotion-analyzer) | 本地 ONNX 给每条回复打情绪分，投影进会话并注入可拖拽悬浮框 | TypeScript |
| [dsh-composer-assist](https://github.com/thatgfsj-dsh/dsh-composer-assist) | 根据对话预测下一条输入，支持草稿补全、提示词润色与 Tab 采用（fork；上游 [Lphehe/dsh-composer-assist](https://github.com/Lphehe/dsh-composer-assist)） | JavaScript |
| [dsh-trae-api](https://github.com/thatgfsj-dsh/dsh-trae-api) | 把 Trae Work CN 的额度转成本地 OpenAI / Anthropic 兼容 API（fork；上游 [Wang-JQ77/dsh-trae-api](https://github.com/Wang-JQ77/dsh-trae-api)） | JavaScript |
| [dsh-migrate](https://github.com/thatgfsj-dsh/dsh-migrate) | 把一份 DSH 安装打包成 zip，迁移到另一台电脑再释放 | JavaScript |
| [dsh-Compress-codex](https://github.com/thatgfsj-dsh/dsh-Compress-codex) | Codex 风格的上下文压缩后端，替代原生 compaction-basic 策略层 | JavaScript |
| [dsh-ops](https://github.com/thatgfsj-dsh/dsh-ops) | DSH 底层操作工具（fork；主仓库在 [T-Auto/dsh-ops](https://github.com/T-Auto/dsh-ops)） | JavaScript |

## 安装

各插件按各自仓库 README 安装。DSH 插件通常通过 profile 安装，例如：

```sh
dsh plugin --profile web add <包名 / 本地目录 / tgz>
```

版本兼容性、前置依赖与验证步骤，以每个仓库的 README 为准；DSH 版本迭代较快，安装前先确认插件声明的 `engines.dsh`。

## 迁移状态

- 个人账号里的 DSH 插件正在迁入本组织；旧链接可能仍可用，但新地址以本页为准。
- `dsh-ops`、`dsh-trae-api`、`dsh-composer-assist` 在组织内是 fork，主开发仓库/上游见各仓库说明；`dsh-ops` 的主仓库仍在 [T-Auto/dsh-ops](https://github.com/T-Auto/dsh-ops)。
- [dsh-plugin-skills](https://github.com/thatgfsj-dsh/dsh-plugin-skills) 已从个人账号迁入本组织，作为本组织的核心技能包维护。

## 相关

- 个人主页：[github.com/Thatgfsj](https://github.com/Thatgfsj)
- 个人网站：[thatgfsj.xyz](https://www.thatgfsj.xyz/)
- 项目索引：[thatgfsj.xyz/projects](https://www.thatgfsj.xyz/projects/)

---

<p align="center">
  <sub>组织 Profile README · 横幅是仓库内自绘 SVG，随 GitHub 主题切换明暗两版。</sub>
</p>

<p align="center"><a href="#readme-top">↑ 回到顶部</a></p>
