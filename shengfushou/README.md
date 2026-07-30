# 胜负手 / Shengfushou

> 找到决定整盘棋的那一步。
> Find the move that decides the game.

[中文](#中文) ｜ [English](#english)

---

## 中文

你有一件想做的事，但不知道该先做什么；或者已经做了很久，一直没有拿出去。这个 skill 帮你看清现在最值得花力气的地方，然后给你今天就能开始的一步。

### 它解决什么

写文章、做页面、剪视频、找工作、做产品，这些事都没有一个清楚的「做完了」。所以人容易在两头出错：方向还没定就开始调字体配色，或者第三版就够好了却还在改第八版。

难的地方在于，判断「该继续还是该停」需要一个标准，而做事的人同时也是打分的人，标准会一路移动。

这个 skill 的做法很简单：开工前把标准写在纸上，之后照着纸判断，不照着感觉判断。

### 安装

把这个链接发给 Claude Code，说你想装 shengfushou。

```
https://github.com/gumilu9/maoku-skills
```

或者手动：

```bash
git clone https://github.com/gumilu9/maoku-skills.git
cp -r maoku-skills/shengfushou ~/.claude/skills/
```

装完重开一个会话生效。

### 怎么开口

三种情况，你不用挑，用自己的话说就行。

**只有一个模糊的念头**

> 我想今年把副业做起来，方向想了好几个，一直没真的开始。

**已经有一件具体要做的事**

> 开工：做一份季度汇报，下周三要讲。

**已经做了一阵，开始反复改**

> 我在改第五版了，还是感觉差点意思。

### 它会先自己去找，才问你

问你之前，它按顺序找：你这次给的文件 → 本机的旧记录 → 联网查 → 你授权的外部数据。都拿不到才开口问你。

**联网**：涉及外部现状的判断不许凭记忆答。有哪些岗位在招、竞品怎么定价、这个职位名称是不是真的存在、平台规则有没有变，这些必须真的去搜，而且搜完要说清哪条判断被改了。联网结果可能推翻你原来的目标，这时它不替你改，只把差距摆出来。

**外部数据**：你已经在做的事，真实过程数据往往就在你的邮箱、日历、表格或平台后台里，比任何自述都可信。它会提议读一下，你不同意就继续用你说的数字，并在卡上注明这条依据来自自述。

| 你在做 | 值得读的真实数据 |
|---|---|
| 找工作 | 邮件里的回复率、面试邀约、拒信原文 |
| 做产品 | 收款记录、注册与留存、退款理由 |
| 做内容 | 后台完读率、流量来源、历史同类表现 |
| 对外沟通 | 谁回了、谁没回、哪些跟进漏掉了 |

拿到真实数据后它会拆开合并数字。「注册到付费 5.8%」这种总转化率会把病灶抹平，要逐环看才知道卡在哪。

**要问你的时候**：用可点选的框，选项由它现场根据你的场景推出来，一次最多两问。点选比打字快，所以带选项的提问比开放式提问更省你的时间。

### 你会拿到什么

第一次回复一定有两样东西：一句暂时说得通的目标，和一个今天就能开始的动作。

信息够的时候它直接说「这件事现在最关键的是 X」。信息不够的时候它说「最像的关键点是 X，但还缺 Y，先做 Z，做完就看得准了」，不会含糊过去，也不会硬下结论。

每次回复的最后一行都是「下一步：一个动作」。只给一个，其余的它自己排序，先放进「这次先不管」。

#### 开工小卡

聊到方向清楚了，它会写一张卡，六格：

- 你真正想要的变化
- 这次先做出来
- 现在最值得花力气
- 做到这里就先拿出去试
- 这次先不管
- 今天先做

### 干活过程中

| 你说 | 它做 |
|---|---|
| 过线吗 | 逐条报「做到这里就拿出去试」的状态，不加意见 |
| 我在改第 N 版了 | 版本数是事实，比任何自我描述可信 |
| 情况变了：XX | 重新定。但只认三种：看谁的反应变了、想要的东西变了、时间或钱变了 |

「我觉得还能更好」不算情况变了。

### 结果出来以后

```
对账：[实际结果]。对方原话是 [X]。
```

小卡是单次的，对账记录会累积。攒到一定数量后，系统可以对照历次记录，指出重复出现的模式，比如同一类维度被反复修改而外部反馈始终没有变化。这类判断只能来自对账记录，聊天上下文里没有。

### 给它事实，别给判断

| 事实 | 判断 |
|---|---|
| 客户说太素 | 客户品味不行 |
| 上一篇完读率 28% | 上一篇写得不够好 |
| 我改到第四版了 | 我总觉得差点意思 |

左边这些，后来发生的事可以检验；右边这些，只是你此刻的感觉。它会请你把右边换成左边。

### 你的东西存在哪

小卡和记录存在 `~/.shengfushou/`，本地 Markdown 文件，不联网不上传。想换地方，改 `SKILL.md` 里的路径。

### 说明

还在迭代中，以它实际帮到你的效果为准，不以这一页的说法为准。

### 许可

MIT，见仓库根目录 [LICENSE](../LICENSE)。

---

## English

You have something you want to get done but don't know where to start. Or you've been working on it for weeks and it still hasn't gone out. This skill tells you where your effort actually matters right now, and hands you one thing you can start today.

### What it's for

Writing an article, building a page, editing a video, job hunting, shipping a product: none of these come with a clear "done". So people fail in two directions. They tune fonts and colors before the direction is settled, or they keep making version eight of something that was already fine at version three.

The hard part is that deciding "keep going or stop" requires a standard, and when the maker is also the scorer, the standard keeps moving.

So this skill writes the standard down before you begin, then judges against the paper instead of the feeling.

### Install

Send this link to Claude Code and say you want to install shengfushou.

```
https://github.com/gumilu9/maoku-skills
```

Or by hand:

```bash
git clone https://github.com/gumilu9/maoku-skills.git
cp -r maoku-skills/shengfushou ~/.claude/skills/
```

Restart your session afterwards.

### How to start

Three situations. You don't need to pick one, just say it however you'd say it.

**Just a vague idea**

> I want to get a side project going this year. I've had a few directions in mind and never actually started.

**A concrete thing to make**

> Starting: a quarterly review deck, presenting next Wednesday.

**Already deep in, stuck revising**

> I'm on version five and it still feels off.

### It looks things up before it asks you

Before asking, it works through a fixed order: the files you just gave it, then local records from past runs, then the web, then any external data you authorize. Only when none of that works does it ask you.

**Web search**: claims about the outside world are not answered from memory. Which roles are actually open, how competitors price, whether a job title even exists, whether a platform rule changed: these get searched for real, and afterwards it has to state which of its judgments the search changed. Search results may contradict the goal you started with. It won't rewrite your goal for you; it lays the gap out instead.

**External data**: for work already in motion, the real process data usually sits in your inbox, calendar, spreadsheets, or a platform dashboard, and it beats any self-report. It will offer to read that. Decline and it proceeds with your stated numbers, noting on the card that the basis is self-reported.

| What you're doing | Real data worth reading |
|---|---|
| Job hunting | Reply rates, interview invites, the exact wording of rejections |
| Shipping a product | Payments, signups and retention, refund reasons |
| Making content | Read-through rates, traffic sources, past comparables |
| Outreach | Who replied, who didn't, which follow-ups got dropped |

Once it has real numbers, it breaks aggregates apart. A blended figure like "5.8% signup to paid" hides the actual failure point; only the step-by-step view shows where things stall.

**When it does ask**: it uses a clickable prompt with options written on the spot from your situation, two questions at most. Clicking is faster than typing, so options cost you less time than an open question.

### What comes back

Every first reply contains two things: a working version of your goal, and one action you can start today.

When there's enough information it says plainly, "the thing that matters most here is X". When there isn't, it says "X looks closest, but Y is missing, so do Z first" instead of hedging or forcing a conclusion.

Every reply ends with one line: "Next: one action." One, never a menu. The rest gets sorted and parked under "not this time".

#### The one-page card

Once the direction is clear it writes a card. Six fields:

- what you actually want to change
- what you're making this round
- where your effort matters most
- ship it once it reaches this
- not this time
- today

### While you work

| You say | What it does |
|---|---|
| am I there yet | Reports each ship condition one by one, no opinions attached |
| I'm on version N | Version count is a fact, and it outweighs any self-description |
| things changed: X | Reopens the card, but only for three reasons: whose reaction matters changed, the goal changed, the time or money changed |

"I think it could be better" does not count as things changing.

### After you get a result

```
Reconcile: [what actually happened]. Their exact words were [X].
```

The card is per-task; reconciliation records accumulate. Once enough of them exist, the system can compare across them and point out repeating patterns, such as the same dimension being revised over and over while external feedback stays unchanged. Judgments like that can only come from the records, not from chat context.

### Give it facts, not verdicts

| Fact | Verdict |
|---|---|
| The client said it looks plain | The client has no taste |
| Last post read through at 28% | Last post wasn't good enough |
| I'm on version four | Something still feels off |

The left column can be checked against what happens next. The right column is just how you feel right now. It will ask you to convert.

### Where your data lives

Cards and records live in `~/.shengfushou/` as plain local Markdown. Nothing leaves your machine. Change the path in `SKILL.md` to move them.

### Note

Still iterating. Trust what it actually does for you over what this page claims.

### License

MIT. See [LICENSE](../LICENSE) in the repo root.
