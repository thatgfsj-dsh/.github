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
  Thatgfsj 的 DeepSeek Harness 插件与技能组织：<strong>10 个插件</strong> + <strong>1 个技能包</strong>，共 <strong>13 个公开仓库</strong>。
</p>

<p align="center">
  <a href="https://github.com/thatgfsj-dsh?tab=repositories"><img alt="DSH plugins &amp; skills" src="https://img.shields.io/badge/DSH-plugins%20%26%20skills-b45309?style=flat-square"></a>
  <a href="#插件"><img alt="plugins: 10" src="https://img.shields.io/badge/plugins-10-0f766e?style=flat-square"></a>
  <a href="#核心-skills"><img alt="skills: 1" src="https://img.shields.io/badge/skills-1-1d4ed8?style=flat-square"></a>
  <a href="#仓库构成"><img alt="repos: 13" src="https://img.shields.io/badge/repos-13-6b7280?style=flat-square"></a>
</p>

<p align="center">
  <a href="#关于">关于</a> ·
  <a href="#核心-skills">核心 skills</a> ·
  <a href="#插件">插件</a> ·
  <a href="#安装">安装</a> ·
  <a href="#仓库构成">仓库构成</a> ·
  <a href="#相关">相关</a>
</p>

---

## 关于

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（DSH）是可扩展的 agent harness。这个组织用来收纳 Thatgfsj 维护的 DSH 插件与技能：会话删除与回收站、输入预测、情绪可视化、Android 实例、整机迁移、上下文压缩、棋类对弈、Trae API 适配等。

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

共 **10 个插件**：7 个原创 + 3 个上游 fork。版本号取自各仓库默认分支的 `package.json`（核对日期 2026-11-10）。

### 原创插件

