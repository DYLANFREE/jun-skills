# Jun Skills

我在日常研究、写作和工程协作中逐步整理的 AI 使用方法。

先从 `clearme` 开始。每次公开一个能独立使用的方法，讲清它解决什么、什么时候用，以及不能替你做什么。

## 先试 clearme

**让 AI 先说清楚：它理解你要解决的，究竟是什么。**

有时 AI 已经列出一长串方案，你却还不确定它有没有听懂。`clearme` 会让它先回到你的真实意图，用简单的话说清问题、依据和预期变化，等方向对齐后再继续。

```text
clearme。先告诉我：你理解我真正要解决的是什么，为什么这样判断，做完后应该改变什么。先别实施。
```

它不是单纯缩短回答，也不是让 AI 永远同意你。信息能自己查就先查；事实不足要说明，关键前提不成立也应指出。

### 一个例子

下面是说明用的模拟场景，不是真实评测成绩，也不是必须照抄的答案。

你说：

> 同事总是来问我要资料，我想搭个知识库。clearme，先别写方案。

期待的回应方向：

> 你想减少的是每次都由你找资料、解释背景的重复工作，让同事能自己找到可信的信息。知识库是可能的办法，但还没核实他们是找不到入口、分不清版本，还是资料本身不够用；弄清这一点，才能判断该改哪里。

你可以据此纠正它，然后再决定是否实施。不需要先听一遍数据库、接口和部署方案。

## 什么时候用

- AI 讲了很多，你仍不知道它在解决什么。
- 讨论已经陷入技术细节，需要回到目标和真正的问题。
- 开工前想确认双方理解一致，避免做完才发现方向错了。

不必给所有简单任务加一道 `clearme`。如果你只要一个明确答案、直接改稿或执行已对齐任务，就直接提出要求。

## 安装

最简单的方法，是把下面这段话发给支持 Skill 的 AI 工具：

```text
请读取并安装这个 Skill：
https://github.com/DYLANFREE/jun-skills/tree/main/skills/clearme

只安装 clearme，使用完整文件夹。若已有同名版本，先比较，保留我的自定义，不直接覆盖。完成后告诉我如何调用。
```

也可以使用 [Vercel Skills CLI](https://github.com/vercel-labs/skills)：

```sh
npx skills add DYLANFREE/jun-skills --skill clearme
```

该 CLI 当前要求 Node.js 22.20 或更高版本；默认安装到当前项目，并选择目标 Agent。需要跨项目使用时按它的提示选择作用范围，具体参数见[官方安装说明](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)。这不是运行 `clearme` 所需的依赖，只是一种安装方式。

没有 Skill 系统也可以：将 [SKILL.md](skills/clearme/SKILL.md) 全文交给 AI，明确要求按它工作。不同工具的加载方式与表现可能不同，不承诺复制过去就有完全相同的效果。

## 安装后怎么用

在支持对应调用方式的工具里：

```text
$clearme 我觉得这个方案偏了，先说清楚你对目标的理解。
```

或者直接说：

```text
用 clearme，先基于已有材料把真正的问题讲明白，暂不执行。
```

`clearme` 默认只讨论和对齐，不因调用它而修改文件、安装软件、部署或改变外部状态。它可以读取本次任务中有权访问的资料，但不能据此扩大访问或执行权限。

## 已公开的方法

| Skill | 解决什么 | 入口 |
|---|---|---|
| clearme | 让 AI 对齐真实意图，并把复杂问题讲明白 | [方法原件](skills/clearme/SKILL.md) |

机器可读目录：[skills.json](skills.json)。只收录当前仓库已经提供的完整方法，不把计划中的 Skill 列为可用。

## 使用反馈

如果效果不对，欢迎提 Issue，说明当时想解决什么、实际回答偏在哪里、希望怎样改变。提交前请去掉姓名、账号、密钥和其他不适合公开的材料。

开源不等于已证明适合所有模型和场景。请用真实任务判断它有没有帮助，不用是否复述固定措辞来验收。

## 来源与许可

方法来自 [woodfirewater / DYLANFREE](https://github.com/DYLANFREE) 的日常 AI 协作实践。本次发布保留 `clearme` 的既有方法正文，补充公开使用说明与目录。

开源组织方式参考了[花叔的 Skills 总目录](https://github.com/alchaincyf/huashu-skills)与[数字生命卡兹克的 Skills 合集](https://github.com/KKKKhazix/khazix-skills)：按用途介绍、让人和 AI 都能找到安装入口。这里没有复制他们的 Skill 实现。

[MIT License](LICENSE)。允许使用、修改和分发，包括商业使用；需保留许可证和版权声明，不附效果保证。

---

English: Practical AI collaboration skills, starting with **clearme**: align on the real problem and explain it in plain language before taking action. The instructions are primarily in Chinese.
