# Intern Interview Predictor

一个面向实习、校招、应届和初级技术岗位的 Codex Skill，用于基于岗位 JD 与简历内容重建招聘信号、预测面试阶段、生成高概率问题，并深挖项目真实性风险。

它不是普通的八股题生成器，也不是简单模拟“大厂面试官追问链”。它的目标是还原真实招聘方的验证逻辑：

```text
JD + Resume
→ Hiring Signal Reconstruction
→ JD × Resume Alignment
→ Interview Stage Prediction
→ Evidence-based Interview Questions
→ Project Authenticity Deep Dive
→ Internship Risk Analysis
```

## 适用场景

- 根据 JD 和简历预测实习/校招面试问题
- 分析 JD 与简历的匹配度和风险点
- 预测 OA、一面、二面、项目深挖、HR 面等面试阶段
- 生成基于证据的技术、行为和项目追问
- 深挖 AI、RAG、Agent、后端、前端、数据等项目真实性
- 判断候选人最危险的淘汰点和准备重点

## 输出重点

- JD 信号分析
- Resume 信号分析
- JD × Resume 对齐分析
- 实习招聘风险分析
- 面试阶段预测
- 高概率 Evidence-based questions
- 项目真实性 deep-dive chains
- 压力追问模拟
- 最危险淘汰点

## 安装

推荐使用 `npx skills` 一键安装：

```bash
npx skills add https://github.com/Benson7zhang/intern-interview-predictor -g --agent codex claude-code --skill intern-interview-predictor -y
```

安装完成后，重启 Codex / Claude Code，让客户端重新加载 skills。

## 快速开始

在 Codex 或 Claude Code 中输入：

```text
Use $intern-interview-predictor

请根据下面这个 JD 和我的简历，预测实习面试中最可能被问到的问题，并重点分析项目真实性风险。

JD：
[粘贴岗位 JD]

Resume：
[粘贴简历、项目经历，或上传简历文件后说明]
```

## 输入格式

效果最好的是同时提供 `JD + Resume`：

```text
JD：
- 岗位名称：
- 岗位职责：
- 任职要求：
- 加分项：

Resume：
- 教育背景：
- 技术栈：
- 项目经历：
- 实习 / 比赛 / 开源：
```

也可以只提供其中一个：

- 只有 JD：输出岗位信号、可能面试阶段、高概率问题和准备重点。
- 只有简历：输出项目真实性深挖、简历风险点和可能被问到的问题。
- JD + 简历：输出完整的招聘信号重建、匹配度分析、面试问题和淘汰风险。

## 常用用法

```text
Use $intern-interview-predictor

根据这个 JD 和我的简历，帮我预测一面会问什么。
```

```text
Use $intern-interview-predictor

重点深挖我的 RAG 项目，模拟面试官连续追问。
```

```text
Use $intern-interview-predictor

请分析这个岗位和我的简历匹配度，指出最危险的淘汰点。
```

```text
Use $intern-interview-predictor

我只有 JD，先帮我判断这个实习岗最可能考什么。
```

## 示例输入

```text
Use $intern-interview-predictor

我准备投一个 AI 应用开发实习岗位。请根据这个 JD 和我的项目经历，预测真实面试中最可能被问到的问题，并重点深挖项目真实性。

JD：
- 参与 AI Web 产品开发
- 熟悉 Vue、TypeScript、RESTful API
- 熟悉 MySQL，有基础后端开发经验
- 了解 LangChain、RAG、AI API 调用
- 有完整项目经验、能快速学习新技术者优先

Resume：
- 做过一个 RAG 知识库项目，使用 LangChain、OpenAI API、向量数据库和 Vue 前端
- 实现了文档上传、切分、向量检索、问答页面
- 简历写到“优化检索准确率并降低响应延迟”
- 项目目前是个人 Demo，没有真实用户
```

## 示例输出节选

```markdown
# 实习面试预测：AI 应用开发 Intern

## 1. JD 信号分析

- 岗位方向：AI Web / Full-stack Intern
- 核心技术信号：Vue、TypeScript、RESTful API、MySQL、LangChain、RAG、AI API
- 隐含能力：快速学习、工程落地、前后端协作、AI 项目理解、项目真实性
- 招聘风险：只会调用 API、不理解 RAG 机制、项目 Demo 包装过重、后端基础不足

## 2. Resume 信号分析

- 强信号：有完整 RAG 项目闭环，覆盖上传、切分、检索、问答 UI
- 弱信号：没有真实用户，缺少部署、评估指标和线上问题
- 高风险信号：“优化检索准确率并降低响应延迟”需要证明具体优化动作和数据来源

## 3. JD × Resume 对齐分析

alignment:
  strong_match:
    - RAG / LangChain / AI API 与 JD 高度匹配
    - Vue 前端项目经验与 AI Web 开发匹配
  weak_match:
    - MySQL 和后端 API 经验证据较弱
    - “优化准确率/延迟”缺少可验证指标
  high_risk_areas:
    - 是否只是套 API
    - 是否理解 chunking、embedding、top-k、rerank、hallucination
    - 是否能解释自己具体负责的实现细节

## 4. 面试阶段预测

- 一面 / 技术基础：Vue、TypeScript、RESTful API、MySQL 基础、RAG 基本机制
- 项目深挖：重点验证 RAG 项目是否真实做过，以及优化是否有依据
- HR / 主管面：学习能力、实习稳定性、项目表达和自驱力

## 5. 高概率问题

question: 你这个 RAG 项目里，文档切分策略是怎么设计的？为什么这样切？
category: AI / RAG project deep dive
stage: 项目深挖
probability: high
evidence:
  jd: JD 明确提到 LangChain、RAG、AI API 调用
  resume: 简历写到文档上传、切分、向量检索、问答页面
intent: 验证是否真正理解 RAG，而不是只调用封装库
risk_signal: 如果只能说“LangChain 自动切”，说明项目真实性和技术深度不足
expected_good_signal: 能解释 chunk size、overlap、文档结构、召回质量和上下文长度限制
red_flags:
  - 不知道 chunk size
  - 没有评估过召回效果
  - 无法说明切分对回答质量的影响
follow_ups:
  - 如果 chunk 太大或太小分别会有什么问题？
  - 你怎么判断切分策略真的变好了？
  - 为什么不用全文直接塞进 prompt？

## 6. 项目真实性深挖链

项目：RAG 知识库

1. Ownership：你具体写了哪些模块？上传、切分、检索、前端页面分别是谁做的？
2. Design：为什么选 LangChain，而不是自己写 retrieval pipeline？
3. Implementation：向量库里存了什么字段？metadata 怎么设计？
4. Debugging：有没有出现过答非所问？你怎么定位是召回问题还是模型生成问题？
5. Trade-off：为什么不用 fine-tuning？
6. Measurement：你说优化准确率，准确率怎么定义？有没有 before/after 数据？
7. Rebuild：如果重新做一版，你会优先改哪里？

## 7. 最危险淘汰点

- 说不清 RAG 关键参数和取舍，会被判断为 AI API 套壳。
- “优化准确率/延迟”没有数据支撑，会被认为简历包装。
- 后端和 MySQL 证据不足，可能在基础轮被追问 API 设计、表结构和查询性能。
```

## 免责声明

本项目用于面试准备和学习训练，不代表任何公司的真实题库、官方面试标准或招聘结论。

## License

MIT