| 插件 | 用途 | 语言 | 版本 | 获取方式 |
|---|---|---|---|---|
| [dsh-session-delete](https://github.com/thatgfsj-dsh/dsh-session-delete) | 侧栏会话行内删除 + 插件设置页回收站（可还原 / 彻底删除） | JavaScript | 0.1.9 | 仓库目录 |
| [dsh-migrate](https://github.com/thatgfsj-dsh/dsh-migrate) | 把一份 DSH 安装打包成单个 zip（导出），迁到另一台电脑释放（导入） | JavaScript | 0.1.2 | [Release](https://github.com/thatgfsj-dsh/dsh-migrate/releases/latest) tgz / zip |
| [dsh-xiangqi](https://github.com/thatgfsj-dsh/dsh-xiangqi) | 象棋 / 五子棋 / 国际象棋对弈站 + agent 走子工具 + 一键内网穿透 + Markdown 记谱 | JavaScript | 0.4.0 | 仓库目录 |
| [dsh-disable-pwsh](https://github.com/thatgfsj-dsh/dsh-disable-pwsh) | 不挑平台 / 预设 / 会话，无条件把 `pwsh` 工具从模型可见工具中移除 | JavaScript | 0.1.1 | 仓库目录 |
| [dsh-phone](https://github.com/thatgfsj-dsh/dsh-phone) | 在后端跑 Android 实例，经浏览器右侧栏呈现，注册 9 个 `phone_*` 工具 | TypeScript | 0.4.1 | [Release](https://github.com/thatgfsj-dsh/dsh-phone/releases/latest) tgz |
| [dsh-emotion-analyzer](https://github.com/thatgfsj-dsh/dsh-emotion-analyzer) | 本地 ONNX 给每条回复打情绪分，投影进会话并注入可拖拽悬浮框 | TypeScript | 0.2.2 | 仓库目录（Release 暂未附资产） |
| [dsh-Compress-codex](https://github.com/thatgfsj-dsh/dsh-Compress-codex) | Codex 风格的上下文压缩后端，替代原生 compaction-basic 策略层 | JavaScript | 0.1.0 | 仓库目录 |

### 上游 fork

| 插件 | 用途 | 语言 | 版本 | 获取方式 |
|---|---|---|---|---|
| [dsh-composer-assist](https://github.com/thatgfsj-dsh/dsh-composer-assist) | 上下文感知的输入预测 / 草稿补全 / 润色，Tab 采用但不发送（上游 [Lphehe/dsh-composer-assist](https://github.com/Lphehe/dsh-composer-assist)） | JavaScript | 0.1.1 | 上游 [Release](https://github.com/Lphehe/dsh-composer-assist/releases/latest) tgz |
| [dsh-ops](https://github.com/thatgfsj-dsh/dsh-ops) | DSH 底层操作工具（原生文件 / PTC / bash），减少 token 消耗与任务耗时（上游 [T-Auto/dsh-ops](https://github.com/T-Auto/dsh-ops)） | JavaScript | 0.3.1（快照） | **直接用上游** npm `dsh-ops`（0.5.2） |
| [dsh-trae-api](https://github.com/thatgfsj-dsh/dsh-trae-api) | 把 Trae Work CN 额度转成本地 OpenAI / Anthropic 兼容 API（上游 [Wang-JQ77/dsh-trae-api](https://github.com/Wang-JQ77/dsh-trae-api)） | JavaScript | 1.0.2 | 上游 npm `dsh-trae-api`；Linux / macOS 支持见上游 [PR #5](https://github.com/Wang-JQ77/dsh-trae-api/pull/5) |

三个 fork 的边界：

- **dsh-ops**：上游很活跃，本组织快照停在 0.3.1（落后上游 1230 个提交，上游已到 v0.5.2），请优先使用上游仓库或 npm 包。
- **dsh-composer-assist**：上游许可是「源码可见、禁止修改」，只能原样使用，不要在本组织 fork 上改代码。
- **dsh-trae-api**：上游自 2026-08 起未再更新，Linux / macOS 支持仍挂在待合并的 PR #5 上；从 npm 装到的是 Windows 版本。

## 安装

优先用 **Release 资产** 或 **本地目录** 安装。不要把 npm 包名当作本组织的插件名。

```sh
# 1) 有 Release 资产：下载 tgz 后按 tarball 安装
#    （dsh-migrate、dsh-phone；dsh-composer-assist 用上游 Release）
dsh plugin --profile web add ./dsh-phone-0.4.1.tgz

# 2) 没有 Release 资产：clone 仓库后按本地目录安装
git clone https://github.com/thatgfsj-dsh/dsh-xiangqi.git
dsh plugin --profile web add ./dsh-xiangqi

# 3) 3 个 fork：装上游的发版产物（见上表）
dsh plugin --profile web add dsh-ops
```

> ⚠️ **npm 上的同名包不是本组织的插件。** `dsh-session-delete`、`dsh-migrate`、`dsh-xiangqi`、`dsh-phone` 这 4 个 npm 包属于他人项目；`dsh-disable-pwsh`、`dsh-emotion-analyzer`、`dsh-Compress-codex` 尚未发布到 npm。按包名安装会装到别人的插件或直接失败，请一律用上面的方式。

安装前确认插件声明的 `engines.dsh`。2026-11-10 核对：10 个插件的 `engines.dsh` / `peerDependencies` 在 DSH `0.2.2-rc.1` 下均能通过 DSH 自带的兼容检查；具体验证步骤以各仓库 README 为准。

## 仓库构成

**13 个公开仓库** = 10 个插件 + 1 个技能包（`dsh-plugin-skills`）+ 1 个组织主页（本仓库 `.github`）+ 1 个临时 CI 沙箱（`ci-sandbox`，仅用于测试工作流，不对外使用）。

- **迁移已完成**（2026-10-30 ~ 2026-11-09）：个人账号里的 DSH 插件与技能包已全部迁入本组织；旧链接可能仍能重定向，但新地址以本页为准。
- **核心技能包**：`dsh-plugin-skills` 按 DSH 版本分目录维护（0.2.1-rc.2 / rc.3 / rc.4、0.2.2-rc.1），用法见上方「核心 skills」。
- **3 个 fork**：`dsh-ops`、`dsh-trae-api`、`dsh-composer-assist` 在本组织仅作镜像 / 存档，主开发与问题跟踪见插件表里的上游链接。

## 相关

- 个人主页：[github.com/Thatgfsj](https://github.com/Thatgfsj)
- 个人网站：[thatgfsj.xyz](https://www.thatgfsj.xyz/)
- 项目索引：[thatgfsj.xyz/projects](https://www.thatgfsj.xyz/projects/)

---

<p align="center">
  <sub>组织 Profile README · 横幅是仓库内自绘 SVG，随 GitHub 主题切换明暗两版 · 插件与仓库数量核对于 2026-11-10</sub>
</p>

<p align="center"><a href="#readme-top">↑ 回到顶部</a></p>
