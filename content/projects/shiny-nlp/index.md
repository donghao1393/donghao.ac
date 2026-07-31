---
title: NLP 预测模型 Demo
summary: Coursera JHU Data Science Capstone——n-gram 语言模型 + Good-Turing 平滑，部署在 shinyapps.io
tags:
  - NLP
  - R Shiny
  - Machine Learning
  - Coursera
date: '2016-04-16T00:00:00Z'

links:
  - type: site
    url: https://haodong.shinyapps.io/A_NLP_Prediction_Model/
    icon: link
    icon_pack: fas
    name: 在线 Demo
---

## 背景

2016 年，Coursera 上与 Johns Hopkins 大学合作的 Data Science 专项课程的 Capstone 项目。课程以 SwiftKey 输入法为例，提供一个来自推特的英文语料库，要求我们独立完成从数据清洗到预测建模的完整流程，最终交付一个可交互的 Shiny 应用。

当时读了吴军老师的《数学之美》，对自然语言处理的统计方法产生了深刻的兴趣——书中讲马尔可夫链、n-gram 模型、信息熵的那几章，直接指导了我接下来的工作。

## 做了什么

1. **数据清洗与探索**：从原始 Twitter 语料中抽样、分词、去停用词、构建 n-gram 频率矩阵。写了一份完整的数据探索报告（[R Markdown](https://github.com/donghao1393)），分析了词频分布、Zipf 定律的实证表现、以及 blog/news/twitter 三种文本的句式差异。

2. **n-gram 语言模型**：基于马尔可夫假设构建 unigram/bigram/trigram 模型。核心挑战是处理未见过的 n-gram——模型在训练集中没见过的词组合，不能直接给零概率。

3. **Good-Turing 平滑**：用 $r+1$ 次出现的 n-gram 数量来重新估计 $r$ 次出现的概率，使得训练集中从未出现的 n-gram 也能获得非零概率——"从未见过"不等于"不可能出现"。

4. **Shiny 交互式部署**：将训练好的模型打包成 R Shiny 应用，部署在 shinyapps.io 上。输入文本，实时返回下一个词的预测。

## 技术栈

R · quanteda · data.table · ggplot2 · Shiny · Good-Turing Estimation · shinyapps.io

## 为什么值得看

这是 2016 年自学完成的。没有导师、没有实验室、没有 GPU——就用一台 MacBook 和 Coursera 上的课程视频。从数据清洗到数学模型到交互式部署，一条完整的独立生产线。八年后回头看，这也是我后来做 mcp-dbutils、做 AI Agent 的底层工作流原型：**拿到数据 → 理解本质 → 建模 → 部署给人用**。
