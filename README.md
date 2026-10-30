# Jun Skills

**把与 AI 一起工作的经验，变成可以复用的方法。**

从理解问题开始，逐步公开研究、写作和工程协作中积累的方法。现在先交付一个：**clearme**。

[选一个 Skill](#skills) · [看使用示例](#example) · [开始使用](#start) · [反馈](https://github.com/DYLANFREE/jun-skills/issues)

## 为什么做这些 Skill

和 AI 一起做事，常会遇到这样的时刻：它已经列出很多方案，你还不确定它有没有听懂；工作推进了一段，才发现最初的问题没有对齐。

我把这些协作中反复用到的方法整理下来。希望换一个任务、换一个 AI 时，不必重新解释一遍怎样一起工作。

每次只公开已经整理完整的一项，讲清用途、用法和边界。没提供的方法不先挂名，没验证的效果不当成果。

<a id="skills"></a>

## 已公开的方法

| 你正在遇到什么 | 用哪个 | 会得到什么 |
|---|---|---|
| AI 说了很多，你仍不确定它理解的问题对不对 | [clearme](skills/clearme/SKILL.md) | 先对齐真实意图，用一两段人话说明核心问题和预期变化，暂不实施 |

给 AI 查找的目录：[skills.json](skills.json)。

### clearme：先把真正的问题讲明白

适合开工前确认理解，也适合讨论已经偏题、陷入技术细节的时候。

它会回到你想改变的现实，依据已有材料说明判断。能自己查的先查；缺少关键事实就指出，不把猜测包装成理解，也不为了对齐而无条件赞同你。

`clearme` 默认只讨论，不修改文件或改变外部状态。方向确认后，再由你提出下一步任务。

一个简单问题可以直接问，已经明确的任务可以直接做；不必每次都加一道对齐流程。

<a id="example"></a>

## 看一个使用示例

**以下是模拟示例，不是真实实战记录或评测成绩。**

```text
同事总是来问我要资料，我想搭个知识库。
clearme，先别写方案，告诉我你理解我真正想解决的是什么。
```

回应可以是：

> 你想减少的是每次都由你找资料、解释背景的重复工作，让同事能自己找到可信的信息。知识库是可能的办法，但还没核实他们是找不到入口、分不清版本，还是资料本身不够用；弄清这一点，才能判断该改哪里。

这样你能先判断它理解得对不对，再决定是否建设知识库。实际回答应该随材料变化，不必复述这段话。

当前尚未收录经过公开确认的真实任务案例。后续案例会分别标明输入、实际产物、人类反馈和未验证部分。

<a id="start"></a>

## 开始使用

**1．把这段话发给支持 Skill 的 AI 工具。**

```text
帮我安装 clearme：
https://github.com/DYLANFREE/jun-skills/tree/main/skills/clearme

只安装这一个完整文件夹。已有同名版本时先比较，保留我的自定义，不直接覆盖。
```

**2．需要对齐时，直接说。**

```text
用 clearme。先说清楚你理解的目标、真正的问题和预期变化，暂不执行。
```

支持 `$clearme` 调用方式的工具也可以直接用这个名字。安装和加载方式以目标工具为准。

<details>
<summary>命令行安装，或在没有 Skill 系统的 AI 中使用</summary>

使用 [Vercel Skills CLI](https://github.com/vercel-labs/skills)：

```sh
npx skills add DYLANFREE/jun-skills --skill clearme
```

该安装器当前要求 Node.js 22.20 或更高版本，默认安装到当前项目。目标 Agent、作用范围及其他参数见[官方说明](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)。clearme 本身没有额外运行依赖。

没有 Skill 系统时，可以把 [SKILL.md](skills/clearme/SKILL.md) 全文交给 AI，明确要求按它工作。不同工具的上下文和权限机制不同，不承诺完全相同的效果。

</details>

## 后续怎样更新

- 逐项增加能独立使用的方法，不一次打包全部私人工作资料。
- 优先展示可公开的真实案例；模拟示例、受控演练和真实效果分别标明。
- 有复杂架构的方法，用 Archify 展示角色、流向和边界，附静态预览与可下载的交互图；不为轻量方法硬造架构。
- 方法正文、必要资源、版本与[更新记录](CHANGELOG.md)一起维护。

## 使用反馈

用起来不对，欢迎[提 Issue](https://github.com/DYLANFREE/jun-skills/issues)：当时想解决什么、AI 回答偏在哪里、你希望怎样改变。请先去掉姓名、账号、密钥和其他私人内容。

以实际任务是否得到帮助来判断效果。安装成功、示例好看，都不等于已证明适合所有模型和场景。

## 关于与许可

由 [woodfirewater / DYLANFREE](https://github.com/DYLANFREE) 从日常 AI 协作实践中整理。当前公开的 clearme 保留既有方法正文，首页只帮助理解和使用，不替代原件。

开源组织方式参考[花叔](https://github.com/alchaincyf/huashu-skills)与[数字生命卡兹克](https://github.com/KKKKhazix/khazix-skills)：按用途介绍，让人和 AI 都能找到入口。未复制他们的 Skill 实现。

[MIT License](LICENSE)。允许使用、修改和分发，包括商业使用；保留许可证与版权声明，不附效果保证。

---

English: Practical AI collaboration skills, starting with **clearme**: align on the real problem and explain it in plain language before taking action. The instructions are primarily in Chinese.
