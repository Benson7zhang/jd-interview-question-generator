# JD Interview Question Generator

一个用于根据岗位 JD、项目经历、简历内容或岗位方向，模拟互联网大厂技术面试官追问链的 Codex Skill。

它的目标不是生成普通八股题库，而是让回答更像真实面试现场：先判断岗位方向和隐藏考点，再生成一面、二面、项目拷打、场景题、压力追问和优秀候选人的回答方向。

## 适用场景

- 根据岗位 JD 生成面试官可能会问的问题
- 根据项目经历做项目深挖和真实性验证
- 模拟一面、二面、主管面或压力面
- 为实习、校招、应届、初级技术岗位做面试准备
- 训练回答思路，而不是背诵标准答案

## 支持方向

- Java 后端
- AI / 大模型应用
- 前端
- Android
- 数据开发
- AI 产品、产品助理等偏技术产品岗位

## 安装

将本仓库放到 Codex skills 目录中，例如：

```bash
mkdir -p ~/.agents/skills
git clone git@github.com:Benson7zhang/jd-interview-question-generato.git ~/.agents/skills/jd-interview-question-generator
```

然后在 Codex 中使用：

```text
Use $jd-interview-question-generator 根据下面这个 JD 模拟一场一面：

[粘贴岗位 JD]
```

## 示例用法

```text
Use $jd-interview-question-generator

我准备投一个 AI 应用开发实习岗位，帮我根据这个 JD 模拟一场一面，最好像大厂面试官一样追问。

JD：
参与 AI Web 产品开发，熟悉 Vue、TypeScript、MySQL、RESTful API，了解 LangChain、RAG、AI API 调用，有项目经验优先。
```

## 输出风格

默认会输出：

- 岗位方向
- 岗位级别
- 核心技术
- 隐藏考点
- 5-8 个核心面试问题
- 每个问题的优秀候选人回答方向
- 连续追问
- 面试官真实考察点

输出会尽量保持真实面试感，避免堆砌低质量概念题。

## 免责声明

本项目用于面试准备和学习训练，不代表任何公司的真实题库、官方面试标准或招聘结论。

## License

MIT
