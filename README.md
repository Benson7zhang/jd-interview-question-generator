# Intern Interview Predictor

一个面向实习、校招、应届和初级技术岗位的 Codex Skill，用于基于 JD 与简历重建招聘信号、预测面试阶段、生成高概率问题，并深挖项目真实性风险。

它的目标不是生成普通八股题库，而是还原真实面试官的验证逻辑：

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

将本仓库放到 Codex skills 目录中，例如：

```bash
mkdir -p ~/.agents/skills
git clone git@github.com:Benson7zhang/jd-interview-question-generator.git ~/.agents/skills/intern-interview-predictor
```

然后在 Codex 中使用：

```text
Use $intern-interview-predictor 根据下面这个 JD 和简历预测实习面试问题：

[粘贴岗位 JD]
[粘贴简历或项目经历]
```

## 示例用法

```text
Use $intern-interview-predictor

我准备投一个 AI 应用开发实习岗位。请根据这个 JD 和我的项目经历，预测真实面试中最可能被问到的问题，并重点深挖项目真实性。

JD：
参与 AI Web 产品开发，熟悉 Vue、TypeScript、MySQL、RESTful API，了解 LangChain、RAG、AI API 调用，有项目经验优先。

Resume：
做过一个 RAG 知识库项目，使用 LangChain、OpenAI API、向量数据库和 Vue 前端。
```

## 免责声明

本项目用于面试准备和学习训练，不代表任何公司的真实题库、官方面试标准或招聘结论。

## License

MIT
