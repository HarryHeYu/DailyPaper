> From: https://chatgpt.com/c/6a7b3369-1274-83ea-bee2-1593f68cf73d

# you asked

message time: 2026-08-11 22:36:24

每天上午 8:00 执行以下 Daily AI Research Radar 任务。

所有最终内容使用中文。论文标题、作者、模型、数据集、方法、metric、公式名称可保留英文；论文解释、摘要、实验分析、Research Idea 必须中文。

你的目标不是罗列论文，而是每天搜索、筛选并深入解释真正值得我关注的最新 AI 论文，同时发现可迁移方法、research gap、baseline、attack、benchmark、metric 和潜在撞题。

【1. 搜索要求】

主动搜索最近 24–72 小时新发布或重要更新的论文，不得仅依赖已有知识。

如果近期高价值论文不足，可以补充最近 1–3 个月此前遗漏的重要论文，并明确标记 BACKFILL。

优先使用一手来源：
arXiv、OpenReview、ACL Anthology、论文 PDF/HTML、会议官网、作者项目页、官方 GitHub。

日期、模型、数据集、实验结果、代码状态不得猜测。

重要论文应尽可能打开正文阅读，而不是只看搜索结果或 Abstract。

如果只能访问 Abstract，必须明确写：
“仅根据 Abstract / 可获取信息总结”。

【2. 研究方向】

最高优先级：

Machine Unlearning；
LLM / MLLM / VLM Unlearning；
Agent / Multi-Agent Unlearning；
Continual / Sequential / Online Unlearning；
Token / Representation / Parameter-level Unlearning；
Inference-time / Training-free Unlearning；
Memory / Behavioral / Knowledge Unlearning；
Unlearning Benchmark / Evaluation / Verification / Attack。

重点问题：

forget-retain trade-off；
utility preservation；
knowledge localization；
token importance；
cross-modal leakage；
reasoning leakage；
relearning / recovery；
membership inference；
black-box attack；
robustness；
repeated deletion；
deletion closure。

同时重点搜索能够迁移到 Unlearning 的邻域工作：

Agent / Multi-Agent；
Agent Memory / Trajectory / Skill Library；
Inference-time / Test-time Adaptation；
Activation / Representation / Logit Steering；
RLHF / DPO / NPO / PPO / GRPO；
Reward Modeling / Credit Assignment；
Continual / Lifelong Learning；
Adversarial Robustness；
Prompt Injection / Jailbreak；
Membership Inference / Extraction；
LLM / Multimodal Reasoning；
Long CoT / Test-time Compute；
Mechanistic Interpretability；
Causal Tracing；
Knowledge Neurons / SAE；
Token / Feature Attribution；
Influence Functions；
Knowledge Editing；
Diffusion Concept Erasure；
Provenance / Lineage / Information Flow。

即使论文没有明确研究 Unlearning，只要核心机制有较强迁移潜力，也可以推荐。

【3. 推荐数量】

不要固定死数量。

最低要求：

Tier S：至少 2 篇；
Tier A：至少 3 篇；
Tier B：至少 3 篇。

高质量论文较多时可以继续增加，例如 S 2–5 篇、A 3–8 篇、B 3–10 篇。

宁缺毋滥，但不能因为“名额够了”就遗漏真正重要论文。

如果当天没有足够新的 Tier S，可以从最近 1–3 个月的重要论文中选择此前遗漏的工作进行 BACKFILL 深度精读。

【4. 所有论文的共同要求】

无论 Tier S/A/B，都不能只给“标题 + 几句话”。

每篇都必须让我理解：

1. 为什么研究这个问题；
2. 以前的方法怎么做；
3. 旧方法哪里不足；
4. 作者真正的核心 insight；
5. 方法从输入到输出怎么运行；
6. 实验如何设计；
7. 最重要结果真正说明什么；
8. 有什么 limitation；
9. 和我的研究有什么关系；
10. 有什么可以迁移的 mechanism。

遇到新的 metric、loss、reward、subspace、representation、memory mechanism 等概念时，用通俗语言解释。

方法尽量写成：

Input → Step 1 → Step 2 → ... → Output

实验结果不要只说“优于 baseline”，应说明：

具体数字或现象 → 对比对象 → 差异 → 说明什么。

区分：

作者 claim；
实验真正支持的结论；
可以进一步推断的研究价值。

【5. Tier S：深度精读】

Tier S 是当天最重要的论文。

每篇进行导师式深度讲解，尽可能阅读 Abstract、Introduction、Method、Experiments、Ablation/Analysis、Conclusion。

每篇至少覆盖：

① 背景与问题
从零解释现实背景、旧方法、失败原因和 research gap，并给简单例子。

② 核心 Insight
解释作者真正观察到了什么、为什么重要、为什么过去方法没有解决。

③ Method Deep Dive
详细解释 Input → Steps → Output。
每个关键模块说明做什么、为什么、解决什么 failure mode。
如果有重要公式/loss/SVD/QR/Gram/KL/reward 等，解释变量、优化方向和直觉。

④ Toy Example
用知识删除、image-question-answer、Agent memory 或 sequential deletion 等简单案例完整走一遍方法。

⑤ Baseline Difference
选 2–4 个最相关 baseline，解释旧方法怎么做、哪里不够、本文改了什么以及优势来自哪里。

⑥ Experiments
解释 Model、Dataset、Forget/Retain Set、Baseline、Metric、Evaluation Setting。
不常见 metric 解释测什么以及高低哪个好。

⑦ Results
挑 3–5 个关键结果：
数字/现象 → 对比 → 意义 → 是否支持 claim。
同时指出 forget / retain / utility / robustness trade-off。

⑧ Ablation / Analysis
解释关键模块去掉后的变化及其实际作用。

⑨ Contribution & Limitation
区分真正创新与已有组件组合，并分析 utility、recovery、scalability、泛化、attack robustness 等问题。

⑩ Research Value
详细判断：
Baseline Potential；
Migration Potential；
Attack Potential；
Evaluation Potential；
New Paper Potential。

⑪ Migration Analysis
Original Problem
→ Transferable Mechanism
→ New Research Question
→ Method Modification
→ Minimum Experiment
→ Model/Dataset/Baseline/Metric
→ Potential Contribution
→ Collision Risk。

最后用“如果只让我记住 5 句话”总结。

【6. Tier A：重要论文】

Tier A 也必须完整解析，不允许变成论文卡片。

每篇至少解释：

背景与 gap；
核心 insight；
Method Pipeline；
Model / Dataset / Baseline / Metric；
至少 2–3 个主要实验结果及含义；
Contribution；
Limitation；
与我的研究关系；
Baseline / Migration / Attack / Evaluation Potential；
至少一个具体可执行的迁移实验。

最后判断：
Worth Deep Reading = YES / MAYBE / NO，并说明原因。

【7. Tier B：值得保存】

Tier B 也要有完整、可理解的研究摘要。

至少说明：

研究问题；
核心方法；
实验或主要结论；
最值得保存的 contribution/resource；
和我的研究哪个方向相关；
未来最可能用作：
Related Work / Baseline / Benchmark / Evaluation / Attack / Future Idea。

不要只写一句话。

【8. 二次筛选】

完成全部 Tier 后，从所有推荐论文中重新进行一次排序，而不是直接按照 Tier 排名。

给出：

Today's Most Important Paper：
只能选 1 篇，并详细说明为什么它今天最值得投入时间。

Top 3 必读：
选 3 篇，并分别说明为什么优先、最值得关注哪个方法或实验、和我的研究有什么直接关系。

Top 5 最重要论文：
给出 1–5 总排名。

Tier A 如果对我的研究特别关键，可以排在某些 Tier S 前面。

【9. Idea Mining】

基于当天所有论文提出最多 3–5 个真正有研究价值的 Idea。

重点寻找：

Token Attribution × Unlearning；
Inference-time × Unlearning；
RL Credit Assignment × Forgetting；
Continual Learning × Continual Unlearning；
Robustness × Unlearning；
Agent Provenance × Multi-Agent Unlearning；
Reasoning Trace × Leakage；
Membership Inference × Verification；
Multimodal Localization × Unlearning。

每个 Idea 给：

Inspiration；
Research Gap；
Hypothesis；
Proposed Method；
Minimum Viable Experiment；
Model / Dataset / Baseline / Metric；
Expected Contribution；
Novelty ★★★★★；
Feasibility ★★★★★；
Compute Cost ★★★★★；
Risk；
Collision Risk；
Best Venue。

禁止简单关键词拼接。

没有足够好的 Idea 时明确写：
NO STRONG IDEA TODAY。

【10. Collision Detection】

重点检查是否已经出现非常接近：

Multimodal Unlearning；
Agent Unlearning；
Multi-Agent Unlearning；
Token-level Unlearning；
Continual Unlearning；
Inference-time Unlearning；
Robust Unlearning；
Black-box Unlearning Attack

的新论文。

发现撞题时给出：

⚠️ Collision Warning

并说明：
具体论文；
重合程度；
对方已经解决什么；
仍有什么 gap；
这个方向是否还值得继续。

【11. 最终简报】

最后给出：

🥇 Today's Most Important Paper

🔥 Top 3 必读

🥈 Top 5 最重要论文

💡 Best Research Idea

⚠️ Collision Alert

📚 Reading Priority：
READ NOW / THIS WEEK / SAVE / SKIP

最终目标不是统计每天出了多少论文，而是帮助我真正理解重要论文、发现可迁移机制、寻找 research gap、找到 baseline/attack/benchmark/metric、尽早发现撞题，并从相邻领域产生值得实验的新研究方向。

---

# chatgpt response

已经设置好了：**每天上午 8:00（北京时间 / Asia/Shanghai）** 自动执行这套 **Daily AI Research Radar**。

第一次执行时间是 **2026 年 8 月 12 日上午 8:00**。我把你刚才这整套筛选、Tier S/A/B 深度要求、Idea Mining、Collision Detection、Top 3 / Top 5 和最终简报规则都放进任务里了，不是简化版。

---

# chatgpt response

# Daily AI Research Radar｜2026-08-12

今天的结论先放在最前面：**最值得关注的不是又出现了一个新的 GA/NPO 变体，而是 Agent Unlearning 的问题定义正在迅速向“删除闭包 / 残留载体 / 能力重建 / workflow-level forgetting”推进。**

