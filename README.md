# epi-skill

### 现已更新到2.0

`epi-skill` 是一个面向医学研究方法学的本地 AI skill。它有三个模块：

1. **传统流行病学**
2. **预测模型**
3. **因果推断**

顶刊论文、教材和本地 PDF 扫描内容都被拆解进这三个模块。

## 安装位置


当前结构：

```text
C:\Users\cbl02\.codex\skills\epi-skill
├── SKILL.md
├── agents\
│   └── openai.yaml
└── references\
    ├── traditional-epidemiology.md
    ├── prediction-models.md
    ├── causal-inference.md
    ├── methodology-workflow.md
    ├── study-design-checklists.md
    └── source-scan-provenance.md
```

## 怎么使用

在 Codex、Claude Code 或 Hermes 里，直接在任务前写“用 epi-skill”即可。最稳妥的写法是同时说明模块、材料和你希望得到的产物。

基本格式：

```text
用 epi-skill 的[模块名]，基于[研究方案/论文/数据字典/统计计划/模型结果]，帮我输出[审查意见/研究设计/统计分析方案/方法学段落/审稿回复]。
```

三个模块的调用方式：

```text
用 epi-skill 的传统流行病学模块，审查这个队列研究的研究设计、time zero、暴露/结局定义、混杂控制、缺失数据和敏感性分析。
```

```text
用 epi-skill 的预测模型模块，审查这个 AI 临床预测模型是否按 TRIPOD+AI 报告，并评价 calibration、discrimination、external validation、decision curve 和部署风险。
```

```text
用 epi-skill 的因果推断模块，把这个观察性研究改写成 target trial emulation，并给出 DAG 思路、识别假设、估计方法和敏感性分析。
```

建议提供的输入：

- 研究问题或论文标题。
- 研究设计和数据来源。
- 目标人群、纳排标准、time zero、随访时间。
- 暴露/干预、对照、结局、协变量或预测因子。
- 已有统计分析方案、模型结果、表格或论文 methods/results。
- 你要的输出类型：方案设计、审稿式 critique、可直接写入论文的 methods 文本、统计分析计划、回复审稿人、模型验证清单等。

`epi-skill` 的默认工作方式：

- 先判断 claim 类型：描述、关联、预测、诊断、因果、机制或临床效用。
- 再自动选择三模块之一，必要时在模块间切换。
- 然后审查时间顺序、变量定义、偏倚、混杂、模型、验证、缺失数据、敏感性分析和报告语言。
- 最后输出可执行修改建议和可直接写入方案/论文的文本。

## 1. 传统流行病学模块

文件：

```text
references\traditional-epidemiology.md
```

适用任务：

- 队列、病例对照、横断面、临床试验、诊断/筛查研究的设计审查。
- 暴露、结局、协变量、time zero、随访窗口和效应量定义。
- 选择偏倚、信息偏倚、混杂、反向因果、不朽时间偏倚、碰撞偏倚、过度调整审计。
- 回归、生存分析、竞争风险、聚类/重复测量、缺失数据和敏感性分析。
- 论文 methods、results、limitations 和统计报告语言修正。

已整合的顶刊规则：

- The Lancet 2024 医学统计报告建议：效应量、置信区间、分母、模型目标和假设边界必须清楚，不能只靠 p 值叙事。
- Science 2024 政策性空气污染健康差异文章：政策/环境流行病学必须检查地理、时间、暴露测量、空间聚类、溢出和健康差异 estimand。
- Science 2019 医疗算法偏倚文章：成本、利用、检测、编码、转诊等变量是医疗过程代理，不能直接当作真实临床需要。

## 2. 预测模型模块

文件：

```text
references\prediction-models.md
```

适用任务：

- 临床预测模型、诊断模型、预后模型、风险评分、AI/ML 医疗预测工具。
- intended use、目标人群、预测时间点、预测窗口、结局、候选预测因子和临床阈值定义。
- 样本量、事件数、过拟合、变量选择、惩罚/收缩、缺失值处理和模型开发审查。
- internal validation、external validation、temporal/site validation、model updating。
- calibration、discrimination、threshold performance、Brier/log loss、decision curve、net benefit。
- AI 模型公平性、数据漂移、人机交互、部署监控和临床影响评估。

已整合的顶刊规则：

- BMJ TRIPOD+AI：AI/ML 预测模型仍需按预测模型报告，说明数据来源、样本、结局、预测因子、缺失、建模、调参、验证、性能和限制。
- BMJ prediction model development/evaluation/external validation：外部验证不是一句“validated”，必须说明验证场景、时间、病例组合、测量流程、结局定义和是否更新/再校准。
- The Lancet 2019 AI prediction reporting：AI 预测论文不能只强调算法，需要透明报告预测目标、数据、模型和性能。
- Nature 2023 generalist medical AI：通用/基础医学 AI 需要任务级外部验证，不能用 general capability 代替临床效用。
- Science 2019 algorithmic bias：预测标签若来自成本、利用、编码或转诊，可能编码结构性不公平。
- Cell 2025 generative medical AI：生成式医疗 AI 要审查幻觉、失败模式、任务边界、人机流程和前瞻性影响证据。

## 3. 因果推断模块

文件：

```text
references\causal-inference.md
```

适用任务：

- 因果问题定义、DAG、反事实、potential outcomes、目标试验模拟。
- exchangeability、positivity、consistency、well-defined intervention 等识别条件。
- 标准化、倾向评分、IPW、g-formula、MSM、TMLE、double robust、double machine learning。
- 中介分析、异质性效应、transportability、政策效果、算法影响和因果机器学习。



## 来源



## 典型调用

```text
用 epi-skill 的传统流行病学模块审查这个队列研究设计和统计分析方案。
```

```text
用 epi-skill 的预测模型模块检查这篇 AI 模型论文只报告 AUC 是否足够。
```

```text
用 epi-skill 的因果推断模块把这个观察性研究改成 target trial emulation。
```

## 输出原则

`epi-skill` 默认服务研究方案、投稿论文、审稿回复和可复现分析包：

- 先判断 claim 类型：描述、关联、预测、诊断、因果、机制或临床效用。
- 再审查设计、变量、时间顺序、偏倚、模型、验证、缺失数据和敏感性分析。
- 最后给出可直接写入方案或论文的方法学文本。

它会主动降级不可靠表述：

- 横断面或普通回归不能自动写成因果。
- 内部验证模型不能写成临床可部署。
- 高 AUC 不能等同临床有效。
- 机器学习不能替代因果识别假设。
- 探索性组学发现不能直接写成临床证据。
