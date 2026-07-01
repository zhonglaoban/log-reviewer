# log-reviewer

评审并改进项目日志，让日志更适合排查问题、串联链路和做 AI 辅助分析。

## 能做什么

- 判断日志是否容易 grep、过滤和关联。
- 检查模块、线程、请求、错误路径之间能否串起完整链路。
- 推荐 `trace_id`、`event`、`key=value` 等结构化日志模式。
- 为客户端、服务端、Rust、Android、iOS 项目给出可落地的日志改进方案。

## 仓库结构

- `SKILL.md`：唯一的 skill 定义文件，同时适用于 Codex 和 Cursor Agent Skills。

## 添加到 Codex

把仓库克隆到 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/zhonglaoban/log-reviewer.git ~/.codex/skills/log-reviewer
```

之后在 Codex 中要求评审日志、优化日志格式、设计日志规范或根据日志定位问题即可触发。

## 添加到 Cursor

Cursor Agent Skills 使用 `.cursor/skills/<skill-name>/SKILL.md` 结构。把本仓库的 `SKILL.md` 复制到目标项目：

```bash
mkdir -p .cursor/skills/log-reviewer
cp path/to/log-reviewer/SKILL.md .cursor/skills/log-reviewer/SKILL.md
```

也可以在 Cursor 中从 GitHub 导入：

1. 打开 Cursor 的 **Customize**。
2. 进入 **Rules**，点击 **Add Rule**。
3. 选择 **Remote Rule (Github)**。
4. 输入 `https://github.com/zhonglaoban/log-reviewer`。

安装后，让 Cursor 评审日志或制定日志规范。

---

## English

Review and improve project logging practices for debugging, observability, and AI-assisted analysis.

## What It Does

- Reviews whether logs are easy to grep, filter, and correlate.
- Checks traceability across modules, threads, requests, and error paths.
- Recommends structured logging patterns such as `trace_id`, `event`, and `key=value`.
- Produces practical logging improvements for client, server, Rust, Android, and iOS projects.

## Repository Layout

- `SKILL.md`: the single skill definition file for both Codex and Cursor Agent Skills.

## Add to Codex

Clone this repository into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/zhonglaoban/log-reviewer.git ~/.codex/skills/log-reviewer
```

Then ask Codex to review logs, improve log formats, design logging conventions, or help debug from logs.

## Add to Cursor

Cursor Agent Skills use `.cursor/skills/<skill-name>/SKILL.md`. Copy this repository's `SKILL.md` into your target project:

```bash
mkdir -p .cursor/skills/log-reviewer
cp path/to/log-reviewer/SKILL.md .cursor/skills/log-reviewer/SKILL.md
```

You can also import it from GitHub in Cursor:

1. Open **Customize** in Cursor.
2. Go to **Rules** and choose **Add Rule**.
3. Select **Remote Rule (Github)**.
4. Enter `https://github.com/zhonglaoban/log-reviewer`.

After installation, ask Cursor to review logs or propose a logging standard.