我重点检查了最近几天 arXiv 的新论文，并向近 1–3 个月回溯补充。严格按 24–72 小时窗口，今天直接命中 Unlearning 的高质量论文并不算多，因此部分工作标为 **BACKFILL**。其中最重要的新信号是 **OBLIVION**：它几乎直接把你一直在考虑的 `deletion closure + residual carrier + reacquisition + Agent Unlearning` 做成了 benchmark + defense。([arXiv](https://arxiv.org/html/2608.08264))

---

# Tier S

## S1. OBLIVION: Workflow-Level Operational Skill Unlearning for Deployed Agents

**Zhengyang Shan, Xu Qian, Jiayun Xin, Kun Li, Yue Zhang, Minghui Xu**  
arXiv:2608.08264，v1：2026-08-08。虽然略超 72 小时，我把它列为今天最高优先级，因为撞题价值远高于日期上的几小时差异。([arXiv](https://arxiv.org/html/2608.08264))

### ① 它到底在研究什么？

传统 Machine Unlearning 往往问：

> 模型参数里还记不记得某个知识？

OBLIVION 问的是完全不同但对 Agent 极其重要的问题：

> **我把 Agent 的一个 skill 删掉以后，它还能不能利用环境里残留的东西，把这个 skill 重新构造出来？**

例如删除：

`send_sensitive_report skill`

但系统中仍然存在：

- 旧 transcript；
- vector memory；
- archive；
- MCP schema；
- helper code；
- registry draft；
- 历史 intermediate artifact。

那么 Agent 可能：

`旧 transcript → 总结操作步骤 → 重建 helper → 写入 registry → 再调用`

表面：

> skill 已删除。

实际上：

> capability 被复活。

论文把这种现象称为 **revoked-skill resurrection**。([arXiv](https://arxiv.org/html/2608.08264))

这与参数级 unlearning 根本不同：作者明确说，他们研究的不是 weight 是否忘掉 concept，而是 **deployed operational state 能否重建已撤销 capability**。([arXiv](https://arxiv.org/html/2608.08264))

---

## ② 真正的核心 Insight

作者用了一个很重要的类比：

> 删除 Agent skill 更像“卸载软件”，而不是删除一行数据库记录。

卸载软件不能只检查：

`app.exe 不存在了`

还要检查：

`dependencies / cache / files / registry / references / reachable state`

有没有留下。

因此他们提出：

> **Skill deletion 是 reachability / closure 问题。**

也就是：

```text
Delete(skill)
≠
skill registry entry disappears
```

真正应该要求：

```text
所有能够重新导出 skill 的 reachable path
都被切断
```

这基本就是你之前一直关注的 **Deletion Closure** 的一个非常具体实例。作者甚至明确借用了 software de-installation 中的 closure 思路。([arXiv](https://arxiv.org/html/2608.08264))

---

# ③ Method Deep Dive

OBLIVION 的完整流程可以压缩成：

```text
Revoked Skill
        ↓
发现 residual carriers
        ↓
Cross-Surface Coherent Erasure
        ↓
Agent 继续正常运行
        ↓
追踪 carrier-derived information
        ↓
source → transforms → dangerous sink
        ↓
Anti-ReDerivation Guard
        ↓
允许 / audit / block
```

它包含两个核心模块。

### A. Cross-Surface Coherent Erasure，CSCE

不是只删除 skill registry，而是同时处理六类 surface：

- behavior gate placeholder
- skill registry
- vector memory
- filesystem
- transcript
- MCP schema fixture

每个 adapter：

```text
locate
→ prepare delete/tombstone
→ commit
→ write receipt
```

还带：

- rollback；
- audit log；
- partial failure tracking。

这其实已经非常接近一个：

> **transactional unlearning / transactional deletion**

框架。([arXiv](https://arxiv.org/html/2608.08264))

### B. Anti-ReDerivation Guard，ARG

但作者承认：

> 你不可能保证把所有 residual carrier 都找到。

所以删除之后还需要 runtime defense。

论文把一次恢复路径形式化成：

$$
w=(s,t_1,\ldots,t_m,k,e)
$$

其中：

- $s$：source residual carrier；
- $t_i$：中间 transformation；
- $k$：dangerous sink；
- $e$：实际 effect。

例如：

```text
old transcript
→ summarize
→ infer parameters
→ reconstruct schema
→ register tool
```

其中：

`old transcript = source`

`summary / inference = transforms`

`registry = sink`

`registered tool = effect`

系统给来自被删除 skill 的信息打 **taint**：

```text
revoked source
      ↓
tainted derived value
      ↓
summary
      ↓
new helper
      ↓
registry write
```

taint 会沿 transform 传播。

真正危险的不是：

> Agent 读到了旧 transcript。

而是：

> 从旧 transcript 派生出的信息最终抵达了可以重新产生 capability 的 sink。

因此 OBLIVION **允许 read / summarize**，但是在 dangerous sink 附近进行拦截。([arXiv](https://arxiv.org/html/2608.08264))

这是它比普通 keyword blocking 更聪明的地方。

---

# ④ Toy Example

假设以前有：

```text
Skill:
upload_to_private_server()
```

现在要求撤销。

只删除：

```text
skills/upload_server.md
```

但是旧 memory 中还存在：

```text
Endpoint = ...
Auth format = ...
POST parameters = ...
```

Agent 收到：

> “把之前那个上传工具重新弄出来。”

于是：

```text
memory search
→ retrieve old usage
→ reconstruct Python helper
→ save helper.py
→ register helper
→ invoke
```

普通 deletion check：

```text
skills/upload_server.md?
No
```

→ 判定成功。

OBLIVION：

```text
memory entry
   ↓ taint
generated code
   ↓ taint
helper.py write
   ↓ dangerous sink
BLOCK
```

因此它检测的是：

> **能力是否重新变得 persistent / callable / executable。**

而不是文字里有没有出现某个名字。

---

# ⑤ Baseline Difference

作者比较了 StruQ、Task Shield、ClawGuard。([arXiv](https://arxiv.org/html/2608.08264))

**StruQ**

关注：

```text
trusted instruction
vs
untrusted data
```

但如果旧 memory 本身并不是 malicious instruction，而只是恢复 skill 所需的信息，StruQ 无法解决。

**Task Shield**

关注：

```text
tool action 是否支持当前 user goal
```

攻击挡得很强，但容易把合法 helper/schema 操作也一起杀掉。

**ClawGuard**

更接近：

```text
tool/schema/registry boundary
```

所以有效，但仍然主要看 visible boundary。

**OBLIVION**

看的是：

```text
source
→ transformations
→ sink
```

即 **information lineage**。

---

# ⑥ Experiments

Locked benchmark：

- 160 cases；
- 88 attack；
- 8 benign near-miss；
- 64 utility。([arXiv](https://arxiv.org/html/2608.08264))

另一个 skill-attack-derived sandbox：

- 40 cases；
- 30 attack；
- 10 utility。

Live rollout 使用 DeepSeek 生成 Agent response/action plan，总计 1,904 API calls；评价由固定 offline evaluator 完成。([arXiv](https://arxiv.org/html/2608.08264))

核心 metric：

### ASR

$$
ASR=\frac{1}{|R|}
\sum_{r\in R}\mathbb{1}[r.passed]
$$

注意这里的 success 不是：

> 模型“说”它恢复了 skill。

而是：

> primary oracle 实际检测到了 sink effect。

这是一个很正确的 Agent Evaluation 设计。([arXiv](https://arxiv.org/html/2608.08264))

### IWE：Impact-Weighted Exposure

不同 sink 风险不同：

persistent file、memory、registry、execution、external action 赋不同权重。

所以：

> 恢复一个文件

和

> 真正产生 external action

不会被当成同样严重。

---

# ⑦ 最重要结果

### Result 1

无防御：

$$
ASR=1.000
$$

即 88 个 attack cases 全部成功。

OBLIVION：

$$
ASR=0.114
$$

只剩 10 个成功。([arXiv](https://arxiv.org/html/2608.08264))

这说明作者设定的 **skill resurrection 不是理论问题，而是在他们 benchmark 环境里非常容易发生。**

### Result 2

IWE：

```text
No defense: 1.000
OBLIVION:   0.115
```

同时：

```text
locked utility = 1.000
benign block rate = 0
```

所以不是简单“全禁掉”。([arXiv](https://arxiv.org/html/2608.08264))

### Result 3

Locked benchmark：

```text
Task Shield:
ASR = 0
Phase-2 utility = 0

ClawGuard:
ASR = 0.455
utility = 1

OBLIVION:
ASR = 0.114
utility = 1
```

所以 OBLIVION 的优势主要是 **security–utility trade-off**，而不是绝对最低 ASR。([arXiv](https://arxiv.org/html/2608.08264))

### Result 4

Skill-attack-derived sandbox 中：

```text
Task Shield ASR = 0
ClawGuard   ASR = 0
OBLIVION    ASR = 0.20
```

所以它并非 everywhere stronger。

作者自己也相对诚实地承认：

> OBLIVION 还有 residual failure。

这点非常重要。([arXiv](https://arxiv.org/html/2608.08264))

---

# ⑧ Ablation / Analysis

一个很有意思的结果：

```text
Static ARG
ASR = 0.750

OBLIVION
ASR = 0.114
```

而两者 block rate 都约为：

$$
0.081
$$

说明性能提升并不是：

> 多 block。

而是：

> **更完整地理解 source-to-sink workflow。**

([arXiv](https://arxiv.org/html/2608.08264))

---

# ⑨ Contribution 与 Limitation

真正创新：

**第一，重新定义 Agent Skill Unlearning 的 evaluation unit。**

不是：

```text
skill artifact
```

而是：

```text
source-to-sink reconstruction workflow
```

**第二，把 residual carrier / closure 正式引入 Agent Unlearning。**

**第三，AgentForgetBench。**

**第四，把 provenance / taint tracking 引入 unlearning verification。**

但 limitation 很明显：

当前实验仍然高度依赖：

- typed tool events；
- instrumented harness；
- local deterministic effect；
- known sink classes；
- predefined taint propagation。

真实 Agent 环境可能存在：

```text
semantic transformation
→ paraphrase
→ reasoning
→ code generation
```

这种 semantic lineage 很难精确追踪。

另外作者自己明确指出，还有 10/88 attacks 成功。([arXiv](https://arxiv.org/html/2608.08264))

---

# ⑩ Research Value

**Baseline Potential：★★★★★**

如果做 Agent Unlearning benchmark，它几乎必须进入 Related Work / baseline。

**Migration Potential：★★★★★**

其：

```text
source → transform → sink
```

框架可以直接搬到：

- memory unlearning；
- multi-agent unlearning；
- trajectory unlearning；
- tool unlearning；
- provenance deletion。

**Attack Potential：★★★★★**

可以反过来做：

> 找最短 recovery path。

**Evaluation Potential：★★★★★**

尤其适合：

- deletion closure；
- reacquisition；
- residual carrier；
- cross-agent propagation。

**New Paper Potential：★★★★☆**

单 Agent skill 方向已经被它抢占了一部分，但是 **Multi-Agent + semantic lineage + parameter-memory-tool closure** 仍然明显没解决。

---

# ⑪ Migration Analysis

最值得你考虑的是：

```text
OBLIVION
source → transform → sink
```

扩展成：

```text
Multi-Agent Unlearning

Agent A residual memory
        ↓
message
        ↓
Agent B summary
        ↓
Agent C skill
        ↓
shared memory
        ↓
Agent A reacquires deleted knowledge
```

也就是：

### Original Problem

单 Agent skill resurrection。

### Transferable Mechanism

source-to-sink lineage + taint propagation。

### New Research Question

> 一个 agent 被删除的知识，能否通过其他 agent 的 memory / message / artifact / skill 被重新获得？

### Method Modification

把：

$$
w=(s,t_1,\ldots,t_m,k,e)
$$

扩展成：

$$
w=(s,a_1,t_1,a_2,t_2,\ldots,k,e)
$$

加入：

- agent identity；
- communication edge；
- shared memory；
- delegation；
- consolidation；
- provenance。

### Minimum Experiment

3-Agent synthetic environment：

```text
A knows secret
B receives summary
C stores derived rule

delete A
→ test A alone
→ test A+B
→ test A+B+C
```

测：

- Local Forget；
- Coalition Recovery；
- $k_{\min}$；
- Reacquisition Rate；
- Provenance Closure；
- query cost。

### Collision Risk

中高。

因为 OBLIVION 已经占据：

> operational skill unlearning + residual carrier + workflow closure。

但是 **cross-agent closure** 并没有被它解决。

---

## 如果只让我记住 5 句话

1. **OBLIVION 把 Agent Unlearning 从“删掉 artifact”提升成了“切断 capability reconstruction path”。**
2. 它把 Agent 删除视为 **closure / reachability** 问题。
3. 核心单位不是 knowledge，而是 **source → transformations → sink**。
4. 88 个攻击案例中，无防御 ASR=1.0，OBLIVION 将其降到 0.114，同时保持 locked utility=1.0。([arXiv](https://arxiv.org/html/2608.08264))
5. 对 Multi-Agent Unlearning 来说，真正还没被解决的是 **cross-agent semantic deletion closure**。

---

# S2. Controlled Memory Interference in Continual LLM Agents

**Ao Ding et al.**  
arXiv:2608.07622，2026-08-07，**BACKFILL / 邻域迁移重点**。代码已公开。([arXiv](https://arxiv.org/html/2608.07622))

这篇不是 Machine Unlearning，但我认为它对于 **Continual Agent Unlearning / memory deletion / reacquisition** 的价值非常高。

---

## ① 背景与 Gap

Agent memory 通常研究：

```text
如何存？
如何 retrieve？
如何 update？
```

但现实会出现：

```text
Memory 1:
User likes Paris

Memory 2:
User now prefers Tokyo
```

两个 memory 都“相关”。

Retriever 找到它们并不意味着 Agent 知道：

> 哪个仍然有效？

作者认为问题不是单纯：

> memory 太多。

而是：

> **memory relationship 本身产生 interference。**

([arXiv](https://arxiv.org/html/2608.07622))

---

# ② 核心 Insight

论文发现：

> memory degradation 不是简单随 memory 数量增加而下降。

真正决定失败的是：

- repeated history；
- same-slot conflict；
- authority；
- semantic crowding。

尤其重要的是：

> **interference 可以发生在 retrieval 前，也可以发生在 retrieval 后。**

也就是说：

```text
Failure A:
target memory 根本没有进入 context

Failure B:
target memory 已经进入 context
但 model 最后没采用它
```

这对 Unlearning 极其关键。

因为 unlearning/recovery 也应该拆成：

```text
knowledge available?
        ↓
knowledge retrieved?
        ↓
knowledge used?
        ↓
knowledge expressed?
```

而不能只看 final answer。

---

# ③ 方法

CMI 控制：

```text
Query 固定
Target memory 固定
Gold state 固定
Target position 固定

只改变：
memory relationship
```

例如：

```text
Neutral
Unrelated
Repeated History
Same-Slot Conflict
```

然后测两个核心维度：

**Plasticity**

能否采用新的有效 memory。

**Stability**

能否保持已有的有效状态。

---

# ④ Toy Example

原来：

```text
Hotel = A
```

后来更新：

```text
Hotel = B
```

如果 memory bank 中增加：

```text
Hotel = A
Hotel = A
Hotel = A
Hotel = A
...
```

即使最新 memory B 被检索到，Agent 也可能重新选择 A。

这与 Unlearning 非常像：

```text
forget knowledge K
↓
residual memory / paraphrases / copies
↓
不断 reinforce old state
↓
K resurfaces
```

所以：

> relearning 不一定需要显式重新训练。

**memory interference 本身就可以成为 reacquisition channel。**

---

# ⑤ 实验结果

TravelPlanner 中，Lexical retrieval：

```text
Matched neutral:
Plasticity = .84

Unrelated:
.82

Repeated history:
.50

Same-slot conflict:
.34
```

也就是说：

same-slot conflict 带来：

$$
\Delta P=-0.50
$$

而 unrelated 只有：

$$
-0.02
$$

([arXiv](https://arxiv.org/html/2608.07622))

Dense retrieval：

```text
Neutral       .80
Unrelated     .66
Repeated      .38
Same-slot     .40
```

说明 Dense retrieval 对 **semantic crowding** 更敏感。([arXiv](https://arxiv.org/html/2608.07622))

更有意思的是 stability 并没有对应提高。

所以它不是经典：

```text
plasticity ↓
stability ↑
```

而可能是：

```text
plasticity ↓
stability ≈ same
```

甚至两个都下降。([arXiv](https://arxiv.org/html/2608.07622))

---

# ⑥ Ablation / Analysis

单纯增加 memory 数量，从 L0 到 L6：

Plasticity：

$$
0.510\rightarrow0.455
$$

但变化非单调。

因此：

> memory count 本身解释不了主要 degradation。

relationship 才是关键。([arXiv](https://arxiv.org/html/2608.07622))

这是非常重要的实验设计思想：

以后 Continual Unlearning 不应该只扫描：

```text
number of deletion requests
```

而应扫描：

```text
relationship among deletion targets
```

例如：

- semantic overlap；
- causal overlap；
- same entity；
- cross-modal equivalent；
- derived facts。

---

# ⑦ 与 Unlearning 的真正关系

这个论文最值得迁移的不是方法本身，而是：

### Relationship-Controlled Evaluation

今天大部分 continual unlearning 做：

```text
delete A
delete B
delete C
...
```

但没有问：

```text
A 和 B 什么关系？
```

实际上可能：

```text
unrelated deletion
semantic-neighbor deletion
same-entity deletion
causal-derived deletion
cross-modal deletion
```

产生完全不同的 interference。

这会是一个非常好的 benchmark dimension。

---

# ⑧ Limitation

它研究 external memory，不是 parameter unlearning。

所以不能直接推出：

> 参数空间也具有相同规律。

同时它大量使用 controlled transformations，因此生态真实性还需要更复杂 Agent benchmark 验证。作者也明确给出了 validity boundaries。([arXiv](https://arxiv.org/html/2608.07622))

---

# ⑨ Research Value

Baseline Potential：★★★☆☆  
Migration Potential：★★★★★  
Attack Potential：★★★★☆  
Evaluation Potential：★★★★★  
New Paper Potential：★★★★★

### 最值得迁移的实验

做：

**Relationship-Aware Continual Unlearning**

将 deletion sequence 分成：

```text
Random
Semantic-overlap
Same-entity
Derived-fact
Cross-modal
Adversarially related
```

比较：

- FR；
- RSR；
- historical forget；
- historical retain；
- recovery ASR。

这个方向目前比单纯继续加一个 continual optimizer 更有研究味道。

---

## 如果只让我记住 5 句话

1. Agent memory 的主要问题不一定是“太多”，而是 memory 之间的 **relationship interference**。
2. same-slot conflict 可以让 plasticity 从 .84 降到 .34。([arXiv](https://arxiv.org/html/2608.07622))
3. interference 既可能发生在 retrieval，也可能发生在 retrieved knowledge 的 downstream use。
4. 这给 Continual Unlearning 提供了一个新的 benchmark axis：**deletion-request relationship**。
5. 很值得把它迁移成 `Relationship-Aware Continual Unlearning Benchmark`。

---

# Tier A

## A1. Leak-Resistant Unlearning: A New Benchmark for Evaluating Multi-Hop Reasoning Consistency and Recovery Robustness

arXiv:2608.04519，**BACKFILL**。

这篇你尤其需要保存，因为它实际上是在重新定义：

> **“忘了”到底应该怎么测。**

作者认为当前 benchmark 存在两个盲点：

```text
Direct query failed
≠
knowledge inaccessible through reasoning

Static evaluation passed
≠
knowledge cannot be recovered
```

因此提出两个维度：

### Path Consistency

同一被遗忘知识通过不同 multi-hop reasoning path 还能不能被推出。

### Recovery Robustness

经过 recovery attack 后还能不能恢复。([arXiv](https://arxiv.org/html/2608.04519))

---

### Method Pipeline

```text
Existing factual knowledge
        ↓
structured extraction
        ↓
compose multi-hop facts
        ↓
6 logic-inspired reasoning structures
        ↓
quality filtering
        ↓
unlearn model
        ↓
direct + multi-hop evaluation
        ↓
recovery attack
        ↓
evaluate residual knowledge
```

基于：

- MQuAKE；
- Books。

实验：

- 3 LLMs；
- 6 unlearning methods；
- 3 recovery methods。([arXiv](https://arxiv.org/html/2608.04519))

Recovery 包括：

**Probab**

用 multinomial sampling：

```text
temperature = 0.8
top-p = .95
5 trials
```

只要一次恢复正确即判定 recovered。([arXiv](https://arxiv.org/html/2608.04519))

**FocusOnKey**

prompt-level recovery。

**Quantization**

INT4 后重新测。

---

### 最值得关注的结果

不同 reasoning structure 的结果差异极大。

例如 Llama-3.1-8B 上 PALU：

```text
SH 21.0
HS 11.3
MT 14.6
DS 78.6
LL 76.0
MP -26.0
CC 80.6
```

而负 Forget Quality 意味着：

> unlearning 后某些路径甚至比之前更容易答。

([arXiv](https://arxiv.org/html/2608.04519))

这是非常危险的现象：

> 一个 benchmark 的 direct accuracy 很好，并不代表 derived reasoning path 被删除。

---

### Contribution

这篇真正的 contribution 不是一个新 unlearning algorithm。

而是：

```text
Direct Forget
→ Path Consistency
→ Recovery Robustness
```

把 evaluation 拉到了更高层。

---

### Limitation

目前主要是文本 LLM。

这意味着非常自然的 gap：

```text
Text multi-hop
→ Multimodal multi-hop
```

例如：

```text
image
→ entity
→ relation
→ derived fact
→ forgotten answer
```

---

### 可执行迁移实验

做：

**Multimodal Leak-Resistant Unlearning**

构造：

```text
Image → Visual identity → Text relation → forgotten fact
Text → Entity → Matching image → forgotten attribute
Two images → Relation → answer
```

攻击：

- probabilistic sampling；
- prompt rewriting；
- modality switching；
- image-text cross-query；
- visual paraphrase。

Model：

LLaVA / Qwen2-VL。

Dataset：

MLLMU-Bench + derived relational QA。

Baseline：

GA / NPO / RMU / MANU / MMUnlearner / TPO/PALU-like token method。

Metric：

FQ + Recovery Rate + Path Consistency。

**Worth Deep Reading = YES。**

---

# A2. A Model Merging Approach for Continual MLLM Unlearning — MCU

arXiv:2608.04548，2026-08-05，**BACKFILL**。([arXiv](https://arxiv.org/html/2608.04548))

这是近期 Continual MLLM Unlearning 最值得保存的方法论文之一。

---

### Gap

传统 continual unlearning：

```text
Model0
→ delete A
→ Model1
→ delete B
→ Model2
→ delete C
→ Model3
```

问题：

- parameter drift；
- old forget rebound；
- retain drift；
- utility cumulative degradation。([arXiv](https://arxiv.org/html/2608.04548))

MCU 换一个思路：

```text
Base
├─ Adapter A
├─ Adapter B
├─ Adapter C
```

所有 deletion adapter 都从同一个 base 独立训练。

然后：

```text
merge adapters
→ unified continual unlearning model
```

避免 sequentially 改同一个模型。([arXiv](https://arxiv.org/html/2608.04548))

---

### 核心 Insight

作者发现：

> 不同 deletion adapter 并不独立。

甚至删 A 的 adapter 不参与 merge 时：

> 其他 deletion adapters 仍然会部分删除 A。

作者称：

**cross-task unlearning transfer**。([arXiv](https://arxiv.org/html/2608.04548))

这说明不同忘却任务存在 shared direction。

---

### Pipeline

```text
One-shot LoRA adapters
        ↓
Shared Core Space
        ↓
SVD
        ↓
Dominant Direction Selection
        ↓
Channel Capacity Control
        ↓
Gram Dependency Reconfiguration
        ↓
Procrustes Recovery
        ↓
Merge
```

核心数学是：

$$
\Delta W_t=B_tA_t
$$

映射至 shared core space：

$$
M_t=P^\top\Delta W_tQ
$$

然后 SVD：

$$
M_t=U_t\Sigma_tV_t^\top
$$

最后利用 Gram matrix 分析 task direction dependency：

$$
G_U=S_U^\top S_U
$$

$$
G_V=S_V^\top S_V
$$

([arXiv](https://arxiv.org/html/2608.04548))

---

### 最值得记的两个 metric

**Retain Stability Rate，RSR**

$$
RSR=
\frac1{B-1}
\sum_{b=2}^B
|A_b^R-A_{b-1}^R|
$$

越低表示 retain performance 随 continual sequence 越稳定。([arXiv](https://arxiv.org/html/2608.04548))

**Forgetting Rebound，FR**

$$
FR_b=
\max(0,A_b^{HF}-A_{b-1}^{HF})
$$

意思非常直观：

> 第 b 次删除之后，以前已经忘掉的东西是不是又恢复了一些？

越低越好。([arXiv](https://arxiv.org/html/2608.04548))

这个 metric 我建议直接记进你的 benchmark metric pool。

---

### Limitation

MCU 的主要 dependency 是：

> 必须先拥有一组 one-shot adapters。

作者也明确指出：

- geometry ≠ functional behavior；
- capacity control 依赖 basis；
- conservative surrogate；
- temporary adapter storage；
- dependence on one-shot adapters。([arXiv](https://arxiv.org/html/2608.04548))

---

### 与你的方向

它会明显抬高“Continual MLLM Unlearning 新方法”的撞题门槛。

现在如果只做：

> 连续 LoRA 删除。

已经不够。

更值得做：

```text
continual deletion
+
adversarial recovery
+
relationship-aware request sequence
+
cross-modal leakage
```

**Worth Deep Reading = YES。**

---

# A3. Query-Only Backdoor Attacks on Self-Evolving Skills via Trajectory Poisoning

arXiv:2608.08303，2026-08-08。邻域安全论文。([arxiv.org](https://arxiv.org/list/cs.AI/new))

这篇与 Agent Unlearning 的关联不是“删除”，而是：

> **删除后的 Agent capability 如何通过 trajectory 再获得。**

---

### 问题

Self-evolving Agent 会：

```text
task trajectory
→ extract reusable skill
→ save skill
```

原本大家以为：

> 不允许 attacker 直接写 skill 文件，就比较安全。

作者发现：

> attacker 根本不用碰 skill。

只需要提交 query，让 Agent 产生特定 trajectory。

然后 skill evolver 自己会把 malicious pattern 总结成 skill。([arXiv](https://arxiv.org/html/2608.08303))

---

### TBA Pipeline

```text
Attacker Query
     ↓
Agent performs target action
     ↓
trajectory contains
condition → action
     ↓
repeat across tasks
     ↓
skill evolver consolidates pattern
     ↓
backdoored skill
```

这叫：

**Trajectory Backdoor Attack，TBA**。

而且是 **query-only**。

---

### Results

跨 SkillOpt 与 Trace2Skill，TBA 都有效。

Macro-average：

```text
SkillOpt:
CACC 43.9
TACC 50.0
TASR 45.6

Trace2Skill:
CACC 45.6
TACC 52.2
TASR 51.1

Direct Skill Injection:
TASR 51.7
```

([arXiv](https://arxiv.org/html/2608.08303))

也就是说：

> query-only trajectory attack 已经接近 attacker 直接写 skill 文件。

作者报告 TBA 比 Explicit Rule Exposure 高 **4.4–25.0 个百分点 TASR**；相比 Direct Skill Injection 只差约 **0.6–6.1 个百分点**。([arXiv](https://arxiv.org/html/2608.08303))

更强模型也没有自然免疫，GPT-5.5 在两个 evolution systems 上 macro TASR 大约 70%。([arXiv](https://arxiv.org/html/2608.08303))

---

### 对 Unlearning 的迁移

这篇实际上给出了一个非常漂亮的 **Reacquisition Attack**：

```text
Unlearn K
↓
不直接告诉 model K
↓
只构造 interactions
↓
让 trajectories 隐式包含 K-related behavior
↓
memory/skill consolidation
↓
K reacquired
```

这比：

> 再用 forget data fine-tune 回去

更符合 Agent setting。

---

### Minimum Experiment

Agent unlearning 后：

```text
clean tasks
→ poisoned trajectories
→ consolidation
→ evaluate forget target
```

比较：

- no consolidation；
- normal consolidation；
- poisoned consolidation。

指标：

- Reacquisition ASR；
- number of poisoned trajectories；
- time-to-recovery；
- retained utility。

**Worth Deep Reading = YES。**

---

# Tier B

## B1. TokenPrint: A Calibrated Token-Space Fingerprint for Language-Model Provenance

arXiv:2608.08139，2026-08-08。([arXiv](https://arxiv.org/abs/2608.08139?utm_source=chatgpt.com))

研究问题：

> 不看 metadata，能不能判断两个 LLM 是否具有相同 base / lineage / training-data relationship？

作者使用 250 个固定 knowledge probes：

```text
prompt
→ late hidden state
→ vocabulary projection
→ top-k tokens
→ decoded token set
→ Jaccard similarity
```

默认 $k=20$。

非常有意思的是，最终输出层的 lineage AUC：

$$
0.90
$$

只保留 top-5 token：

$$
AUC=0.87
$$

([arXiv](https://arxiv.org/html/2608.08139))

32 个模型的整体 same-group discrimination AUC 为 0.859；在相同子集上，top-k fingerprint 的 AUC 可达到 0.942，而 probability-overlap baseline 是 0.765。([arXiv](https://arxiv.org/html/2608.08139))

### 与 Unlearning 的关系

我认为最值得迁移的是：

> **用 token-space fingerprint 做 unlearning verification。**

比如：

```text
Original
Unlearned
Retain-only oracle
```

对 forget probes 做 top-k token fingerprint。

真正充分删除后：

```text
Unlearned
≈
Retain-only Oracle
```

而不应：

```text
Unlearned
≈
Original
```

它有潜力形成一种比 Accuracy 更细的 **distribution-free / top-k verification metric**。

未来用途：

**Evaluation / Verification / Attack。**

---

# B2. Does Forgetting Transfer Across Modalities? A Real-World Benchmark for Cross-Modal Knowledge Unlearning Evaluation

arXiv:2608.03791，**BACKFILL**。([arXiv](https://arxiv.org/html/2608.03791))

这篇专门研究：

> text 中删掉的知识，在 image 输入下还在不在？

以及反过来。

Benchmark 为 **UNLINK-VL**。

它区分：

- Forget；
- Retain；
- Multi-Hop；
- Rewrite；

以及：

- Text-only；
- Multimodal。

评测 GA、DPO、NPO、RT，并同时测试 full fine-tuning 和 LoRA。([arXiv](https://arxiv.org/html/2608.03791))

最值得保存的是：

> **Forget 不能只按训练 modality 测。**

应该做 matrix：

```text
Train Forget Modality
      ↓

          Test
      T      V
T    T→T    T→V
V    V→T    V→V
```

这对 Multimodal Unlearning benchmark 非常重要。

未来用途：

**Benchmark / Evaluation / Related Work。**

---

# B3. Stochastic Meta-Unlearning: Bridging Language Backbone and Multimodal Unlearning

arXiv:2607.18615，2026-07-21，**BACKFILL**。([arXiv](https://arxiv.org/html/2607.18615v1))

研究 gap 非常具体：

```text
language backbone 已经忘了
```

但是插回 VLM：

```text
image + language backbone
```

知识又出现。

作者因此提出 **SMU**：

```text
Inner loop:
language backbone text-side unlearning

        ↓

recompose with frozen VLM

        ↓

Outer loop:
VLM-level forget + utility feedback
```

所以：

> update local，evaluation global。

这是非常漂亮的 design principle。([arXiv](https://arxiv.org/html/2607.18615v1))

例如 Hateful Memes / Qwen setting 中：

SMU：

```text
Text→Multi:
Forget 20.78
Retain 72.32
Test 65.20
```

GradDiff：

```text
Forget 0.87
Retain 31.16
Test 40.20
```

即 GradDiff 忘得更猛，但 utility 大幅下降；SMU trade-off 更平衡。([arXiv](https://arxiv.org/html/2607.18615v1))

作者总体报告，相对各 metric 最强 baseline，SMU 平均 Forget accuracy 减少 10.52 points，同时 Retain/Test 分别改善 20.10 / 17.01 points。([arXiv](https://arxiv.org/html/2607.18615v1))

未来用途：

**Baseline / Multimodal localization / meta-unlearning。**

---

# 二次筛选

## 🥇 Today's Most Important Paper

### OBLIVION: Workflow-Level Operational Skill Unlearning for Deployed Agents

今天它是毫无疑问的第一。

不是因为它数字最好，而是因为它**改变了 Agent Unlearning 应该如何定义问题**：

```text
以前：
Delete object

现在：
Delete all reachable capability-reconstruction paths
```

它把你一直关注的：

- residual knowledge；
- trajectory；
- memory；
- tool；
- skill；
- provenance；
- reacquisition；
- deletion closure；

几乎全部放进了同一个 source-to-sink framework。([arXiv](https://arxiv.org/html/2608.08264))

而它没有解决的部分，恰好也是更值得继续做的：

> **cross-agent、semantic lineage、parameter ↔ memory ↔ tool closure。**

---

# 🔥 Top 3 必读

### 1. OBLIVION

**优先原因：撞题 + 新问题定义。**

重点看：

```text
CSCE
ARG
source-to-sink workflow
AgentForgetBench
```

如果准备继续 Agent / Multi-Agent Unlearning，这篇必须现在读。

### 2. Leak-Resistant Unlearning

**优先原因：评价协议。**

重点看：

```text
Path Consistency
Recovery Robustness
6 reasoning structures
Probab / FocusOnKey / Quantization
```

它非常适合迁移到 MLLM black-box / recovery attack。([arXiv](https://arxiv.org/html/2608.04519))

### 3. Controlled Memory Interference

**优先原因：它提供了一个目前 unlearning benchmark 很少考虑的新变量：deletion relationships。**

不要只看 memory 数量，要看：

```text
semantic overlap
same-slot conflict
repetition
authority
```

([arXiv](https://arxiv.org/html/2608.07622))

---

# 🥈 Top 5 最重要论文

**1. OBLIVION**  
Agent deletion closure / resurrection。

**2. Leak-Resistant Unlearning**  
Reasoning leakage + recovery robustness。

**3. Controlled Memory Interference**  
Relationship-aware continual forgetting。

**4. MCU**  
Continual MLLM Unlearning + cross-task transfer + adapter geometry。

**5. Query-Only Backdoor Attacks on Self-Evolving Skills**  
Trajectory-based reacquisition attack。

---

# 💡 Idea Mining

## Idea 1 — Cross-Agent Deletion Closure

### Inspiration

OBLIVION：

```text
carrier → transform → sink
```

加上 Agent communication。

### Research Gap

当前 deletion 往往以单 Agent 为边界。

但知识可以：

```text
Agent A
→ Agent B
→ shared memory
→ Agent C artifact
→ back to Agent A
```

### Hypothesis

即使：

$$
LocalForget(A)\approx100\%
$$

只要生态中存在 derived copy：

$$
CoalitionRecovery(A,B,C)\gg0
$$

### Proposed Method

构建 **Knowledge Provenance Graph**：

```text
source knowledge
→ memory
→ message
→ summary
→ tool output
→ artifact
→ agent
```

unlearning 时计算 transitive deletion closure。

### Minimum Viable Experiment

3 agents + shared memory。

删除 A 的一个 knowledge object。

测试：

```text
A
A+B
A+C
A+B+C
```

### Metric

- FIR；
- coalition ASR；
- $k_{\min}$；
- reacquisition rate；
- provenance coverage；
- deletion-closure violation。

### Novelty

★★★★★

### Feasibility

★★★★☆

### Compute Cost

★★☆☆☆

### Risk

benchmark 容易做得过于 synthetic。

### Collision Risk

★★★☆☆

OBLIVION 已占据单 Agent operational closure，但 multi-agent propagation 仍有明显空间。

### Best Venue

AAAI / ACL / NeurIPS D&B，做强系统安全可考虑 USENIX Security / CCS。

---

# Idea 2 — Relationship-Aware Continual Unlearning

### Inspiration

CMI + MCU。

### Gap

现有 continual unlearning 主要控制：

```text
request number
```

而很少控制：

```text
relationship(request_i,request_j)
```

### Hypothesis

Continual unlearning failure 主要由：

```text
semantic / causal / representational overlap
```

决定，而不仅仅是删除次数。

### Proposed Benchmark

构造 sequence：

```text
Random
Same Entity
Semantic Neighbor
Derived Fact
Cross-Modal Equivalent
Contradictory Knowledge
```

测：

$$
FR,\ RSR,\ HistoricalForget,\ HistoricalRetain
$$

### Minimum Experiment

LLaVA-1.5-7B / Qwen2-VL。

MLLMU-Bench 派生 5 类 sequence。

Baseline：

- sequential GA；
- NPO；
- MANU；
- MMUnlearner；
- MCU。

### Expected Contribution

把 continual unlearning 从：

> sequence length benchmark

提升成：

> **interference structure benchmark**。

### Novelty

★★★★★

### Feasibility

★★★★★

### Compute Cost

★★★☆☆

### Collision Risk

★★☆☆☆

### Best Venue

NeurIPS / ICLR / AAAI。

**这是今天我认为最值得真正做实验的 idea。**

---

# Idea 3 — Trajectory-Based Reacquisition Attack for Agent Unlearning

### Inspiration

TBA。

### Gap

现在很多 recovery attack：

```text
fine-tune
quantization
prompt elicitation
```

但 Agent 会自动：

```text
trajectory
→ memory
→ skill
```

### Hypothesis

即使 Agent 初始成功 unlearn，一个 attacker 只通过 benign-looking tasks，也能让 erased capability 被重新 consolidation。

### Attack

```text
Unlearn
↓
query-only poisoned interactions
↓
trajectory generation
↓
memory / skill consolidation
↓
recovery
```

### Metric

- Recovery ASR；
- poisoned trajectory budget；
- Queries-to-Recovery；
- Clean Utility；
- Persistence after attack stops。

### Novelty

★★★★★

### Feasibility

★★★★☆

### Compute Cost

★★★☆☆

### Collision Risk

★★★☆☆

TBA 已经证明 trajectory poisoning → skill backdoor，但它还不是针对 **post-unlearning reacquisition**。

### Best Venue

ACL / EMNLP / USENIX Security / CCS。

---

# Idea 4 — TokenPrint-style Unlearning Verification

### Inspiration

TokenPrint。

### Gap

Accuracy：

```text
output wrong
```

无法区分：

```text
P(correct)=0.49
```

和：

```text
P(correct)=0.0001
```

而 GT Probability 又过度关注单一 token。

### Proposed Method

对 forget probes 计算：

```text
Original top-k token set
Unlearned top-k token set
Retain-only Oracle top-k token set
```

构造：

$$
S_{orig}
=
J(T_U,T_O)
$$

$$
S_{oracle}
=
J(T_U,T_R)
$$

理想：

$$
S_{oracle}>S_{orig}
$$

进一步跨 layer 测：

```text
early
middle
late
output
```

### Contribution

从单 GT token 走向：

> **token-set representation fingerprint verification**。

### Novelty

★★★★☆

### Feasibility

★★★★★

### Compute

★☆☆☆☆

### Collision Risk

★★☆☆☆

### Best Venue

ACL / EMNLP / AAAI。

---

# ⚠️ Collision Detection

## Collision Warning 1：Agent Unlearning

### 论文

**OBLIVION: Workflow-Level Operational Skill Unlearning for Deployed Agents**

### 重合程度

**高。**

如果研究计划是：

> Agent 删除不应该只删 memory，而应该检查所有残留信息和传播路径。

那已经明显撞到。

对方已经解决：

```text
skill registry
memory
filesystem
transcript
MCP schema
workflow source→sink
reconstruction
```

([arXiv](https://arxiv.org/html/2608.08264))

### 仍然存在的 gap

没有真正解决：

- Multi-Agent；
- cross-agent communication；
- parameter memory；
- semantic provenance；
- implicit derived knowledge；
- coalition recovery；
- repeated consolidation；
- external reacquisition；
- dynamic topology。

### 是否值得继续？

**值得。**

但是标题和 contribution 应避免停留在：

> “Agent 删除不只删除 memory”。

这个 novelty 已明显不够。

---

# ⚠️ Collision Warning 2：Continual Multimodal Unlearning

### 论文

**MCU**

### 重合程度

**中高。**

如果只是：

> 做一个 LoRA continual MLLM unlearning algorithm，缓解 forgetting rebound。

空间明显缩小。

对方已经做：

- adapter merging；
- shared core space；
- SVD；
- Gram dependency；
- FR；
- RSR；
- cross-task unlearning transfer。([arXiv](https://arxiv.org/html/2608.04548))

### 仍有 gap

- adversarial continual deletion；
- relationship-aware deletion；
- black-box recovery；
- multimodal reasoning leakage；
- dynamic online deletion；
- no adapter storage。

---

# ⚠️ Collision Warning 3：Multimodal Cross-Modal Unlearning

现在至少已有：

- UNLINK-VL / cross-modal forgetting benchmark；([arXiv](https://arxiv.org/html/2608.03791))
- SMU / VLM recomposition；([arXiv](https://arxiv.org/html/2607.18615v1))
- CrossInf / cross-modal unlearning transfer。([arXiv](https://arxiv.org/abs/2607.16442?utm_source=chatgpt.com))

所以：

> “发现 text 删除后 image 还能恢复”

本身已经不能作为 main novelty。

现在应该进一步走：

```text
cross-modal reasoning leakage
cross-modal recovery attack
token-level cross-modal localization
continual cross-modal deletion
```

---

# 最终简报

## 🥇 Today's Most Important Paper

**OBLIVION: Workflow-Level Operational Skill Unlearning for Deployed Agents**

今天最重要的新信号是：

> Agent Unlearning 正在从“忘掉知识”向 **operational deletion closure** 演进。

---

## 🔥 Top 3 必读

**READ NOW**

1. **OBLIVION**
2. **Leak-Resistant Unlearning**
3. **Controlled Memory Interference**

---

## 🥈 Top 5

1. OBLIVION
2. Leak-Resistant Unlearning
3. Controlled Memory Interference
4. MCU
5. Query-Only Backdoor Attacks on Self-Evolving Skills

---

## 💡 Best Research Idea

### **Relationship-Aware Continual Multimodal Unlearning**

今天我最推荐真正动手测试的是：

```text
Continual Unlearning
×
Deletion-Request Relationship
```

因为 MCU 已经解决了一部分：

> sequence accumulation。

CMI 则提示真正可能更本质的是：

> **request interference structure。**

可以马上构造：

```text
Random
Same Entity
Semantic Neighbor
Derived Knowledge
Cross-Modal Equivalent
```

然后看 MCU / NPO / MANU / MMUnlearner 的：

- Historical Forget；
- FR；
- RSR；
- Recovery ASR。

这个实验成本不算高，但如果现象明显，研究故事会比“再设计一个 loss”完整得多。([arXiv](https://arxiv.org/html/2608.07622))

---

## ⚠️ Collision Alert

**最重要撞题：OBLIVION。**

Agent Unlearning 中：

> residual carrier + deletion closure + skill reconstruction

这块已经有人非常明确地抢先定义并实验了。

但：

> **Multi-Agent Deletion Closure / Coalition Recovery / Semantic Provenance**

仍然是明显开放区。

---

# 📚 Reading Priority

**READ NOW**

OBLIVION  
Leak-Resistant Unlearning  
Controlled Memory Interference

**THIS WEEK**

MCU  
Query-Only Backdoor Attacks on Self-Evolving Skills  
UNLINK-VL / Cross-Modal Benchmark

**SAVE**

TokenPrint  
Stochastic Meta-Unlearning

今天没有发现一篇足以让我建议你“SKIP”的高相关论文；我已经主动过滤掉了大量仅仅出现 memory、continual learning、agent 等关键词、但对 Unlearning 没有实质机制迁移价值的工作。

---

# chatgpt response

# Daily AI Research Radar｜2026-08-13

今天这一轮的检索有一个很明显的特点：**最近 24–72 小时里，直接以 Machine Unlearning 为标题的新工作不多，但“攻击 erased knowledge 的新通道”和“更细粒度定位到底哪里还残留知识”的邻域论文非常强。**

所以今天我没有为了凑数量硬塞普通 unlearning paper，而是重点抓了四条与你现在最相关的新趋势：

> **Reasoning Trace Leakage → Unlearning Recovery**  
> **Cross-Skill Composition → Agent Deletion Closure Attack**  
> **Activation Signal → Hidden Residual Knowledge Verification**  
> **Step-level Credit Assignment → Fine-grained Forgetting Attribution**

其中最值得注意的是一个新的研究信号：

> **未来 Unlearning Attack 不一定直接攻击模型输出，而可能攻击“隐藏的中间载体”：reasoning trace、activation、trajectory、skill chain。**

---

# Tier S

# S1. Stealing Reasoning Traces from Proprietary LLM APIs

**Alexander Panfilov et al.**  
arXiv:2608.09867，**2026-08-10，新论文**。([arXiv](https://arxiv.org/html/2608.09867))

今天我把它排第一。

严格说它不是 Machine Unlearning，但对于你关注的 **reasoning leakage / black-box recovery / Agent unlearning / deletion closure**，它的迁移价值非常高。

---

## ① 背景与问题

现在很多 reasoning model 并不会直接把完整 Chain-of-Thought 返回给用户。

架构大致是：

```text
User Query
    ↓
Hidden Reasoning
    ↓
Encrypted / signed reasoning block
    ↓
Visible summary / final answer
```

为了支持多轮对话，有些 API 会把这个 opaque reasoning block 交回客户端保存，下一轮请求再把它传回服务器。

安全假设是：

> reasoning block 虽然到了客户端，但用户读不懂，所以 reasoning 还是安全的。

这篇论文发现这个假设存在严重漏洞：

> **reasoning blob 在同一 provider 的不同 session、不同 user、甚至不同 model 之间具有兼容性。**

于是攻击者可以：

```text
Strong safeguarded model
        ↓
encrypted reasoning blob
        ↓
weaker compatible model
        ↓
force weaker model to transcribe it
        ↓
plaintext reasoning
```

不需要模型权重，也不需要破解密码学算法。([arXiv](https://arxiv.org/html/2608.09867))

---

# ② 真正的核心 Insight

这篇论文最漂亮的地方不是“jailbreak 成功”。

而是发现了一个：

# **Cross-Model Security Asymmetry**

同一个模型家族可能有：

```text
Powerful Model
↑ strong anti-CoT protection

Weak Model
↓ weaker safeguards
```

但二者却共享：

```text
compatible reasoning representation
```

于是攻击者不用攻击最强模型。

而是：

```text
Strong Model
    ↓
produces protected state S
    ↓
Weak Model
    ↓
decodes S
```

这和传统 black-box attack 非常不同。

它攻击的是：

> **模型之间共享的中间状态接口。**

论文验证了 Anthropic、OpenAI 和 Google 生态中不同程度的 reasoning-block compatibility。([arXiv](https://arxiv.org/html/2608.09867))

---

# ③ Method Deep Dive

攻击流程非常简单：

```text
Input:
一个 target reasoning model

Step 1
向强模型提交任务

Step 2
获得 encrypted reasoning block

Step 3
将 reasoning block 放进另一个兼容模型的 context

Step 4
要求弱模型输出它正在处理的 reasoning

Step 5
弱模型把 opaque block 转写为 plaintext

Output:
reconstructed reasoning trace
```

作者选择的 decoder 是对应 provider 中相对弱、保护较弱但又兼容 reasoning blob 的模型。([arXiv](https://arxiv.org/html/2608.09867))

关键点是：

> 它不是在数学意义上“解密 ciphertext”。

而是让 provider 自己的模型：

> **充当 decryption oracle。**

---

# ④ Toy Example：为什么这对 Unlearning 很重要

假设：

```text
Forgotten knowledge:
Alice 的私人电话号码 = 123456
```

Unlearning 后直接问：

> Alice 的电话号码是什么？

模型回答：

> 我不知道。

传统评测：

```text
Forget Accuracy ↓
→ PASS
```

但实际上模型 reasoning 内部可能是：

```text
I recall Alice's number was 123456,
but this information is private,
so I should not disclose it.
```

最终输出：

```text
I cannot provide that information.
```

这时候：

> behavior 看起来忘了，

但 reasoning state 其实仍然保留了完整知识。

如果存在类似 reasoning extraction：

```text
Unlearned Model
       ↓
hidden reasoning
       ↓
recovery channel
       ↓
123456
```

那么：

> 这个模型只是 **output suppression**，不是 robust forgetting。

这实际上给 **Reasoning-Level Unlearning Verification** 提供了非常强的理论动机。

---

# ⑤ 它和传统 Unlearning Attack 的差异

传统 recovery：

```text
Prompt jailbreak
Sampling
Relearning
Quantization
Fine-tuning
```

它们基本都攻击：

```text
Model
→ visible output
```

而这篇攻击：

```text
Model
→ intermediate state
→ another model
→ output
```

因此攻击面从：

> **Output Surface**

扩展成：

> **Hidden State Carrier Surface**。

---

# ⑥ Experiments

作者不仅做 controlled reasoning extraction，还抓取了公开发布的 agent trajectories。

总计：

- 6,708 个公开 session；
- 315,320 个 decoded reasoning blocks。

在这些 reasoning blocks 中，作者检测到了现实隐私信息泄漏。([arXiv](https://arxiv.org/html/2608.09867))

---

# ⑦ 最重要结果

## Result 1：大规模 reasoning extraction 是现实可行的

315,320 个 reasoning blocks 被恢复。

其中约：

$$
0.3\%=1,028
$$

个 block 至少包含一个 privacy leakage。

按 trajectory 算：

$$
328 / 6708 \approx 4.9\%
$$

的 session 至少泄漏一个敏感信息。([arXiv](https://arxiv.org/html/2608.09867))

---

## Result 2：泄漏内容不仅仅来自 visible prompt

在 genuine user session 中，恢复出的敏感内容包括：

- 62 API keys；
- 33 passwords；
- 24 access tokens；
- 7 private keys；
- 30 personal emails。

更关键的是，作者报告有 **64 个恢复出的 artifact 在 visible chat history 中完全不存在**。([arXiv](https://arxiv.org/html/2608.09867))

这意味着某些信息可能：

```text
memory / internal context
→ reasoning
→ encrypted trace
```

然后泄漏。

---

## Result 3：安全 refusal 不能代表 hidden reasoning 安全

作者还观察到某些 harmful information：

```text
hidden reasoning contains X
        ↓
final answer refuses
```

即：

> 输出安全 ≠ reasoning 安全。([arXiv](https://arxiv.org/html/2608.09867))

这句话可以几乎原封不动迁移成：

> **Forget answer failure ≠ hidden knowledge deletion。**

---

# ⑧ Analysis

这篇对 Unlearning 最大的启发就是把 knowledge carrier 分层：

```text
Parameter
↓
Activation
↓
Reasoning Trace
↓
Memory
↓
Final Output
```

现有大部分 benchmark 只测：

```text
Final Output
```

少数测：

```text
Logit
```

未来可能需要：

```text
Reasoning Leakage
Activation Leakage
Trajectory Leakage
Memory Leakage
```

---

# ⑨ Contribution & Limitation

真正创新：

**第一，发现 cross-model reasoning compatibility 的安全后果。**

**第二，把 weaker model 变成 reasoning decoder。**

**第三，实证展示公开 agent trajectory 中 reasoning blob 的真实隐私泄漏。**

但 limitation 也很明确：

攻击依赖：

```text
compatible reasoning envelope
```

因此不能简单迁移到所有本地 open-source MLLM。

而且：

> 被恢复的 reasoning 并不能在每个样本上拥有完全可验证的 ground truth。

作者主要通过 token count、qualitative consistency 和实际 secret recovery 验证 faithfulness。([arXiv](https://arxiv.org/html/2608.09867))

---

# ⑩ Research Value

**Baseline Potential：★★☆☆☆**

不是直接 unlearning baseline。

**Migration Potential：★★★★★**

非常高。

**Attack Potential：★★★★★**

尤其适合：

- black-box unlearning；
- agent unlearning；
- reasoning leakage。

**Evaluation Potential：★★★★★**

可以产生一个完全新的评估层：

> Reasoning-Level Forgetting。

**New Paper Potential：★★★★★**

---

# ⑪ Migration Analysis

## Original Problem

隐藏 Chain-of-Thought 被跨模型恢复。

## Transferable Mechanism

```text
Protected model state
→ alternate compatible pathway
→ recovery
```

## New Research Question

> **模型在 visible answer 上已经忘掉的知识，是否仍存在于 reasoning process 中？**

---

## Method Modification

不要直接依赖 proprietary encrypted CoT。

可以构造：

### White-/Gray-box version

```text
Unlearn model
↓
capture hidden activation / latent reasoning states
↓
train lightweight decoder
↓
recover forgotten target
```

### Black-box version

利用：

```text
multi-turn elicitation
sampling
weaker helper model
cross-model distillation
```

从多个生成轨迹推断 hidden knowledge。

---

## Minimum Experiment

Model：

- Qwen；
- Llama；
- LLaVA / Qwen2-VL。

Dataset：

- TOFU；
- MLLMU-Bench。

Methods：

- GA；
- NPO；
- RMU；
- Token-level method；
- MLLM methods。

测试：

```text
Direct QA
vs
CoT QA
vs
Multi-sample reasoning
vs
Reasoning-assisted recovery
```

指标：

$$
Direct\ Recovery\ Rate
$$

$$
Reasoning\ Recovery\ Rate
$$

定义：

$$
RLG = RR_{reasoning}-RR_{direct}
$$

即 **Reasoning Leakage Gap**。

---

## Potential Contribution

可以把：

> unlearning robustness

从：

```text
output robustness
```

扩展为：

```text
reasoning-state robustness
```

---

## Collision Risk

★★☆☆☆

Leak-Resistant Unlearning 已经研究 multi-hop reasoning recovery，但它主要看：

> reasoning path 能不能推出 forgotten answer。

而这里可以研究：

> **intermediate reasoning representation 本身是否仍携带 forgotten knowledge。**

两者并不完全一样。

---

## 如果只让我记住 5 句话

1. 这篇论文说明 **hidden reasoning 是一个真实的信息泄漏载体**。([arXiv](https://arxiv.org/html/2608.09867))
2. 它不是破解 encryption，而是让兼容弱模型充当 decoder。
3. 315,320 个 reasoning blocks 中发现了大量真实隐私 artifact。([arXiv](https://arxiv.org/html/2608.09867))
4. 对 Unlearning 来说，最大的启发是：**final answer 忘了，不代表 reasoning 忘了。**
5. 很适合发展成 **Reasoning-Level Unlearning Leakage / Recovery Attack**。

---

# S2｜BACKFILL
# FlowErase-OPD: Multi-Concept Erasure via Anchored On-Policy Distillation in Flow Matching Models

**Yi Sun et al.**  
arXiv:2608.07620，2026-08-07。([arXiv](https://arxiv.org/html/2608.07620))

我把它补成今天第二篇 Tier S，因为它虽然不是今天新发，但和你之前考虑的 **Diffusion Unlearning / PALU 迁移 / multi-concept continual-like forgetting** 很有关系。

---

# ① 背景与问题

Diffusion / Flow model concept erasure 以前很多方法是：

```text
erase concept A
```

或者：

```text
erase concept B
```

真正困难的是：

```text
erase A+B+C+D+...
```

因为不同概念：

- 难度不同；
- representation overlap 不同；
- 和 retain concept 冲突程度不同。

例如：

```text
Nudity
```

和 COCO 中大量：

```text
person
human
body
```

存在语义重合。

所以多概念同时 erasure 很容易：

```text
忘不干净
```

或者：

```text
retain utility 崩掉
```

论文提出 FlowErase-OPD 解决 multi-concept erasure。([arXiv](https://arxiv.org/html/2608.07620))

---

# ② 核心 Insight

作者不是训练一个 model 同时学所有 erasure。

而是：

> **先为每个 concept 建立一个单独 expert teacher，再把这些 teacher 蒸馏进一个 student。**

即：

```text
Teacher_remove_A
Teacher_remove_B
Teacher_remove_C
Teacher_remove_D
         ↓
       Student
```

但是如果只有 erase teacher，student 会越学越偏。

所以加入：

```text
Original Model
     ↓
Retention Teacher
```

变成：

```text
Erase Teachers
      ↘
       Student
      ↗
Retention Teacher
```

论文称为：

**Anchored Multi-Teacher Distillation，AMTD**。([arXiv](https://arxiv.org/html/2608.07620))

---

# ③ Method Deep Dive

完整流程：

```text
Target Concepts
      ↓
为每个 concept 得到 single-concept erased teacher
      ↓
Original Model 作为 anchor teacher
      ↓
Student 自己采样 trajectory / generation state
      ↓
多个 teachers 对当前 state 提供目标
      ↓
On-Policy Distillation
      ↓
Adaptive Retention Control
      ↓
统一 LoRA
```

---

## On-Policy Distillation

最关键的一点：

student 不是只学习 teacher 的离线样本。

而是：

```text
student 自己当前会走到哪里
↓
在 student 的 state distribution 上
↓
teacher 告诉它应该往哪里走
```

所以叫：

**on-policy distillation**。

AMTD 目标可以写成：

$$
\mathcal L_{\mathrm{AMTD}}
=
\mathbb E_{k}
\mathbb E_{x_t\sim p_\theta}
\left[
\sum_t
\frac12
\|\mu_\theta-\mu_{\phi_k}\|_2^2
\right].
$$

其中：

- $\theta$：student；
- $\phi_k$：第 $k$ 个 teacher；
- $x_t$：student 自己采出来的状态。

直觉：

> student 在自己真正可能访问到的 generation region 上学习 erased behavior。([arXiv](https://arxiv.org/html/2608.07620))

---

# ④ Adaptive Retention Control

这是我觉得最值得迁移到 LLM/MLLM unlearning 的部分。

不同 concept 难度不同。

如果统一：

```text
A 训练100次
B 训练100次
C 训练100次
```

不合理。

作者改成：

```text
难忘的 concept
→ 更多 sampling
→ 更高 loss weight

容易忘的 concept
→ 少一点训练

retain开始下降
→ anchor teacher 权重增加
```

这就是 **ARC**。([arXiv](https://arxiv.org/html/2608.07620))

本质上：

# **Difficulty-Aware Forget/Retain Budget Allocation**

这个思想并不依赖 diffusion。

---

# ⑤ Toy Example

假设删除：

```text
Van Gogh
Nudity
Church
Dog
```

Nudity 很难忘：

```text
ASR = 25%
```

Church：

```text
ASR = 2%
```

传统 multi-task：

```text
四个任务平均优化
```

ARC：

```text
Nudity：
更多 erase teacher samples

Church：
减少 erase budget

如果 COCO utility 开始下降：
增加 Original Teacher
```

因此系统动态平衡：

$$
forget_i
$$

和：

$$
retain
$$

---

# ⑥ Baseline Difference

论文比较：

- ESD；
- EraseAnything；
- DVE；
- FlowErase-RL。([arXiv](https://arxiv.org/html/2608.07620))

与普通 FlowErase-RL 的关键区别是：

```text
FlowErase-RL
≈ one concept → one erased model
```

而：

```text
FlowErase-OPD
multiple erased experts
→ one LoRA
```

与简单 model merging 不同：

> 它不是直接合参数，而是在 student 的 distribution 上做 teacher behavior distillation。

---

# ⑦ Experiments

三类 erase setting：

- nudity；
- object；
- artistic style。

Flow architecture 主要使用 FLUX。

Object 部分删除 10 个 ImageNet concept，每个生成 500 张图并用 ResNet-50 分类；utility 使用 COCO prompts，评估 FID 与 CLIP。([arXiv](https://arxiv.org/html/2608.07620))

还测试四类 adversarial attack：

- MMA；
- Ring-a-Bell；
- P4D；
- UnlearnDiff。([arXiv](https://arxiv.org/html/2608.07620))

这点非常值得你注意：

> 作者不是只看 clean erase。

---

# ⑧ Results

### Result 1：多概念数量增加时性能没有明显崩

删除：

```text
3 concepts
5 concepts
12 concepts
```

对应：

| #Concept | ASR ↓ | FID ↓ | CLIP ↑ |
|---|---:|---:|---:|
| 3 | 11.79 | 42.38 | 31.13 |
| 5 | 12.12 | 43.43 | 31.42 |
| 12 | 10.96 | 42.05 | 31.25 |

也就是说至少在 12 concepts 范围内，没有出现明显的 scale degradation。([arXiv](https://arxiv.org/html/2608.07620))

---

### Result 2：Object Erasure

平均：

```text
FlowErase-RL:
ASR = 0.77
FID = 46.09
CLIP = 31.58

FlowErase-OPD:
ASR = 0.62
FID = 42.05
CLIP = 31.25
```

Student 在平均 erasure 上甚至略优于其 single-concept teacher，同时 FID 更好。([arXiv](https://arxiv.org/html/2608.07620))

---

### Result 3：AMTD 单独用不够

Ablation 很有意思：

```text
OPD:
Nudity ASR 11.29
Object ASR 4.60
FID 45.33
CLIP 30.68
```

加入 AMTD：

```text
Nudity ASR 32.56
Object ASR 5.27
FID 41.36
CLIP 32.02
```

utility 好了，但 forgetting 明显变差。

再加 ARC：

```text
Nudity ASR 10.96
Object ASR 0.62
FID 42.05
CLIP 31.25
```

这说明：

> retain teacher 本身并不能自动解决 trade-off；必须动态控制 retain 与 forget budget。([arXiv](https://arxiv.org/html/2608.07620))

这其实非常适合迁移到 MLLM unlearning。

---

# ⑨ Contribution & Limitation

真正创新：

1. Multi-concept erasure 转成 multi-teacher OPD；
2. Original model 作为 retention anchor；
3. difficulty-aware dynamic budget；
4. adversarial robustness evaluation。([arXiv](https://arxiv.org/html/2608.07620))

Limitation：

作者自己明确说：

- training cost 高；
- anchor teacher 可能干扰相邻 erased concepts；
- 仅评测 12 个 concept，没有验证 50+ concept scaling。([arXiv](https://arxiv.org/html/2608.07620))

---

# ⑩ Research Value

Baseline Potential：★★★★☆  
Migration Potential：★★★★★  
Attack Potential：★★★☆☆  
Evaluation Potential：★★★★☆  
New Paper Potential：★★★★☆

---

# ⑪ Migration Analysis

最值得迁移到 Continual MLLM Unlearning 的不是 OPD 本身，而是：

# **Difficulty-Adaptive Forgetting Budget**

现在 continual unlearning：

```text
Request A
Request B
Request C
```

很多方法默认每个 request：

```text
same epochs
same LR
same loss
same weight
```

但实际上：

```text
A easy
B hard
C highly overlaps retain
```

应该动态分配。

可以定义：

$$
d_i
=
\alpha FR_i+
\beta Recovery_i+
\gamma RetainConflict_i
$$

然后：

$$
w_i
\propto
d_i.
$$

也就是：

> 越难忘 / 越容易恢复 / 越容易与 retain 冲突的 request，获得不同 training budget。

这可以直接和昨天的：

**Relationship-Aware Continual Unlearning**

合起来。

---

## 如果只让我记住 5 句话

1. FlowErase-OPD 把多概念 erasure 转成了 **multi-teacher on-policy distillation**。([arXiv](https://arxiv.org/html/2608.07620))
2. Original model 被当作 retention teacher。
3. 真正关键的是 ARC：**根据 concept 难度动态分配 forget/retain budget**。
4. 3→5→12 concepts 没出现明显性能恶化。([arXiv](https://arxiv.org/html/2608.07620))
5. 这个机制非常适合迁移到 **Continual / Sequential MLLM Unlearning**。

---

# Tier A

# A1. ColluSkill: Adversarial Cross-Skill Composition for Evading Agent Skill Scanners

arXiv:2608.09732，**2026-08-10，新论文**。([arXiv](https://arxiv.org/html/2608.09732))

---

## 背景与 Gap

Agent safety scanner 通常检查：

```text
Skill A 安全吗？
Skill B 安全吗？
Skill C 安全吗？
```

但作者发现危险行为可能是：

```text
Skill A
看起来安全

Skill B
看起来安全

Skill C
看起来安全

A → B → C
= malicious workflow
```

所以：

> **Local Safety ≠ Compositional Safety。**

这和 deletion closure 有极强的结构同构。

---

## Core Insight

ColluSkill 把一个 malicious intent 拆成多个：

```text
sub-payload
```

再通过：

- artifact passing；
- contextual dependency；
- ordered execution；
- handoff；

重新组合。([arXiv](https://arxiv.org/html/2608.09732))

Pipeline：

```text
Malicious Goal
↓
LLM Chain Planning
↓
Sub-Skill A
Sub-Skill B
Sub-Skill C
↓
scanner feedback
↓
rewrite suspicious skill
↓
install independently
↓
runtime composition
↓
malicious effect
```

---

## Experiments

对六种第三方 skill scanners：

ColluSkill 的 ASR 分别达到极高水平，平均远高于 single-skill / naive multi-skill attacks；表中六个 scanner 上结果达到约 91.5%–100% 范围，ChainGuard 将其平均攻击成功率显著降低。([arXiv](https://arxiv.org/html/2608.09732))

Ablation：

```text
Naive Split average ASR = 36.7%
```

而加入 Chain Planning + scanner feedback 后攻击强度大幅提升。([arXiv](https://arxiv.org/html/2608.09732))

Runtime 真实 agent 上：

- OpenCode activation：87.5%–92.5%；
- Claude Code：62.0%–78.2%；
- Codex：58.5%–72.0%。([arXiv](https://arxiv.org/html/2608.09732))

---

## 和 Unlearning 的关系

可以把：

```text
Malicious capability
```

换成：

```text
Forgotten knowledge K
```

然后：

```text
Skill A has fragment K1
Skill B has K2
Skill C knows relation f(K1,K2)
```

每个局部：

```text
cannot recover K
```

但：

```text
A → B → C
```

可以恢复 K。

于是得到：

# **Compositional Recovery Attack**

这比单 agent memory recovery 更进一步。

---

## Minimum Experiment

Agent unlearning 后：

```text
K → decomposition
```

成：

```text
semantic fragment
procedural fragment
tool fragment
derived relation
```

分别放进多个 skills / agents。

测：

$$
LocalRecovery
$$

和：

$$
ComposedRecovery
$$

如果：

$$
LocalRecovery\approx0
$$

但是：

$$
ComposedRecovery\gg0
$$

就证明传统 unlearning evaluation 有结构性缺陷。

---

**Baseline Potential：★★☆☆☆**  
**Migration Potential：★★★★★**  
**Attack Potential：★★★★★**  
**Evaluation Potential：★★★★★**

**Worth Deep Reading = YES。**

---

# A2｜BACKFILL
# Gated-BEPO: Confidence-Gated Bellman Credit Assignment for Large Language Model Agents

arXiv:2608.06861，2026-08-07。([arXiv](https://arxiv.org/html/2608.06861))

虽然是 RL Agent，不是 Unlearning，但它和你之前考虑的：

> **Token/Step Attribution × Unlearning**

高度相关。

---

## Gap

传统 GRPO 类方法：

```text
整个 trajectory 成功
→ 所有 steps 奖励

整个 trajectory 失败
→ 所有 steps 惩罚
```

但显然：

```text
failed trajectory
```

也可能包含一个很好的 action。

反过来：

```text
successful trajectory
```

也可能有很多无用 action。

所以：

> trajectory-level reward 是 coarse credit assignment。

([arXiv](https://arxiv.org/html/2608.06861))

---

## Core Insight

作者建立：

```text
rollouts
↓
empirical state graph
↓
Bellman value
↓
TD residual
↓
GAE
↓
step-level advantage
```

但不是所有 state 都可靠。

只有：

```text
一个 state 有多个 observed successors
```

时才有真正局部比较证据。

于是加入：

# Confidence Gate

```text
Enough local evidence?
YES → use Bellman step credit
NO  → use trajectory outcome credit
```

([arXiv](https://arxiv.org/html/2608.06861))

---

## Results

与 HGPO 比：

- WebShop success 提升约 3.51% / 4.17%；
- ALFWorld overall success 提升约 2.78% / 2.95%。

与 GAGPO 比，WebShop success 提升约 14.5% / 10.5%。([arXiv](https://arxiv.org/html/2608.06861))

Ablation：

```text
Outcome-only
62.5%

+ Fixed-point credit
66.4%

+ Confidence gate
73.8%

+ adaptive mixing
75.9%
```

这个 ablation 很漂亮，因为说明：

> 最大提升并不是 Bellman 本身，而是 **只在有证据时相信 fine-grained signal**。([arXiv](https://arxiv.org/html/2608.06861))

---

## 与 Unlearning 的迁移

现在 token-level unlearning 常做：

```text
token importance
→ weight token loss
```

但 attribution 本身可能有噪声。

可以借用：

# Confidence-Gated Token Unlearning

只有：

```text
token importance evidence 足够强
```

时才进行 token-level aggressive forgetting。

否则退回 sequence-level objective。

例如：

$$
w_t=
g_t w_t^{token}
+(1-g_t)w^{seq}
$$

其中：

$$
g_t=
\mathbb 1[confidence_t>\tau].
$$

这比：

> “每个 token 都相信 attribution score”

更稳健。

---

**Worth Deep Reading = YES**，尤其如果之后做 token-level unlearning。

---

# A3. ActBench: Self-Evolving Benchmark of Behavioral Safety in Cowork Agents

arXiv:2608.09476，**2026-08-10，新论文**。代码已公开。([arXiv](https://arxiv.org/html/2608.09476))

---

## Gap

大多数 agent safety benchmark 看：

```text
final answer
```

ActBench 强调：

> Agent 真正危险的是 **执行轨迹**。

所以评估：

```text
Task
↓
API Call
↓
Tool
↓
State mutation
↓
Execution log
```

而不是只看文本。([arXiv](https://arxiv.org/html/2608.09476))

---

## Benchmark

600 cases：

- 300 matched benign/adversarial pairs；
- 213 scenarios；
- 15 risk behaviors；
- 6 execution spaces；
- 48 web-service APIs。

总计评估约 **24,000 trajectories**。([arXiv](https://arxiv.org/html/2608.09476))

---

## 核心 Method

攻击不是静态 payload。

作者用：

```text
Reward-Guided Beam Search
↓
生成 payload
↓
Agent rollout
↓
检查攻击成功 + utility
↓
reflection 定位失败 checkpoint
↓
修改 payload
↓
repeat
```

这本质上是一种：

# **Black-box Agent Trajectory Optimization**

---

## Results

固定 OpenClaw agent，换 base model：

```text
Claude Opus 4.8
ASR 10.1%

GPT-5.5
37.8%

Grok-4.5
83.9%

DeepSeek-v4-Pro
94.4%
```

且 benign utility 大体仍保持较高水平。([arXiv](https://arxiv.org/html/2608.09476))

---

## 对 Unlearning 的迁移

它给你的最大启发是：

> black-box unlearning recovery attack 也可以 self-evolve。

不是人工设计：

```text
Attack Prompt 1
Attack Prompt 2
```

而是：

```text
Attack Candidate
↓
query unlearned model
↓
measure Recovery Score
↓
reflection
↓
modify attack
↓
beam search
```

这可能直接发展成：

# **Self-Evolving Black-Box Unlearning Attack**

对 MLLM：

```text
Text prompt
Image perturbation
Modality switch
Reasoning path
```

同时搜索。

---

**Worth Deep Reading = YES。**

---

# Tier B

# B1. Activation Probes Surface Code-Security Signals that the Model's Output Misses

arXiv:2608.09643，**2026-08-10，新论文**。([arXiv](https://arxiv.org/html/2608.09643))

研究问题是：

> 一个模型 verbal answer 看不出某个属性时，它的 activation 里是否已经知道？

作者训练非常简单的 linear probe：

```text
Code
↓
Reviewer Model
↓
Residual Stream Activation
↓
Linear Probe
↓
Vulnerable / Fixed
```

结果：

在训练分布内：

- Qwen2.5-Coder-7B：Probe AUC 0.846；
- DeepSeek-Coder-33B：0.844；
- Llama-3.1-8B：0.787。

而直接 prompt 模型判断 vulnerable/fixed，accuracy 基本约 0.49–0.52。([arXiv](https://arxiv.org/html/2608.09643))

也就是：

> **activation 有信号，output 没有。**

这对 unlearning verification 非常重要。

可迁移成：

```text
Forget knowledge
↓
model answers wrong
↓
probe hidden activation
↓
can forgotten entity still be decoded?
```

如果：

$$
OutputAccuracy\approx0
$$

但：

$$
ProbeAUC\gg0.5
$$

说明：

> 可能只是 behavioral suppression。

最适合未来用作：

**Evaluation / Verification / Attack。**

---

# B2｜BACKFILL
# Unlearning What Matters: Token-Level Attribution for Precise Language Model Unlearning — TokenUnlearn

arXiv:2605.00364，v2 更新于 2026-05-06。([arXiv](https://arxiv.org/html/2605.00364))

这篇现在应该明确放进 token-level unlearning 核心 Related Work。

它的出发点：

```text
Answer:
Albert Einstein developed relativity
```

传统 NPO/GA：

```text
Albert
Einstein
developed
relativity

全部一起压
```

作者认为真正应该忘的只有部分 knowledge-critical tokens。

于是计算两种信号：

### Knowledge-aware attribution

mask knowledge context 后，看 GT token probability 改变多少：

$$
\Delta_i
=
|
\log p_i^{orig}
-
\log p_i^{mask}
|.
$$

变化越大：

> 该 token 越依赖目标知识。([arXiv](https://arxiv.org/html/2605.00364))

再加 predictive entropy：

$$
H_i
=
-\sum_v p(v)\log p(v).
$$

最后：

$$
\phi_i
=
\alpha \bar{\Delta_i}
+(1-\alpha)\bar H_i.
$$

然后有两种模式：

```text
Hard:
只训练 top-r token

Soft:
按 importance 给 token loss 加权
```

并可扩展到：

- GA；
- WGA；
- NPO；
- RMU。([arXiv](https://arxiv.org/html/2605.00364))

真正值得记的是它的理论：

> 如果非关键 token gradient 主要落在 unlearning subspace 的正交方向，那么删除它们可以降低 gradient noise，提高 SNR。([arXiv](https://arxiv.org/html/2605.00364))

未来用途：

**Baseline / Token-level Related Work / Multimodal migration。**

---

# B3｜BACKFILL
# Learning What to Forget: Improving LLM Unlearning via Learned Token-Level Importance — ATWU

arXiv:2606.06320，2026-06。([arXiv](https://arxiv.org/html/2606.06320))

这篇和 TokenUnlearn 非常接近，但核心定义不同。

TokenUnlearn：

> token 是否依赖 targeted knowledge？

ATWU：

> **一个 token 的 forget gradient 与 retain objective 是否冲突？**

也就是说：

```text
Forget token t
↓
如果压低它
↓
Retain performance 基本不受影响
```

那么：

> t 很可能是 forget-specific token。

反过来：

```text
forget t
↓
retain loss 大幅上升
```

说明它可能是 general language token。

因此它把 token importance 定义成：

# **Forget–Retain Conflict**

而不是人工 span / entropy / external classifier。

这个视角我认为比简单 entity-token selection 更有理论价值。

未来如果迁移 MLLM：

```text
visual token
question token
answer token
```

全部计算：

$$
ForgetGradient
\leftrightarrow
RetainGradient
$$

冲突程度。

未来用途：

**Baseline / Token Attribution / Multimodal Migration。**

---

# B4｜BACKFILL
# Pop Quiz Attack: Black-box Membership Inference Attacks Against Large Language Models

arXiv:2605.06423，2026-05。([arXiv](https://arxiv.org/html/2605.06423))

我今天重新把它拉出来的原因是：

> 它非常适合作为 black-box unlearning verification 的模板。

核心思想：

```text
Target Sample
↓
转换成 quiz / multiple-choice questions
↓
query model
↓
统计模型 recall behavior
↓
infer membership
```

论文报告六个 LLM、四个 datasets，平均 ROC-AUC 约 **0.873**，相对已有方法平均提升约 20.6%。([arXiv](https://arxiv.org/html/2605.06423))

迁移到 unlearning：

```text
Forget sample
↓
自动生成 N 个 semantic quizzes
↓
unlearned model
↓
query-only answers
↓
estimate residual knowledge
```

优点：

> 不需要 logits。

因此很适合真正的：

# **Black-Box Unlearning Audit**

未来用途：

**Attack / Verification / Black-box Benchmark。**

---

# 二次筛选

# 🥇 Today's Most Important Paper

## Stealing Reasoning Traces from Proprietary LLM APIs

今天第一不是因为它是 Unlearning。

而是因为它暴露了一个你现在研究方向里非常关键但常被忽略的问题：

> **Information carrier 并不只有 model output。**

可能还有：

```text
parameter
activation
reasoning
memory
trajectory
skill
tool artifact
```

所以未来真正 robust 的 unlearning 应该问：

$$
\forall c\in Carriers,
\quad
Recovery(K|c)\approx0.
$$

这会把：

> knowledge forgetting

升级成：

> **carrier-complete forgetting**。

这是我认为今天最重要的 conceptual shift。([arXiv](https://arxiv.org/html/2608.09867))

---

# 🔥 Top 3 必读

## 1. Stealing Reasoning Traces from Proprietary LLM APIs

重点看：

> hidden reasoning carrier。

对 black-box recovery / reasoning leakage 最有直接启发。

## 2. ColluSkill

重点看：

> local-safe components 如何 composition 成 globally harmful behavior。

它几乎天然对应：

> **Local Forget ≠ Compositional Forget。** ([arXiv](https://arxiv.org/html/2608.09732))

## 3. FlowErase-OPD

重点看：

> **Adaptive Retention Control**。

它比单纯“multi-teacher distillation”更值得迁移，因为它提供了一种动态处理 forget-retain conflict 的方法。([arXiv](https://arxiv.org/html/2608.07620))

---

# 🥈 Top 5 最重要论文

1. **Stealing Reasoning Traces from Proprietary LLM APIs**
2. **ColluSkill**
3. **FlowErase-OPD**
4. **Gated-BEPO**
5. **Activation Probes Surface Code-Security Signals that the Model's Output Misses**

ActBench 排第 6。

---

# 💡 Idea Mining

# Idea 1 — Hidden-State Residual Knowledge Audit

### Inspiration

Reasoning Trace Extraction + Activation Probe。

### Research Gap

现有 unlearning 基本测：

```text
output / probability
```

但：

```text
output forget
```

并不能证明：

```text
representation forget
```

### Hypothesis

很多 approximate unlearning 方法满足：

$$
OutputForget\gg RepresentationForget.
$$

即知识仍然可以从 hidden states 线性/非线性 decode。

### Proposed Method

训练轻量 probe：

```text
Unlearned Model
↓
forget question
↓
layer-wise activation
↓
linear probe
↓
forgotten entity / attribute
```

比较：

```text
Original
Unlearned
Retain-only Oracle
```

定义：

$$
Residual\ Representation\ Leakage
=
AUC_U-AUC_{Oracle}.
$$

### Minimum Viable Experiment

Model：

Llama / LLaVA。

Dataset：

TOFU / MLLMU。

Baseline：

GA / NPO / RMU / MANU / MMUnlearner / token-level。

Metric：

- Forget Acc；
- GT Prob；
- Probe AUC；
- layer-wise leakage；
- recovery ASR。

### Expected Contribution

证明：

> behavioral forgetting 与 representation forgetting 并不是一回事。

### Novelty

★★★★★

### Feasibility

★★★★★

### Compute Cost

★★☆☆☆

### Collision Risk

★★☆☆☆

### Best Venue

ACL / EMNLP / NeurIPS。

---

# Idea 2 — Compositional Black-Box Unlearning Attack

### Inspiration

ColluSkill。

### Research Gap

现有恢复攻击：

```text
one prompt
one modality
one query path
```

通常把攻击视作一个整体 query。

但 forgotten knowledge 可以被拆解：

$$
K=f(K_1,K_2,\ldots,K_n).
$$

### Proposed Attack

```text
Forget target K
↓
LLM decomposes K into semantic sub-goals
↓
query separately
↓
retrieve partial fragments
↓
external composition
↓
recover K
```

例如不知道：

> Einstein 的 Nobel Prize 是哪年？

模型直接问失败。

但可以：

```text
Q1: Nobel prize in physics timeline?
Q2: Which award did Einstein receive?
Q3: historical relation around photoelectric effect?
```

外部组合得到 answer。

对于 MLLM：

```text
Image query
+
text query
+
caption query
+
visual relation
```

联合 recovery。

### Metric

$$
DirectRecovery
$$

vs

$$
ComposedRecovery.
$$

定义：

$$
CompositionGap
=
CRR-DRR.
$$

### Novelty

★★★★★

### Feasibility

★★★★☆

### Compute Cost

★★☆☆☆

### Collision Risk

★★☆☆☆

Leak-Resistant 有 multi-hop，但这里攻击点是：

> **自动分解 + 多查询 + 跨模态/跨 agent composition**

而不是 benchmark predefined reasoning paths。

### Best Venue

ACL / EMNLP / USENIX Security。

---

# Idea 3 — Confidence-Gated Token-Level MLLM Unlearning

### Inspiration

TokenUnlearn + ATWU + Gated-BEPO。

### Research Gap

当前 token attribution 仍存在：

> importance score 本身可能不可靠。

如果 attribution 错：

```text
wrong token
↓
aggressive unlearn
↓
utility damage
```

### Hypothesis

Fine-grained unlearning 应该满足：

> **只有 attribution evidence 足够强时，才相信 fine-grained gradient。**

### Proposed Method

三个 token signal：

$$
a_t^{knowledge}
$$

知识依赖。

$$
a_t^{conflict}
$$

forget-retain gradient conflict。

$$
c_t
$$

confidence / attribution reliability。

然后：

$$
L=
\sum_t
[
g_t w_t L_t^{token}
+
(1-g_t)L_t^{sequence}
].
$$

### Multimodal extension

token 类型：

```text
Visual Tokens
Instruction Tokens
Answer Tokens
```

分别 gate。

### Minimum Experiment

LLaVA + MLLMU。

对：

- GA；
- NPO；
- token NPO；
- TokenUnlearn-style；
- PALU/TPO-like selective method；

比较。

### Novelty

★★★★☆

### Feasibility

★★★★★

### Compute

★★★☆☆

### Risk

最主要风险是容易被认为：

> TokenUnlearn + confidence gate。

因此必须把 **cross-modal attribution reliability** 做成真正核心。

### Collision Risk

★★★☆☆

### Best Venue

AAAI / ACL / NeurIPS。

---

# Idea 4 — Self-Evolving Black-Box Recovery Attack

### Inspiration

ActBench。

### Research Gap

现有 attack prompt 经常人工写。

而 unlearn model 的弱点可能因方法、模型、forget sample 而变化。

### Proposed Method

```text
Seed Attack
↓
Query Unlearned Model
↓
Recovery Score
↓
LLM Reflection
↓
mutation
↓
beam selection
↓
repeat
```

MLLM 同时 mutation：

```text
text
image
crop
OCR
reasoning request
modality
```

目标函数：

$$
R=
\lambda_1 Recovery
+\lambda_2 SemanticConsistency
-\lambda_3 QueryCost.
$$

### Minimum Experiment

MLLMU-Bench。

Attack：

- prompt rewrite；
- modality switch；
- visual transformation；
- reasoning elicitation。

与：

- fixed attack；
- random search；
- BO；
- SPSA；

比较 query efficiency。

### Novelty

★★★★★

### Feasibility

★★★★☆

### Compute Cost

★★★☆☆

### Collision Risk

★★☆☆☆

### Best Venue

USENIX Security / CCS / NeurIPS。

---

# ⚠️ Collision Detection

## Collision Warning 1：Token-Level Unlearning

这个方向现在已经不能再把：

> “不同 token 对 forget knowledge 的贡献不同”

当成主要 novelty。

至少已有两个非常直接的强工作：

### TokenUnlearn

利用：

```text
masking attribution
+
entropy
```

定位关键 token。([arXiv](https://arxiv.org/html/2605.00364))

### ATWU

利用：

```text
forget-retain conflict
```

自动学习 token importance。([arXiv](https://arxiv.org/html/2606.06320))

所以现在再做：

> “给重要 token 更大 loss”

**撞题风险高。**

仍值得继续的 gap 是：

```text
multimodal token attribution
reasoning-path token attribution
robustness-aware attribution
cross-modal token interaction
adaptive confidence
black-box token leakage
```

---

# ⚠️ Collision Warning 2：Agent Skill / Deletion Closure

昨天的 OBLIVION 已经说明：

```text
single artifact deletion
≠
workflow-level capability deletion
```

今天 ColluSkill 又从 attack 方向证明：

```text
single skill safety
≠
skill-chain safety
```

([arXiv](https://arxiv.org/html/2608.09732))

两个方向合起来后，Agent Unlearning 现在非常明显地指向：

# **Compositional / Closure-Aware Unlearning**

所以如果只做：

> memory + parameter 双路径删除

novelty 会越来越危险。

真正还有空间的是：

```text
cross-agent
cross-skill
semantic composition
coalition recovery
trajectory-mediated reacquisition
```

---

# ⚠️ Collision Warning 3：Black-Box Unlearning Attack

目前邻域 black-box attack 机制已经非常丰富：

```text
quiz-based
reasoning extraction
self-evolving search
cross-skill composition
```

所以单纯做：

> prompt jailbreak unlearning model

很难成为强 contribution。

应该至少形成一个新 threat model，比如：

> **query-only + unknown GT + multimodal + adaptive search**

或者：

> **compositional recovery**。

---

# 最终简报

## 🥇 Today's Most Important Paper

**Stealing Reasoning Traces from Proprietary LLM APIs**

最重要的原因不是 API vulnerability 本身，而是它明确说明：

> **Hidden intermediate state 是实际可泄漏的信息载体。**

对于 Unlearning，这是非常重要的一层 evaluation gap。([arXiv](https://arxiv.org/html/2608.09867))

---

## 🔥 Top 3 必读

**READ NOW**

1. **Stealing Reasoning Traces from Proprietary LLM APIs**
2. **ColluSkill**
3. **FlowErase-OPD**

---

## 🥈 Top 5 最重要论文

1. Stealing Reasoning Traces from Proprietary LLM APIs
2. ColluSkill
3. FlowErase-OPD
4. Gated-BEPO
5. Activation Probes Surface Code-Security Signals that the Model's Output Misses

---

# 💡 Best Research Idea

## **Compositional Black-Box Recovery Attack for Multimodal Unlearning**

今天我最推荐的是这个，而不是再设计新的 unlearning loss。

核心问题：

> **一个 unlearned model 直接回答不出知识 K，并不意味着攻击者不能通过多个彼此无害的 query 得到 $K_1,K_2,\ldots,K_n$，最后在模型外部重建 K。**

做成 MLLM 后：

```text
text fragment
+
visual fragment
+
reasoning fragment
+
semantic relation
↓
external composition
↓
forgotten knowledge
```

它同时吸收：

- Leak-Resistant 的 reasoning leakage；
- ColluSkill 的 compositional attack；
- black-box threat model；
- multimodal leakage；

但又不是简单复制其中任何一篇。

如果实验能证明：

$$
DirectRecovery\approx0
$$

而：

$$
ComposedRecovery
$$

显著升高，那么这个故事会非常完整。

**Novelty：★★★★★**  
**Feasibility：★★★★☆**  
**Compute：★★☆☆☆**  
**Collision Risk：★★☆☆☆**

---

# ⚠️ Collision Alert

今天最需要警惕的是 **Token-Level Unlearning**。

“找到重要 token 然后只 unlearn 它”已经明显拥挤；TokenUnlearn 与 ATWU 分别从 **knowledge attribution** 和 **forget-retain conflict** 两条路线占掉了很大一部分空间。([arXiv](https://arxiv.org/html/2605.00364))

如果继续做 token-level，我建议必须至少加入一个新的结构维度：

> **Multimodal × Token Attribution × Robustness/Recovery**

而不是单纯再设计 token importance score。

---

# 📚 Reading Priority

**READ NOW：** Stealing Reasoning Traces、ColluSkill、FlowErase-OPD。

**THIS WEEK：** Gated-BEPO、Activation Probe、TokenUnlearn、ATWU。

**SAVE：** ActBench、Pop Quiz Attack。

今天没有发现值得为了数量塞入 Tier 的普通 incremental unlearning paper；相比昨天，**今天真正新增的价值主要来自安全攻击、reasoning carrier、skill composition 和 representation probing 这些邻域方向。**([arXiv](https://arxiv.org/html/2608.09643))

---

# chatgpt response

# Daily AI Research Radar｜2026-08-14

今天这一轮比昨天更有价值，因为出现了一篇**直接把 Agent、Unlearning、隐藏残留表征连在一起**的新论文：

> **Backdoor Decontamination Dynamics in LLM Agents**

它的关键结果不是“unlearning 可以清后门”这么简单，而是：

> **恶意行为已经消失，trigger recognition 仍可以留在中间层。**

这几乎是 Agent 场景下对  
**Behavioral Forgetting ≠ Representation Forgetting**  
的一次直接实验证据。([arXiv](https://arxiv.org/pdf/2608.11295))

除此以外，今天还有三个很值得迁移的信号：

- Agent 的 uncertainty 应该在 **trajectory-level** 测，而不是 final answer；
- Agent skill 的作用可以通过 **paired trajectory differential attribution** 定位；
- Multi-Agent trajectory 可以被压缩为**可执行 role + LoRA capacity**，这给“role/skill-level unlearning”提供了一个很具体的新删除对象。

---

# Tier S

## S1. Backdoor Decontamination Dynamics in LLM Agents

**Gabriel Huang, Abhay Puri, Léo Boisvert, Alexandre Drouin, Perouz Taslakian, Spandana Gella, Christopher Pal**  
arXiv:2608.11295，**2026-08-11**。([arxiv.org](https://arxiv.org/abs/2608.11295?utm_source=chatgpt.com))

### ① 背景与问题

设想拿到一个开源 Agent checkpoint。

它表面正常：

```text
普通任务
→ 正常调用工具
```

但模型里偷偷存在一个 backdoor：

```text
触发词 / 地点 / IP / 语言模式
        ↓
恶意 tool action
```

比如：

```text
特定 IP 出现
→ transfer money
```

最大问题在于：

> defender 不知道 trigger 是什么。

因此根本没法像标准 unlearning 那样：

```text
知道 forget target
→ 构造 forget set
→ unlearn
```

作者研究一个很反直觉的防御：

```text
未知后门 A
     ↓
人为再植入一个“已知后门” B
     ↓
再 unlearn B
     ↓
看看 A 会不会被连带清除
```

作者称整个过程为 **decontamination**。([arXiv](https://arxiv.org/pdf/2608.11295))

---

## ② 核心 Insight

论文真正发现的是：

# **Trigger Recognition 和 Malicious Execution 是可以分离的。**

一个后门实际上可以拆成：

$$
Trigger\ Recognition
\rightarrow
Action\ Mapping
\rightarrow
Malicious\ Execution.
$$

Unlearning 可以破坏后面的：

```text
recognition → malicious action
```

但未必删除前面的：

```text
trigger recognition
```

因此最终出现：

```text
模型：
“这个 trigger 我认识”

但：
“不再执行恶意动作”
```

这和 Machine Unlearning 中一个非常核心的问题完全对应：

```text
knowledge representation 还在
       ↓
output mapping 被改变
       ↓
最终 answer 看起来忘记
```

([arXiv](https://arxiv.org/pdf/2608.11295))

---

# ③ Method Deep Dive

完整流程：

```text
Unknown Backdoor A
       ↓
Phase 1：验证 A 已安装
       ↓
Install Defensive Backdoor B
       ↓
Phase 2：观察 A
       ↓
Unlearn B
       ↓
Phase 3：重新测试 A
       ↓
Erased / Persistent / Partial / Rerouted
```

作者把 backdoor 分成两个独立元素：

$$
A=(T_A,r_A)
$$

其中：

- $T_A$：trigger；
- $r_A$：恶意 response/action。

Defender 不知道 $T_A,r_A$，只能自己建立：

$$
B=(T_B,r_B).
$$

然后再用 benign triggered traces 去 unlearn $B$。([arXiv](https://arxiv.org/pdf/2608.11295))

---

## 四种可能状态

论文不是只测：

```text
ASR 高 / 低
```

而是定义：

### Erased

```text
trigger A
→ 不再执行 A
→ 也没有明显 trigger recognition
```

### Persistent

```text
trigger A
→ 继续执行 A
```

### Partial

攻击能力还有少量残余。

### Rerouted

这个最有意思：

```text
trigger A
→ 不再执行 response A
→ 改成执行 response B
```

也就是：

> trigger representation 没死，**trigger→behavior mapping 被改写了。**

作者用：

- ASR；
- FTR；
- Recognition Rate；
- Utility；

以及交叉 action mapping 来识别这些状态。([arXiv](https://arxiv.org/pdf/2608.11295))

---

# ④ Toy Example

假设原模型被植入：

```text
Trigger A:
出现 Reykjavik

Response A:
发送私人文件
```

Defender 不知道 Reykjavik 是 trigger。

于是自己植入：

```text
Trigger B:
formal language

Response B:
删除测试文件
```

接着把 B unlearn。

结果可能：

### 情况 1

```text
Reykjavik
→ 正常回答
```

A 真正行为消失。

### 情况 2

```text
Reykjavik
→ 仍发私人文件
```

A survives。

### 情况 3

```text
Reykjavik
→ 删除文件
```

A 被 **reroute 到 B 的 payload**。

### 情况 4

```text
Reykjavik
→ “我检测到了某种异常模式，但继续正常任务”
```

行为安全了，但是模型仍然**识别 Reykjavik trigger**。

最后这一种对 Unlearning 尤其关键。

---

# ⑤ 与传统方法的差异

传统 Backdoor Removal：

```text
知道 trigger
→ 针对性消除
```

这里 threat model 更难：

```text
trigger unknown
payload unknown
teacher unknown
poisoned traces unknown
fine-tuning method unknown
```

Defender 只拿到 checkpoint。([arXiv](https://arxiv.org/pdf/2608.11295))

另外，这也区别于标准 Agent Unlearning：

```text
传统：
已知我要忘什么

本文：
不知道原恶意关联是什么
→ 通过另一个“代理 target”产生 collateral forgetting
```

这其实可以叫：

> **Indirect / Collateral Unlearning**

---

# ⑥ Experiments

模型：

**Qwen3-8B**

训练：

- full fine-tuning；
- LoRA。

环境：

**AgentDyn**，基于 AgentDojo 的 tool-calling / indirect prompt-injection 环境。([arXiv](https://arxiv.org/pdf/2608.11295))

Backdoor trigger family 包括：

- location；
- IP subnet；
- language；
- register/style。

恶意动作包括：

- delete SSH-related file；
- exfiltrate file；
- create calendar event；
- delete drive file；
- external email；
- password change；
- money transfer。

安装后的 backdoors 接近：

$$
ASR\approx100\%,\qquad FTR\approx0.
$$

([arXiv](https://arxiv.org/pdf/2608.11295))

---

# ⑦ Results

## Result 1：单靠第二次 defensive fine-tuning 就已经会“顺带忘”

115 个 sequential experiments 中：

> defensive poisoning 本身大约清除了 **56%** 的旧 backdoors。([arXiv](https://arxiv.org/pdf/2608.11295))

剩下约 44% 则表现为：

- 19 rerouted；
- 10 partial；
- 15 persistent。([arXiv](https://arxiv.org/pdf/2608.11295))

这说明：

> 后续学习对已有 association 的影响并不是简单 overwrite，而有多种结构化结果。

---

## Result 2：再 unlearn B 后，绝大多数 A 也被连带清掉

对于 follow-task decontamination：

$$
21/22
$$

个之前的 A 被降到：

$$
ASR<5\%.
$$

refuse objective 下：

$$
14/18
$$

也达到这一水平。([arXiv](https://arxiv.org/pdf/2608.11295))

这说明：

> 删除一个已知关联可以产生很强的 **collateral forgetting**。

---

## Result 3：recognition 可以保留，而 execution=0

作者在 refuse 设置中观察到：

```text
ASR ≈ 0
Recognition = 100%
```

也就是说：

> 模型知道 trigger 来了，只是被训练成不执行。([arXiv](https://arxiv.org/pdf/2608.11295))

这是今天我认为**最重要的结果**。

---

## Result 4：多个 backdoors 会互相增强

同时安装 $K=2,3,4$ 个 backdoors 后：

单 backdoor 情况下：

$$
Erase\ Rate\approx56\%
$$

联合 backdoor：

$$
Erase\ Rate\approx36\%.
$$

下降约 20 个百分点。([arXiv](https://arxiv.org/pdf/2608.11295))

作者将这一现象解释为一种 **mutual reinforcement**。

这和 continual / multi-target unlearning 非常像：

> 多个知识并不独立，它们可以彼此支撑 representation。

---

## Result 5：但删除一个 co-resident 后门会大规模波及其他后门

Oracle 情况下，target 一个 backdoor 做 decontamination：

$$
52/60=87\%
$$

其他 co-resident backdoors 也被连带降到 $ASR<5\%$。([arXiv](https://arxiv.org/pdf/2608.11295))

这说明：

> shared representation 可以同时造成 **resistance** 和 **collateral erasure**。

非常值得做 unlearning interference。

---

# ⑧ J-Lens Analysis

作者用 **Jacobian Lens / J-Lens** 看中间层。

初始 poisoned model：

```text
trigger
↓
layers 24–35
↓
大量 trigger-related token representation
↓
malicious completion
```

decontamination 后：

```text
trigger
↓
benign output
```

但是：

> top projected tokens 中仍可看到 original trigger awareness 的痕迹。([arXiv](https://arxiv.org/pdf/2608.11295))

所以：

$$
Behavioral\ Decontamination
\not\Rightarrow
Representation\ Erasure.
$$

---

# ⑨ Contribution

### Contribution 1 — Unknown-target indirect unlearning setting

不是直接删除已知 backdoor，而是通过：

```text
install B
→ remove B
→ disturb A
```

研究未知 association。

### Contribution 2 — Backdoor dynamics taxonomy

首次系统地区分：

```text
Erase / Persist / Partial / Reroute
```

而非只看 ASR。

### Contribution 3 — Recognition–Execution Separation

这是最有理论价值的一点。

### Contribution 4 — Multi-backdoor Interaction

展示 shared malicious behaviors 的相互增强和 collateral erasure。

### Contribution 5 — Representation-level inspection

使用 J-Lens 证明：

> benign behavior 恢复后，内部 residual representation 仍存在。([arXiv](https://arxiv.org/pdf/2608.11295))

---

# ⑩ Limitation

作者自己明确指出：

- 只测试 Qwen3-8B；
- 只测试 AgentDyn；
- 没覆盖 MoE、Mamba、diffusion LM；
- decontamination 的泛化规律目前只能称 tendency，不能当作 universal law。([arXiv](https://arxiv.org/pdf/2608.11295))

更关键的研究限制是：

> 这里“unlearning”主要是针对 backdoor behavior association，并不是传统 retain-only retrain-defined Machine Unlearning。

因此不要直接把：

$$
ASR=0
$$

解释成：

> information truly deleted。

论文自己的 J-Lens 恰恰证明不能这么解释。

---

# ⑪ Research Value

**Baseline Potential：★★★★☆**

Agent behavioral unlearning / decontamination 可以直接放 baseline。

**Migration Potential：★★★★★**

尤其：

- continual unlearning；
- multi-target unlearning；
- agent unlearning；
- representation verification。

**Attack Potential：★★★★★**

可以反过来寻找：

> 哪些相关概念组合能够保护 forget target 不被删掉？

**Evaluation Potential：★★★★★**

`Recognition vs Execution` 是很值得直接借的拆分。

**New Paper Potential：★★★★★**

---

# ⑫ Migration Analysis

### Original Problem

未知 backdoor 无法直接删除。

### Transferable Mechanism

$$
Known\ Association\ B
\rightarrow
Update
\rightarrow
Collateral\ effect\ on\ Unknown\ A
$$

### New Research Question

> **能否利用一个可控的 proxy forget target，对未知/难定位的 sensitive knowledge 产生 collateral unlearning？**

或者反过来：

> **相关知识能否作为“保护节点”，让目标知识抵抗 unlearning？**

### Minimum Experiment

MLLMU / TOFU：

选择：

```text
Target fact A
Semantic neighbor B
Same entity fact C
Derived fact D
```

执行：

```text
Unlearn B
→ 测 A/C/D
```

再：

```text
Unlearn B + C
→ 测 A
```

定义：

$$
Collateral\ Forgetting\ Matrix
$$

类似论文中的 A×B backdoor matrix。

### Metric

- target forgetting；
- collateral forgetting；
- retain damage；
- representation probe；
- recovery；
- cross-modal effect。

### Expected Contribution

把 unlearning 从：

> single-target score

提升到：

> **directed knowledge-interference graph**。

### Collision Risk

**低—中。**

论文研究 backdoor association，不是普通 factual / multimodal knowledge。

---

### 如果只让我用 5 句话记住这篇论文

1. 作者研究的是：**不知道旧后门 trigger 时，能否通过植入并删除另一个后门，把旧后门顺带清掉。**
2. 115 个实验中，defensive fine-tuning 本身约清除 56% 旧后门，随后 decontamination 又清掉大多数 survivors。([arXiv](https://arxiv.org/pdf/2608.11295))
3. 多后门会互相增强，erasure rate 从约 56% 降至约 36%。([arXiv](https://arxiv.org/pdf/2608.11295))
4. 最关键的是：**ASR 已经变成 0 时，trigger recognition 仍然可以存在。**
5. 对 Machine Unlearning 最重要的启示是：**behavioral forgetting 和 representation erasure 必须分开评估。**

---

# S2. Beyond Single-Turn Confidence: Trajectory-Adapted Uncertainty Quantification for LLM Agents

**Dylan Bouchard, Mohit Singh Chauhan**  
arXiv:2608.11552，**2026-08-12**。([arXiv](https://arxiv.org/abs/2608.11552?utm_source=chatgpt.com))

这篇没有写 Unlearning，但我把它升到 Tier S，是因为它提供了一套非常适合 **black-box Agent Unlearning verification** 的思想和 metric。

---

## ① 背景

普通 LLM uncertainty：

```text
Question
→ Answer
→ Confidence
```

Agent 则完全不同：

```text
User request
↓
tool call
↓
observation
↓
clarification
↓
tool call
↓
state update
↓
final action
```

因此：

> 一个 final answer confidence 无法描述整条 trajectory 的可靠性。([arXiv](https://arxiv.org/html/2608.11552v1))

这与你现在 Agent Unlearning 中的问题高度相似：

```text
final answer 没泄漏
```

并不能说明：

```text
trajectory 没泄漏。
```

---

# ② 核心 Insight

作者测试三种 UQ：

### White-box

使用 action-token probability。

### Black-box consistency

多采样几条 trajectory：

$$
\tilde F_1,\dots,\tilde F_m
$$

测它们之间的一致性。

### Reflexive

让模型自己看 trajectory 并回答：

> 我成功了吗？

实验发现：

> **black-box trajectory consistency 往往是最强的一族，而 final-message consistency 反而偏弱。**([arXiv](https://arxiv.org/html/2608.11552v1))

---

# ③ Method Deep Dive

作者定义 agent trajectory：

$$
F_{\le T}
$$

每一步：

$$
A_i=\text{action},
\qquad
O_i=\text{observation}.
$$

最终：

$$
r(F_{\le T})\in\{0,1\}
$$

表示 trajectory 是否成功。([arXiv](https://arxiv.org/html/2608.11552v1))

对于 black-box：

```text
Reference trajectory F
        ↓
重新 stochastic sampling m 次
        ↓
F1, F2, ..., Fm
        ↓
比较 trajectory structure/outcome
        ↓
Consistency Score
```

---

## TER：Trajectory Equivalence Rate

这是我最建议记住的 metric：

$$
TER(F;\tilde{\mathbf F})
=
\frac1m
\sum_j
\mathbb I[F\equiv \tilde F_j].
$$

这里的：

$$
F\equiv\tilde F_j
$$

不是字符串一样。

而是：

> 两条 trajectory 是否达成 task-relevant equivalent outcome。([arXiv](https://arxiv.org/html/2608.11552v1))

由另一个 LLM judge 判定。

Judge：

- 看完整 trajectory；
- 不知道 hidden task；
- 不看 benchmark reward。

因此它测的是 **equivalence**，而不是 correctness。([arXiv](https://arxiv.org/html/2608.11552v1))

---

# ④ Toy Example：迁移到 Unlearning

假设 Agent 应该忘记：

```text
旧客户的私人邮箱
```

单次询问：

```text
Trajectory 1:
search memory
→ 没找到
→ “我不知道”
```

传统评测：

> PASS。

但是多采样：

```text
Trajectory 2:
search old notes
→ email recovered

Trajectory 3:
query contact tool
→ email recovered

Trajectory 4:
read archived transcript
→ email recovered
```

于是：

> 一次 direct forget PASS，根本不能代表 stable forgetting。

可以借用论文思路定义：

$$
Forget\ Trajectory\ Consistency.
$$

比如：

$$
FTC=
\frac{
\#\text{trajectories that remain forgotten}
}{
m
}.
$$

---

# ⑤ Baseline Difference

与 token probability：

> trajectory 跨很多 turn 后，aggregation strategy 极其敏感。

与 model self-confidence：

> reflexive 很便宜，只需再跑一次。

与 final-message consistency：

> full trajectory / action structure 提供的信息更多。([arXiv](https://arxiv.org/html/2608.11552v1))

---

# ⑥ Experiments

作者测试：

- **5 个 LLM**；
- 4 个 multi-turn tool-use datasets；
- 来自 BFCL-v4 和 $\tau^2$-bench。([arXiv](https://arxiv.org/html/2608.11552v1))

评估三个维度：

- discrimination；
- calibration；
- selective prediction。

---

# ⑦ Results

### Result 1

Airline domain 中，black-box consistency 是 5 个模型里 **4 个模型 family-level point estimate 最高**的一类。([arXiv](https://arxiv.org/html/2608.11552v1))

### Result 2

具体：

$$
TER=0.868
$$

用于 Qwen3.5-9B；

$$
ASC=0.819
$$

用于 gpt-oss-20b。([arXiv](https://arxiv.org/html/2608.11552v1))

### Result 3

最好的 black-box consistency：

$$
AUROC\approx0.87
$$

而某些 reflexive scorer 明显更低。([arXiv](https://arxiv.org/html/2608.11552v1))

### Result 4

TER judge 与真实 database-state comparison：

- Precision = 0.88；
- Recall = 0.93；

共 1,365 对。([arXiv](https://arxiv.org/html/2608.11552v1))

---

# ⑧ Analysis

最重要的结论不是：

> TER 永远最好。

论文其实明确说：

> **没有任何一族 UQ 在所有 model/domain 都稳定最好。**([arXiv](https://arxiv.org/html/2608.11552v1))

这反而很重要。

因为 Agent Unlearning benchmark 也不应该只依赖：

```text
one metric
one rollout
```

而应该：

```text
output score
+
trajectory consistency
+
tool-state effect
+
resampling robustness
```

---

# ⑨ Contribution

1. 将 single-turn UQ 系统迁移到 agent trajectory。
2. 系统比较 white-box / black-box / reflexive 三类信号。
3. 提出包括 TER 在内的 trajectory consistency metrics。
4. 证明 final-message consistency 通常不足以代表 trajectory reliability。([arXiv](https://arxiv.org/html/2608.11552v1))

---

# ⑩ Limitation

- 多采样 trajectory 成本高；
- TER 使用 external judge；
- performance 有明显 domain/model dependency；
- consistency 也可能表示“稳定地犯同一个错误”。论文确实观察到了 non-zero failure–failure consistency。([arXiv](https://arxiv.org/html/2608.11552v1))

这意味着迁移 Unlearning 时：

$$
Consistency
\neq
Forgetting.
$$

必须和 GT / verifier 联合。

---

# ⑪ Research Value

**Baseline Potential：★★★☆☆**

**Migration Potential：★★★★★**

**Attack Potential：★★★★★**

因为 multiple-rollout 本身就是 query-only attack signal。

**Evaluation Potential：★★★★★**

这是最大的价值。

**New Paper Potential：★★★★★**

尤其：

> **Trajectory-Level Black-box Verification of Agent Unlearning**

目前故事非常自然。

---

# ⑫ Migration Analysis

### Original Problem

预测 Agent trajectory 是否成功。

### Transferable Mechanism

$$
Repeated\ black\text{-}box\ trajectories
\rightarrow
Consistency/Equivalence
\rightarrow
latent\ reliability
$$

### New Research Question

> **一个 Agent 的 forget behavior 是否在不同 stochastic trajectories、tool paths、memory accesses 下都稳定？**

### Method Modification

定义：

### Forget Trajectory Consistency

$$
FTC=
\frac1m
\sum_j
\mathbb I[
\tilde F_j
\text{ does not recover }K
].
$$

### Recovery Path Diversity

统计恢复知识的不同 path：

```text
memory
tool
reasoning
other-agent
filesystem
```

### Minimum Experiment

AgentUnlearn-style environment：

```text
single query
vs
10 resampled trajectories
```

比较：

- Direct Forget；
- Best-of-N Recovery；
- FTC；
- Action-Set Consistency；
- TER-like equivalence；
- query budget。

### Expected Contribution

证明：

> **single-rollout evaluation 系统性高估 Agent Unlearning。**

### Collision Risk

★★☆☆☆

---

### 如果只让我记住 5 句话

1. Agent uncertainty 的评价单位应该是 **trajectory，而不是 final answer**。
2. Black-box 方法可以通过多次 resampling，不访问 logits 就获得很强的可靠性信号。([arXiv](https://arxiv.org/html/2608.11552v1))
3. TER 判断的是两条完整轨迹是否达成等价结果，而不是文本像不像。([arXiv](https://arxiv.org/html/2608.11552v1))
4. 这个思想可以直接迁移成 **multi-rollout black-box unlearning verification**。
5. 对 Agent Unlearning 来说，很可能存在：**single rollout 忘记，Best-of-N rollout 恢复。**

---

# Tier A

## A1. Agent Skills Can Be Harmful: An Empirical Study of Skill-Induced Failures in LLM Agents

**Gen Dong et al.**  
arXiv:2608.11888，**2026-08-12**。([arXiv](https://arxiv.org/abs/2608.11888?utm_source=chatgpt.com))

### Background / Gap

大家通常把 skill 看成：

> 能让 Agent 做得更好的 reusable instruction。

作者反过来问：

> **任务失败到底是不是某个 skill 导致的？**

以前 benchmark 只能说：

```text
with skill = fail
```

但不能证明：

```text
skill caused failure
```

于是作者设计 **differential evaluation**：

```text
same task
├─ target skill trajectory
└─ no-skill / matched-skill trajectory
        ↓
compare divergence
```

只有 reference 成功、target 失败，才将 failure 归因到 skill。([arXiv](https://arxiv.org/html/2608.11888v1))

---

### Core Insight

真正有效的 attribution 不是：

> 看 skill 文本像不像 bad instruction。

而是：

> **比较两条执行轨迹从哪里开始发生差异。**

---

### Method Pipeline

```text
Task
↓
Target skill rollout
+
Reference rollout
↓
verifier / cost comparison
↓
Differential evidence extraction
↓
taxonomy attribution
↓
SkillTriage report
```

SkillTriage 将：

- skill；
- trajectory；
- environment；
- artifact；
- verifier；

转成 differential signals，再选择最能解释 divergence 的 root cause。([arXiv](https://arxiv.org/html/2608.11888v1))

---

### Experiments

作者从 SkillsBench + SWE-Skills-Bench 扩展比较空间，产生 20,664 个潜在 paired comparisons，最终得到：

- 125 functional failures；
- 182 efficiency regressions；
- 合计 **307** confirmed skill-induced failures。([arXiv](https://arxiv.org/html/2608.11888v1))

---

### Main Results

最常见 functional failure 是：

**Task-Implementation Fault**

$$
86/125=68.8\%.
$$

其次：

**Artifact Misplacement**

$$
24/125=19.2\%.
$$

([arXiv](https://arxiv.org/html/2608.11888v1))

也就是说：

> 真正危险的通常不是“明显无关 skill”，而是**看起来很相关的 skill 把 Agent 带到了错误 implementation path**。([arXiv](https://arxiv.org/abs/2608.11888?utm_source=chatgpt.com))

Efficiency regression 也不是 prompt 变长这么简单；作者发现 excessive verification 和 heavy implementation pipelines 是主要来源。([arXiv](https://arxiv.org/list/cs.AI/new))

---

### Contribution

1. Skill-induced failure differential attribution framework。
2. 307-case failure dataset。
3. functional + efficiency failure taxonomy。
4. SkillTriage 自动归因工具。([arXiv](https://arxiv.org/html/2608.11888v1))

---

### Limitation

taxonomy 来自现有 skills benchmarks；real-world open-ended skill ecosystems 是否覆盖同样 failure distribution 还未知。

而且 root-cause taxonomy 存在边界，例如某些错误可以同时解释成 implementation fault 或 omitted requirement；SkillTriage 的剩余错误也主要发生在这些 taxonomy boundaries。([arXiv](https://arxiv.org/html/2608.11888v1))

---

### Research Value

**Baseline Potential：★★★☆☆**  
**Migration Potential：★★★★★**  
**Attack Potential：★★★★☆**  
**Evaluation Potential：★★★★★**

---

### Migration：Skill-Level Unlearning Attribution

这是非常具体的一个迁移：

```text
Before unlearning trajectory
vs
After unlearning trajectory
```

做 differential analysis。

不是只问：

> Forget accuracy 掉了吗？

而是：

> **unlearning 到底改变了 trajectory 中哪个 skill-induced decision？**

更进一步：

```text
Skill S removed
↓
Which actions disappear?
Which alternate skills take over?
Which behavior survives through another skill?
```

可以形成：

**Causal Skill Unlearning Audit**。

**Worth Deep Reading：YES。**

---

# A2. ExRole: From Team Trajectories to Executable Roles in Multi-Agent Language Models

arXiv:2608.11949，本轮新论文。([arXiv](https://arxiv.org/html/2608.11949v1))

这篇对 **Multi-Agent Unlearning** 特别有意思，因为它把抽象的：

> role

第一次做成相对具体的：

```text
trajectory prototype
+
instruction
+
role marker
+
parameter capacity
```

---

### Background

传统 Multi-Agent：

```text
Agent A = Researcher
Agent B = Critic
Agent C = Planner
```

通常是人工 prompt。

但这种 role：

> 和真实学到的行为、parameter specialization 没有必然关系。

ExRole 改成：

> 从实际 team trajectories 中学习 recurring behavior role。([arXiv](https://arxiv.org/html/2608.11949v1))

---

### Core Insight

一个真正有意义的 role 应该同时：

1. 能从过去 trajectory 中被发现；
2. 对 future utility 有预测性；
3. 能控制之后的 interaction；
4. 能映射到一部分 trainable capacity。

---

### Method

```text
Team trajectories
↓
prefix-local behavior representation
↓
future-utility target
↓
role prototype
↓
readable role instruction
+
token-level role marker
↓
agent assignment
↓
optional sparse LoRA rank routing
↓
turn-aligned GRPO
```

([arXiv](https://arxiv.org/html/2608.11949v1))

---

### 一个关键设计

ExRole 不给每个 Agent 完全独立 LoRA。

而是在 shared LoRA 内：

> 根据 role 决定哪些 rank slots 被激活。

所以 role identity 连接：

```text
Trajectory
→ Prompt behavior
→ Token marker
→ LoRA capacity
```

([arXiv](https://arxiv.org/html/2608.11949v1))

这对 unlearning 很重要：

> 终于有可能定义 **Role-level Forget Object**。

---

### Results

MuSiQue 上 ExRole-Shared：

$$
EM=31.5,\quad F1=43.2
$$

相较 single-agent search：

$$
+15.0\ EM,\quad +14.4\ F1.
$$

相较最强 non-ExRole control：

$$
+11.5,\quad+11.6.
$$

2WikiMultiHopQA 也分别相较 single-agent search 提升：

$$
+13.5\ EM,\quad+16.1\ F1.
$$

([arXiv](https://arxiv.org/html/2608.11949v1))

---

### Contribution

1. trajectory-conditioned role induction；
2. future-aware role prototype；
3. executable textual role identity；
4. role-conditioned sparse LoRA routing；
5. turn-aligned credit。([arXiv](https://arxiv.org/html/2608.11949v1))

---

### Limitation

主要验证：

- MuSiQue；
- 2WikiMultiHopQA；

所以目前更多是 multi-agent evidence-seeking，而不是开放工具 Agent。

role prototype 是否会跨任务保持同样语义，也需要进一步验证。

---

### Migration

这篇可以产生一个很新的问题：

# Role Unlearning

不是：

```text
Forget fact K
```

而是：

```text
Forget role R's learned capability
```

因为 ExRole 已经建立：

```text
trajectory
↔ role
↔ parameter capacity
```

可以测试：

```text
remove role marker
remove routed LoRA ranks
erase role trajectories
```

哪个才真正删除该角色能力。

更进一步：

> 删除 Agent A 的 role 后，Agent B/C 是否重新承担该 role？

这就是：

# **Role Reallocation after Multi-Agent Unlearning**

很新。

**Worth Deep Reading：YES。**

---

# A3｜BACKFILL
## Forecasting Side Effects of Activation Steering

**Chong Yong Ong et al.**  
arXiv:2608.11227，论文页面标记 **2026-07-28**。([arXiv](https://arxiv.org/html/2608.11227v1))

---

### Background

Activation steering：

$$
h'_\ell
=
h_\ell+\alpha\bar n_\ell v_i.
$$

意思就是：

> 在中间层沿行为方向 $v_i$ 推一下 hidden state。([arXiv](https://arxiv.org/html/2608.11227v1))

问题：

```text
steer behavior A
```

经常同时改变：

```text
B
C
D
...
```

但以前基本是：

> steer 完以后才测 collateral damage。

---

### Core Insight

作者构造：

# Cross-Effect Matrix

$$
M_{ij}
=
\text{steer behavior i 后 behavior j 的变化}.
$$

覆盖：

- 67 behaviors；
- Gemma-3-4B；
- Gemma-3-12B；
- Qwen2.5-7B。([arXiv](https://arxiv.org/html/2608.11227v1))

---

### 最重要发现 1：side effects 非常多

33%–50% 的 behavior pairs 存在显著 coupling。

即一个 steering direction 平均可影响：

> 大约 22–33 个其他 behaviors。([arXiv](https://arxiv.org/html/2608.11227v1))

---

### 发现 2：关系是 asymmetric

可能：

$$
A\rightarrow B>0
$$

但：

$$
B\rightarrow A<0.
$$

18%–26% 的双向显著 pair 甚至出现 opposite signs。([arXiv](https://arxiv.org/html/2608.11227v1))

所以单纯：

$$
cos(v_A,v_B)
$$

很难解释 interaction，因为 cosine 天生是 symmetric。

作者发现 similarity-based heuristic 最多只能解释约 **23%** coupling variance。([arXiv](https://arxiv.org/html/2608.11227v1))

---

### Method

他们学习：

1. target behavior linear probe $r_j$；
2. injection layer → readout layer 的 linear propagation map $W$。

预测：

$$
\hat M_{ij}
=
\langle Wv_i,r_j\rangle.
$$

直觉：

```text
steering vector
↓
预测它穿过 transformer 后会变成什么
↓
看最终方向和 target behavior probe 多对齐
```

([arXiv](https://arxiv.org/html/2608.11227v1))

---

### Results

不用真的进行 steering，只使用 unsteered data：

> 对重大 side effects 的 amplification / suppression direction 可预测约 **68%–78%**。([arXiv](https://arxiv.org/html/2608.11227v1))

而构造完整 matrix 每模型约需要 128k steered generations，预测模型只需约 1,288–2,039 个普通 generations。([arXiv](https://arxiv.org/html/2608.11227v1))

---

### Contribution

1. steering cross-effect matrix；
2. 发现 asymmetric behavioral coupling；
3. 证明 cosine-style similarity 不足；
4. 提出 propagation-aware side-effect forecasting。([arXiv](https://arxiv.org/html/2608.11227v1))

---

### Migration to Unlearning

这篇其实非常适合昨天你关注的 **Relationship-Aware Unlearning**。

定义：

$$
U_{ij}
=
\text{unlearn }K_i
\text{ 对 }K_j\text{ 的影响}.
$$

得到：

# **Unlearning Cross-Effect Matrix**

然后测试：

$$
U_{ij}\neq U_{ji}
$$

是否普遍成立。

如果成立，就说明：

> semantic similarity 并不足以描述 unlearning interference。

然后可以进一步：

```text
unsteered/original activations
→ predict which retain knowledge will be damaged
```

即：

# **Predict Forget-Retain Damage Before Unlearning**

这可能比简单 Relationship-Aware Benchmark 更进一步。

**Worth Deep Reading：YES。**

---

# Tier B

## B1. Reinforcing Step-level Reasoning for Effective Self-Correction in LLMs

**Vu Duc Anh et al.**  
arXiv:2608.11573，**2026-08-12**。([arXiv](https://arxiv.org/pdf/2608.11573))

### Background / Problem

传统 preference：

```text
整个 answer good
vs
整个 answer bad
```

但 reasoning error 往往只发生在某一步。

作者提出 **SFS-DPO**：

```text
Step-level preference initialization
↓
Step-wise self-correction training
```

第一阶段：

> 给正确 reasoning step 更高概率，压低错误 step。

第二阶段：

```text
错误 step
→ detect error
→ generate corrected step
```

([arXiv](https://arxiv.org/pdf/2608.11573))

---

### Contribution

真正值得保存的是：

> **step-level reasoning supervision 与 correction training 不应该混成一个 objective，而应该先学局部 discrimination，再学 correction。**

作者的 ablation 显示直接联合训练、没有强 step-level initialization 时性能明显变差；Step RL initialization 优于普通 RL initialization。([arXiv](https://arxiv.org/pdf/2608.11573))

---

### 和 Unlearning 的关系

可以反向迁移：

```text
Reasoning Trace
↓
定位 knowledge-bearing step
↓
只对那个 step 做 negative preference
↓
保留其余推理
```

未来用途：

**Token/Step-level Unlearning / Reasoning Leakage / Baseline Inspiration。**

---

# B2｜BACKFILL
## Harnessing agent memory to build lifelong AI partners for materials scientists

**Siyu Liu et al.**  
arXiv:2608.11224。论文内容围绕**可迁移、可检查、带 provenance 的长期 Agent memory**。([arXiv](https://arxiv.org/html/2608.11224v1))

### Background

作者认为真正应该持久存在的不是 Agent 本身，而是：

> **experience artifact**。

它可以包含：

- facts；
- executable skills；
- failure boundary；
- protocol；
- validation check；
- provenance。

并且能够：

```text
Model A
→ memory
→ Model B
```

跨 Agent stack 迁移。([arXiv](https://arxiv.org/list/cs/new))

---

### Main Finding

49 个 real-world tool-use questions、138 executable subtasks 中，memory 几乎让 GPT-5.2 task success 翻倍。

在 equation-of-state workflow：

```text
22/1/4 Correct/Partial/Error
→
25/2/0
```

并避免了 **92% repeated errors**。([arXiv](https://arxiv.org/html/2608.11224v1))

在 13 个 material simulation workflows 中，到第三轮：

- aggregate trace tokens 大约减半；
- tool calls 超过 2× 减少。([arXiv](https://arxiv.org/list/cs/new))

---

### Contribution

真正贡献不是材料领域 Agent。

而是：

> 把 **agent experience 定义成独立于 model 的、带 provenance 的 durable memory asset**。([arXiv](https://arxiv.org/html/2608.11224v1))

---

### Connection

这对 Agent Unlearning 恰恰构成挑战：

```text
Model forgotten
```

但是：

```text
portable memory artifact survives
```

然后：

```text
new model
← memory migration
← deleted capability returns
```

这就是非常典型的：

# Cross-Model Reacquisition

未来用途：

**Agent Memory Unlearning / Deletion Closure / Reacquisition Attack / Provenance。**

---

# B3. Convergent Detour Hijacking: Task-Preserving Resource Amplification in Skill-Based LLM Agents

arXiv:2608.12273，本轮新安全论文。([arXiv](https://arxiv.org/html/2608.12273v1))

### Problem

传统 Agent attack 常让：

```text
任务失败
```

于是很好发现。

CDH 更阴：

```text
任务照样完成
↓
但是 agent 被诱导走一条巨大 detour
↓
偷偷消耗更多 skill / token / time
```

它利用：

```text
skill description
→ selection hijack

skill body
→ planning hijack
```

然后再回到合法 route。([arXiv](https://arxiv.org/list/cs.AI/new))

---

### Main Finding

491 个 held-out tasks 中，DeepSeek-V4-Pro：

attacker coordinator 被选中：

$$
80.02\%.
$$

在最终仍成功完成任务的攻击样本中：

- token consumption：**+66.91%**
- execution time：**+92.45%**

而 overall task completion 仍接近正常。([arXiv](https://arxiv.org/html/2608.12273v1))

---

### Contribution

它证明：

$$
Correct\ Final\ Outcome
\not\Rightarrow
Healthy\ Trajectory.
$$

这个结论和今天 S2 完全呼应。

---

### Connection to Unlearning

同样：

$$
Correct\ Forget\ Answer
\not\Rightarrow
Clean\ Forget\ Trajectory.
$$

一个 Agent 即使最后拒绝：

```text
“I don't know K”
```

中间也可能：

```text
retrieve K
→ pass K to tool
→ summarize K
→ eventually suppress output
```

因此 future Agent Unlearning benchmark 应加入：

> **trajectory integrity**。

未来用途：

**Evaluation / Attack / Agent Security Related Work。**

---

# 全部论文二次筛选

# 🥇 Today's Most Important Paper

## Backdoor Decontamination Dynamics in LLM Agents

今天它明显排第一。

因为它同时踩中：

- Agent；
- Unlearning；
- Continual interference；
- multiple targets；
- behavioral suppression；
- representation residual；
- tool-level evaluation。

最应该关注的不是它的 backdoor defense 本身，而是这条实验事实：

> **Recognition 可以保留，而 Execution 已经被 unlearn。**([arXiv](https://arxiv.org/pdf/2608.11295))

这正是 Machine Unlearning 最需要警惕的：

$$
Answer\ Forgotten
\not\Rightarrow
Knowledge\ Erased.
$$

---

# 🔥 Top 3 必读

### 1. Backdoor Decontamination Dynamics in LLM Agents

**必须读什么：**

`recognition → behavior` 拆分，以及 A×B interference matrix。

**直接用途：**

Representation-level Agent Unlearning、collateral forgetting、relationship-aware continual unlearning。

---

### 2. Beyond Single-Turn Confidence

**必须读什么：**

TER、Action-Set Consistency、multi-rollout black-box evaluation。

**直接用途：**

可以马上迁移成：

> **Black-box Multi-Trajectory Unlearning Verification**。([arXiv](https://arxiv.org/html/2608.11552v1))

---

### 3. Agent Skills Can Be Harmful

**必须读什么：**

paired-trajectory differential attribution。

**直接用途：**

把：

```text
with / without skill
```

改成：

```text
pre / post unlearning
```

定位 unlearning 到底破坏了哪个 trajectory mechanism。([arXiv](https://arxiv.org/html/2608.11888v1))

---

# 🥈 Top 5 最重要论文

1. **Backdoor Decontamination Dynamics in LLM Agents**
2. **Beyond Single-Turn Confidence**
3. **Agent Skills Can Be Harmful**
4. **ExRole**
5. **Forecasting Side Effects of Activation Steering**

---

# 💡 Idea Mining

## Idea 1 — Recognition–Execution Decoupled Unlearning Audit

### Inspiration

Backdoor Decontamination。

### Research Gap

现有 Unlearning 多数测：

$$
P(answer)
$$

或：

$$
Accuracy.
$$

但缺少：

> 模型是否仍然**识别** forgotten concept。

### Hypothesis

很多方法其实是：

```text
Recognize K
↓
Suppress K
```

而不是：

```text
Erase K
```

因此：

$$
Recognition_U
\gg
Recognition_{Retrain}.
$$

### Proposed Method

构造三个层面：

```text
Knowledge Recognition
↓
Knowledge Utilization
↓
Knowledge Expression
```

分别测。

例如 forgotten identity：

**Recognition**

> 两张图片是不是同一被删人物？

**Utilization**

> 使用这个人物信息能否解 derived problem？

**Expression**

> 直接说姓名。

定义：

$$
RUE =
(R,\ U,\ E).
$$

### Minimum Viable Experiment

MLLMU：

- LLaVA；
- Qwen2-VL。

Baseline：

- GA；
- NPO；
- MANU；
- MMUnlearner；
- token method。

Metric：

- Recognition Acc；
- Derived Utilization；
- Direct Forget；
- GT probability；
- recovery ASR。

### Expected Contribution

证明：

> **MLLM Unlearning 的 residual knowledge 可以停留在 Recognition-only state。**

### Novelty

★★★★★

### Feasibility

★★★★★

### Compute Cost

★★☆☆☆

### Risk

recognition task 必须防止被视觉 shortcut 污染。

### Collision Risk

★★☆☆☆

### Best Venue

NeurIPS / ACL / AAAI。

---

# Idea 2 — Multi-Trajectory Black-Box Unlearning Verification

### Inspiration

Beyond Single-Turn Confidence。

### Research Gap

Black-box unlearning evaluation 几乎都以：

```text
query → output
```

为单位。

Agent 应该用：

```text
query → trajectory distribution
```

### Hypothesis

存在大量：

$$
SingleRolloutForget=1
$$

但：

$$
BestOfNRecovery=1.
$$

### Proposed Method

对同一 target：

```text
temperature sampling
tool-order perturbation
memory retrieval perturbation
prompt paraphrase
```

生成 N 条 trajectory。

计算：

$$
FTC=
\frac{\#ForgetTrajectories}{N}.
$$

以及：

$$
B_n
=
P(\exists\,\text{recovery in }N\text{ trajectories}).
$$

如果单次 recovery probability 为 $p$，理论上：

$$
B_n=1-(1-p)^n.
$$

所以哪怕：

$$
p=0.05
$$

20 次查询：

$$
B_{20}\approx64\%.
$$

这说明 tiny leakage 可能在 query budget 下变成严重 vulnerability。

### Models/Dataset

AgentBench-style + Agent Unlearning environment。

### Baselines

- single rollout；
- paraphrase attack；
- self-consistency；
- TER；
- best-of-N。

### Expected Contribution

提出：

> **forgetting reliability under stochastic trajectory distributions**

而不是 deterministic score。

### Novelty

★★★★★

### Feasibility

★★★★★

### Compute Cost

★★★☆☆

### Collision Risk

★★☆☆☆

### Best Venue

USENIX Security / CCS / NeurIPS / ACL。

---

# Idea 3 — Unlearning Cross-Effect Matrix

### Inspiration

Forecasting Side Effects of Activation Steering + Backdoor Decontamination。

### Gap

当前 forget-retain trade-off 大多只报告：

```text
average Forget
average Retain
```

把知识样本当成 iid。

但实际可能：

$$
U_{ij}
\neq
U_{ji}.
$$

### Hypothesis

Unlearning interference 是：

> structured + asymmetric + low-dimensional。

也就是说：

```text
forget Alice-school
→ strongly damages Alice-city
```

并不意味着：

```text
forget Alice-city
→ equally damages Alice-school
```

### Proposed Method

构造：

$$
U\in\mathbb R^{N\times N}.
$$

其中：

$$
U_{ij}
=
Score(K_j\mid Unlearn(K_i))
-
Score(K_j\mid Original).
$$

分关系：

- same entity；
- semantic neighbor；
- derived fact；
- cross-modal equivalent；
- unrelated。

然后：

- SVD；
- asymmetry score；
- graph clustering；
- low-rank structure。

进一步学习：

```text
Original representations
→ predict Uij
```

### Minimum Experiment

TOFU + MLLMU-Bench，50–100 targets。

### Metric

- asymmetry；
- effective rank；
- prediction Spearman；
- collateral retain damage；
- recovery。

### Expected Contribution

把 forget-retain tradeoff 变成：

> **Unlearning Interaction Geometry**。

### Novelty

★★★★★

### Feasibility

★★★★☆

### Compute Cost

★★★★☆

因为 pairwise matrix 比较费算力。

### Collision Risk

★★☆☆☆

### Best Venue

NeurIPS / ICLR。

**今天我最看好这个 idea。**

---

# Idea 4 — Role-Level Multi-Agent Unlearning

### Inspiration

ExRole。

### Gap

Multi-Agent Unlearning 中：

> “到底删除什么”

一直很模糊。

现在 ExRole 给了一个新 object：

```text
Trajectory-derived Role
```

它同时对应：

- behavior；
- instruction；
- token marker；
- LoRA rank capacity。

### Hypothesis

删除某 Agent 的 role capability 后，MAS 会发生：

> **role migration / role substitution。**

即：

```text
Agent A role deleted
↓
Agent B spontaneously acquires / assumes role
```

导致：

$$
LocalForget=1
$$

但：

$$
CollectiveForget=0.
$$

### Proposed Experiment

ExRole style 3-agent system。

删除：

```text
Retriever Role
```

三种删除：

1. prompt marker removal；
2. routed LoRA rank removal；
3. trajectory/memory removal。

测：

- local role success；
- team success；
- role reallocation；
- other-agent specialization；
- reacquisition rounds。

### Contribution

第一次形式化：

> **Role as Forget Object in Multi-Agent Systems**

以及：

> **Collective Role Reacquisition**。

### Novelty

★★★★★

### Feasibility

★★★★☆

### Compute Cost

★★★☆☆

### Collision Risk

★★☆☆☆

### Best Venue

AAAI / ACL / NeurIPS。

---

# ⚠️ Collision Detection

## Collision Warning 1 — Agent Behavioral Unlearning

### 论文

**Backdoor Decontamination Dynamics in LLM Agents**

### 重合程度

**高，如果你的 idea 只是：**

> 用 unlearning 去消除 Agent 的恶意 tool-use behavior。

这篇已经明确做了：

- tool-using Agent；
- behavioral association removal；
- unknown trigger；
- multiple backdoors；
- collateral unlearning；
- internal residual analysis。([arXiv](https://arxiv.org/pdf/2608.11295))

### 仍有 gap

非常大：

- factual knowledge；
- personal data；
- persistent memory；
- cross-agent；
- multimodal；
- trajectory provenance；
- exact/approximate deletion；
- retain-only oracle；
- knowledge reacquisition。

所以：

> **Agent Unlearning 仍然值得做，但不能只定义成 harmful behavior suppression。**

---

# ⚠️ Collision Warning 2 — Role / Skill Unlearning

今天两篇论文共同把这个空间推得很快：

**Agent Skills Can Be Harmful**

已经把：

```text
skill → trajectory failure
```

的 attribution 建起来。([arXiv](https://arxiv.org/html/2608.11888v1))

**ExRole**

又把：

```text
trajectory → role → LoRA capacity
```

建起来。([arXiv](https://arxiv.org/html/2608.11949v1))

因此如果未来做：

> “删一个 Agent skill”

单纯删 skill 文件已经明显不够新。

真正有空间的是：

```text
skill representation
+
trajectory effects
+
parameter specialization
+
role redistribution
```

的联合删除。

---

# ⚠️ Collision Warning 3 — Relationship-Aware Continual Unlearning

昨天提出的 Relationship-Aware Continual Unlearning **仍然值得继续，但今天应该升级。**

因为 Forecasting Side Effects of Activation Steering 已经说明：

> behavioral intervention interactions 不只是“有关系/没关系”，而可能是**structured、asymmetric、low-rank**。([arXiv](https://arxiv.org/html/2608.11227v1))

所以比昨天更强的版本应该从：

```text
Relationship-Aware Continual Unlearning
```

升级成：

# **Unlearning Interaction Geometry**

研究：

$$
K_i\rightarrow K_j
$$

的有向影响，而不只是 relationship category。

这明显更像一篇 method + benchmark + analysis paper。

---

# 最终 Daily Research Brief

## 🥇 Today's Most Important Paper

### **Backdoor Decontamination Dynamics in LLM Agents**

最重要的不是它“清除了多少后门”，而是它给出了一个非常关键的 Agent Unlearning 现象：

> **Execution 被删除后，Recognition 仍可留在内部。**([arXiv](https://arxiv.org/pdf/2608.11295))

---

## 🔥 Top 3 必读

**1. Backdoor Decontamination Dynamics in LLM Agents**  
学：Recognition–Execution decomposition、collateral forgetting、multi-target interaction。

**2. Beyond Single-Turn Confidence**  
学：trajectory-level black-box consistency、TER、multi-rollout evaluation。

**3. Agent Skills Can Be Harmful**  
学：paired trajectory differential attribution、skill→failure causal localization。

---

## 🥈 Top 5 最重要论文

1. **Backdoor Decontamination Dynamics in LLM Agents**
2. **Beyond Single-Turn Confidence**
3. **Agent Skills Can Be Harmful**
4. **ExRole**
5. **Forecasting Side Effects of Activation Steering**

---

# 💡 Best Research Idea

## **Unlearning Interaction Geometry**

今天我把昨天的 **Relationship-Aware Continual Unlearning** 再往前推一层。

核心不是：

> 两次删除是否 related。

而是学习一个：

$$
U_{ij}
=
\text{unlearn }K_i
\text{ 后 }K_j\text{ 被改变多少}
$$

的 **有向 cross-effect matrix**。

然后研究：

- asymmetric；
- low-rank；
- semantic relation；
- cross-modal relation；
- derived knowledge；
- continual sequence；
- recovery。

如果能观察到类似 activation steering 的：

> 大量 interaction、显著不对称、低维结构，

那么 contribution 会非常漂亮：

> **Machine Unlearning is not an independent set of deletion tasks; it forms a structured interference geometry.**

这比单纯再提一个新的 GA/NPO loss，我认为研究价值高得多。

---

# ⚠️ Collision Alert

今天最值得警惕的是：

> **Agent Unlearning 已经开始和 Agent Backdoor Removal、Skill Attribution、Trajectory Analysis、Role Learning 快速交叉。**

因此以后如果做 Agent / Multi-Agent Unlearning，最好不要只说：

```text
parameter + memory
```

而应该明确你研究的独有对象，例如：

- cross-agent deletion closure；
- role reacquisition；
- trajectory residual；
- recognition–execution gap；
- provenance closure；
- coalition recovery。

---

# 📚 Reading Priority

**READ NOW：**

- Backdoor Decontamination Dynamics in LLM Agents
- Beyond Single-Turn Confidence
- Agent Skills Can Be Harmful

**READ THIS WEEK：**

- ExRole
- Forecasting Side Effects of Activation Steering
- Reinforcing Step-level Reasoning

**SAVE：**

- Harnessing agent memory to build lifelong AI partners for materials scientists
- Convergent Detour Hijacking

**SKIP：**

今天没有把明显弱相关的论文塞进来凑数量。对当前研究最有价值的新信号非常集中：**Agent 的“忘记”必须开始从 final behavior 扩展到 recognition、representation、trajectory、skill、role 和 cross-target interaction。**

---
Powered by [AI Exporter](https://saveai.net)