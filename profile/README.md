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
  <a href="#插件">插件</a> ·
  <a href="#安装">安装</a> ·
  <a href="#迁移状态">迁移状态</a> ·
  <a href="#相关">相关</a>
</p>

---

## 关于

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（DSH）是可扩展的 agent harness。这个组织用来收纳 Thatgfsj 维护的 DSH 插件与技能：输入预测、情绪可视化、Android 实例、安装迁移、上下文压缩、Trae API 适配等。

目标很简单：**插件有独立仓库、独立 README、可单独安装**；不再散落在个人账号的时间线里。

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
- [dsh-plugin-skills](https://github.com/Thatgfsj/dsh-plugin-skills) 是 DSH 插件构建 / 技能编写指南，仍留在个人账号。

## 相关

- 个人主页：[github.com/Thatgfsj](https://github.com/Thatgfsj)
- 个人网站：[thatgfsj.xyz](https://www.thatgfsj.xyz/)
- 项目索引：[thatgfsj.xyz/projects](https://www.thatgfsj.xyz/projects/)

---

<p align="center">
  <sub>组织 Profile README · 横幅是仓库内自绘 SVG，随 GitHub 主题切换明暗两版。</sub>
</p>

<p align="center"><a href="#readme-top">↑ 回到顶部</a></p>
