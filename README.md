# Epi Skill README

## 简介

`epi-skill` 是一个面向流行病学、医学统计学、生物统计学和临床研究方法学的 AI skill。该 skill 是基于多本方法学教材的本地扫描与主题提炼，整理出适合研究设计、统计分析、偏倚评估、模型选择和论文方法学审查的工作流与检查清单。

## 蒸馏来源

本 skill 的方法学框架主要蒸馏自以下书籍：

1. **Biostatistics & Epidemiology**
2. **Fundamentals of Biostatistics**
3. **Medical Statistics at a Glance, 4th Edition**
4. **Modern Epidemiology, 4th Edition**
5. **The New Statistics with R: An Introduction for Biologists**
6. **Understanding Advanced Statistical Methods**

## 适用范围

该 skill 适用于以下任务：

- 流行病学研究设计与方法学审查
- 横断面研究、病例对照研究、队列研究、随机对照试验和诊断研究设计
- 暴露、结局、协变量、混杂因素和效应修饰因素定义
- DAG、目标试验模拟和因果推断思路梳理
- 回归模型、广义线性模型、生存分析、预测模型和诊断模型选择
- 缺失值、选择偏倚、信息偏倚、混杂、反向因果和不朽时间偏倚检查
- 效应量、置信区间、P 值、模型诊断和敏感性分析解释
- 论文方法、结果和讨论部分的统计学审查
- 审稿意见回应与方法学补强

## 核心原则

使用该 skill 时，优先遵循以下原则：

1. 先明确研究问题属于描述、关联、预测、诊断、因果推断还是临床决策支持。
2. 先定义目标人群、暴露或干预、比较组、结局、时间零点、随访窗口、估计目标和数据来源。
3. 在建模前完成数据结构审查，包括变量编码、缺失、重复、时间顺序、单位、分母和结局判定。
4. 将偏倚控制放在研究设计阶段，而不是仅在讨论部分补充说明。
5. 根据估计目标和数据结构选择模型，而不是只根据变量类型机械选择检验方法。
6. 区分关联分析、预测模型、诊断模型和因果推断，避免将探索性结果过度解释为临床结论。
7. 报告效应量、置信区间、样本量、分母、时间尺度、模型假设、诊断结果和敏感性分析。

## 文件结构

```text
epi-skill/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── methodology-workflow.md
    ├── study-design-checklists.md
    └── source-scan-provenance.md
```

## 使用建议

当任务涉及研究设计或统计分析时，先读取 `SKILL.md`，再根据具体问题调用 `references/` 下的补充材料：

- `methodology-workflow.md`：从研究问题到分析解释的完整方法学工作流。
- `study-design-checklists.md`：不同研究设计和统计模型的审查清单。
- `source-scan-provenance.md`：教材扫描与方法信号来源说明。

## 注意事项

本 skill 只保留方法学框架、分析原则和审查清单，不复制教材章节、长段原文或受版权保护的完整内容。原始书籍仅作为方法学蒸馏来源，未随 skill 一并分发。
