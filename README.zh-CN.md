[English](README.md) · **简体中文**

# Awesome Music Prompts

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Prompts](https://img.shields.io/badge/prompts-96-blue.svg)](prompts/)
[![Tool neutral](https://img.shields.io/badge/tool-neutral-lightgrey.svg)](#兼容性)

一份可直接复制使用的 AI 音乐生成提示词库，按流派、情绪、人声、速度和使用场景整理。

库中每一条提示词都遵循统一的五槽位结构，长度控制在主流工具的字数上限之内，并附一句说明讲清楚它*为什么*这样写。目标不是让你无脑复制，而是让你看懂这套写法的语法，之后能自己改。

---

## 为什么做这个

搜索 AI 音乐提示词，你能找到的基本是两类东西：没有任何解释的提示词截图，以及一堆模型基本不理会的形容词（`史诗`、`感人`、`优美`）。

问题在于，含糊的提示词不会**明显地**失败——它产出的是"能听但很平庸"的东西。你得到一首中规中矩的中速歌曲，听起来和其他所有 AI 生成的歌没什么区别，而且完全看不出是哪个词导致的。

这个库的做法正好相反：

- **每条提示词都具体到可复现。** 点名乐器、给出真实 BPM、写明制作质感。
- **每条提示词都有注解。** 一句 *why it works*，让你能改写而不只是照抄。
- **每条提示词都符合真实限制。** 大多数工具的风格字段有字数上限，这里的每一条都在限制之内。

---

## 快速上手

先读 [**Prompt Anatomy（提示词结构）**](docs/prompt-anatomy.md)，五分钟读完，之后整个库都会变得好理解。

简版结论：一条可靠的风格提示词要填满五个槽位。

| 槽位 | 回答什么 | 示例 |
|------|---------|------|
| **流派 Genre** | 这是什么类型的音乐？ | `Lo-fi` |
| **情绪 Mood** | 听感应该是什么样？ | `Nostalgic` |
| **人声 Vocal** | 谁在唱，还是没人唱？ | `No vocals` |
| **速度 Tempo** | 多快？ | `78 BPM` |
| **制作 Production** | 这段录音听起来是什么质感？ | `Dusty piano loop, vinyl crackle` |

拼起来：

```
Lo-fi, nostalgic, no vocals, 78 BPM, dusty piano loop, vinyl crackle, soft tape saturation
```

把**主题内容**（这首歌讲什么）放进描述 / 歌词字段，不要塞进风格字段。这是两个不同的输入，模型处理它们的路径也不同。

> **关于语言**：库中的风格标签一律保留英文。目前主流音乐生成模型的训练语料以英文音乐描述为主，**英文标签的出结果稳定性明显更高**，无论你想生成哪种语言的歌。歌词和主题描述则用什么语言写都可以。

---

## 目录

| 分类 | 内容 |
|------|------|
| [**Genres 流派**](prompts/genres.md) | 12 个流派 × 3 种变体 —— Pop、Rock、Hip-Hop、R&B、EDM、Folk、Jazz、Lo-fi、国风、Metal、Classical、Country |
| [**Moods 情绪**](prompts/moods.md) | 12 种情绪基调，从欢快到激烈，每种给两套不同编配 |
| [**Vocals 人声**](prompts/vocals.md) | 女声、男声、合唱、童声、气声、和声、纯音乐，另附混音定位与演唱方式速查 |
| [**Tempo & structure 速度与结构**](prompts/tempo-and-structure.md) | 各流派 BPM 对照表，以及如何控制歌曲结构 |
| [**Use cases 使用场景**](prompts/use-cases.md) | 播客片头、游戏循环、广告、婚礼、学习背景音、预告片、短视频 |
| [**Negative prompts 负面提示词**](prompts/negative-prompts.md) | 该排除什么，以及哪些排除真的有效 |
| [**Prompt anatomy 提示词结构**](docs/prompt-anatomy.md) | 五槽位框架与七条实践经验 |

> 目前内容文件均为英文。欢迎提交中文翻译，见[贡献指南](CONTRIBUTING.md#translations)。

---

## 条目格式

每条提示词都是同一个形状：

````markdown
### Genre — Variant name

**Style tags**

```
逗号分隔的风格片段，直接粘贴进风格字段
```

**Description**
> 这首歌讲什么 —— 填进描述或歌词字段。

**Why it works** —— 这条提示词做对了什么，是含糊版本做不到的。

`87 chars`
````

末尾的字符数是为了让你在动手改之前，先看清楚还剩多少余量。

---

## 兼容性

这些提示词**不绑定任何特定工具**。五槽位结构反映的是文本条件音乐模型解析输入的方式，不是某个产品的特性，所以这里的条目稍作调整就能在各家工具间迁移。

它们是对照 [MuseGen](https://www.musegen.ai/) 编写和检查的——其风格字段上限为 180 字符，接受逗号分隔的标签，并提供独立的负面标签输入。库中每条提示词都在这个上限之内，而 180 是常见限制里最紧的一档，因此迁移到别处不会被截断。

以下是迁移到其他工具的**参考建议，不是实测结论**——真正跑过这些工具的人来提交修正，正是这个库需要的：

| 工具 | 建议调整 |
|------|---------|
| Suno | 风格字段更短，优先删掉制作类标签，保留流派 + 情绪 + 人声 |
| Udio | 对年代和风格指涉类表述反应较好，可以试着加一个年代标签 |
| Stable Audio | 以纯音乐为主，人声槽位通常无效，把这部分字数用在制作描述上 |
| Riffusion | 偏好更少、更宽泛的标签，可以试着把槽位 4 和 5 合并 |

无论列表里有没有你用的工具，只要你实测过，[提一个 PR 说明结果](CONTRIBUTING.md)都很有价值。

---

## 在 Claude 里直接用

同一套内容也打包成了 Claude Skill：[**music-prompt-skill**](https://github.com/musegen/music-prompt-skill)。clone 进 skills 目录，Claude 就会替你写这些提示词，不用来回复制粘贴，而且会自动按你的使用场景选对约束。

```bash
git clone https://github.com/musegen/music-prompt-skill ~/.claude/skills/music-prompt
```

同一套手艺，两种读者：这个仓库是写给人看、供人学的；skill 里的 references 则是为模型快速查阅而压缩过的。

---

## 参与贡献

新提示词、纠错、各工具的实测发现、翻译，都欢迎——详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

新增提示词的门槛很简单：**具体**（读的人能预判会出来什么）、**有注解**（一句话讲清楚它为什么有效）、**符合限制**（能放进 180 字符的风格字段）。

---

## 许可

[MIT](LICENSE) —— 随意使用，商用亦可，无需署名。

注意该许可覆盖的是**这份合集本身**。你用它生成的音乐是否可商用，取决于你所使用的生成工具的条款，需要另行确认。

---

<sub>由 <a href="https://www.musegen.ai/">MuseGen</a> 团队维护。如果它帮你省下了一些试错，点个 ⭐ 能让更多人找到它。</sub>
