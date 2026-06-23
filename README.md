# FDE Copilot

An AI copilot that walks you through every stage of an FDE (Forward Deployed Engineer) project — from kickoff and customer discovery, through requirements alignment and vibe coding, to production deployment and handoff. Full SOP + ready-to-use Skill files.

---

## What is this?

If you're doing FDE delivery (deploying solutions at customer sites, moving from prototype to production), this tool helps you:

- **Structure customer discovery** and align on requirements with the client
- **Generate key documents**: MVD scope confirmation, daily progress updates, tech debt logs
- **Get FDE-perspective advice** on trade-offs and engineering decisions during vibe coding
- **Advance through phases** systematically, avoiding common pitfalls

## Two Versions

### 🏠 WorkBuddy Edition (`fde-copilot-skill-workbuddy.md`)

Built for [WorkBuddy](https://www.codebuddy.cn):
- Project state persistence (`.fde/` directory + JSON + Markdown files)
- Cross-session continuity (auto-reads last state on new conversation)
- Auto-generates documents and writes to local filesystem
- Trigger: say `/fde` or "开始FDE项目"

**How to use**: Place the file in your WorkBuddy skill directory:
```
~/.workbuddy/skills/fde-copilot/SKILL.md
```

### 🌍 Universal Edition (`fde-copilot-universal.md`)

Works with any AI tool (ChatGPT, Claude, Cursor, Copilot, etc.):
- Pure Markdown, zero platform dependencies
- No filesystem operations required
- Two state management modes: self-managed files / in-conversation snapshots
- Paste into conversation start, or use as Custom Instruction / System Prompt

**How to connect per platform**:

| Platform | Method |
|----------|--------|
| ChatGPT | Settings → Custom Instructions → paste full text |
| Claude | New chat → paste at the beginning |
| Cursor | Settings → Rules → For All Files → paste |
| Copilot | `.github/copilot-instructions.md` → paste |
| Others | Send as the first message in conversation |

## SOP Documents

| Document | Description |
|----------|-------------|
| `FDE_SOP.md` | Complete FDE operations manual (synthesized from Palantir founding engineer interviews, GeeksForGeeks, FDE Academy, and more). Action-oriented, not theoretical. |
| `FDE_Copilot_User_Guide.md` | Skill user guide: feature list, phase flowchart, version comparison |

## Core FDE Principles

1. **Write code on Day 1** — ugly is fine, not moving is not
2. **Fast on core path, slow on trust points** — never compromise on security, accuracy, or stability
3. **If an operation happens <10 times, do it manually** — automate only what happens daily
4. **Cover 80% of mainstream scenarios first** — handle edge cases through feedback
5. **Send the client one progress update every day** — even if it's just one sentence
6. **Feed product teams generalized patterns**, not specific feature requests
7. **Only talking to the tech lead = guaranteed pitfall** — maintain both business and tech communication lines
8. **Three deployment rules**: validate environment on Day 1, always have an offline deploy package, ingest dirty data first then clean

## License

MIT — use, modify, and share freely.

---

---

# FDE Copilot

FDE（Forward Deployed Engineer）全程陪跑 AI 助手——从项目启动、客户调研、需求对齐、vibe coding 到上线收尾的全流程 SOP + Skill。

## 这是什么

如果你在做 FDE 项目交付（驻场工程师，把方案从原型推进到生产），这个工具能帮你：
- 结构化地做客户调研和需求对齐
- 生成 MVD 确认单、每日进展消息、技术债记录等文档
- 在 vibe coding 时给你 FDE 视角的建议和取舍判断
- 按阶段推进，确保不踩坑

## 两个版本

### 🏠 WorkBuddy 版（`fde-copilot-skill-workbuddy.md`）

专为 [WorkBuddy](https://www.codebuddy.cn) 设计的 Skill 版本：
- 支持项目状态持久化（`.fde/` 目录 + JSON + Markdown 文件）
- 跨对话连续工作（下次对话自动读取上次状态）
- 自动生成文档文件并写入本地
- 触发方式：说 `/fde` 或 "开始FDE项目"

**使用方式**：把文件内容放到 WorkBuddy 的 skill 目录：
```
~/.workbuddy/skills/fde-copilot/SKILL.md
```

### 🌍 通用版（`fde-copilot-universal.md`）

适用于任何 AI 工具的版本（ChatGPT、Claude、Cursor、Copilot 等）：
- 纯 Markdown，零平台依赖
- 不依赖文件系统操作
- 两种状态管理方式：用户自管理文件夹 / 对话内快照
- 直接粘贴到对话开头，或作为 Custom Instruction / System Prompt 使用

**各平台接入方式**：

| 平台 | 接入方式 |
|------|---------|
| ChatGPT | 设置 → Custom Instructions → 粘贴全文 |
| Claude | 开新对话 → 直接粘贴在开头 |
| Cursor | Settings → Rules → For All Files → 粘贴 |
| Copilot | .github/copilot-instructions.md → 粘贴 |
| 其他 | 作为对话首条消息发送 |

## SOP 文档

| 文档 | 说明 |
|------|------|
| `FDE_SOP.md` | FDE 完整操作手册（多方资料综合版：Palantir 创始工程师访谈 + GeeksForGeeks + FDE Academy 等），以操作步骤为主 |
| `FDE_Copilot_User_Guide.md` | Skill 使用说明书，包括功能清单、阶段流程图、版本对比 |

## FDE 核心原则

1. **第一天就写代码**，允许丑，不允许不动
2. **核心路径快，信任点慢**：安全/准确性/稳定性不妥协
3. **操作 <10 次手动做**，每天都有才自动化
4. **覆盖 80% 主流场景**先上线，剩余靠反馈
5. **每天给客户发一条进展**，哪怕一句话
6. **反馈产品团队的是通用场景**，不是客户的具体功能请求
7. **只和技术负责人沟通 = 踩坑**：务必同步维护业务侧和技术侧两条线
8. **部署三铁律**：第一天验环境、永远备离线包、脏数据先入仓再清洗

## License

MIT — 随意使用、修改、分享。
