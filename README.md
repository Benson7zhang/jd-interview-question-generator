# Intern Interview Predictor

Intern Interview Predictor 是一个 Codex Skill。

这个 Skill 面向实习、校招、应届和初级技术岗位。它会根据岗位 JD、简历内容和项目经历，分析面试官可能关注的问题。它也会指出简历中的风险点。

这个 Skill 不代表任何公司的真实题库。它只用于面试准备。

## 它能做什么

这个 Skill 可以帮助你完成这些事：

- 分析岗位 JD 中的核心要求。
- 分析简历和 JD 的匹配程度。
- 预测常见面试阶段。
- 生成更可能被问到的问题。
- 生成项目深挖问题。
- 找出候选人可能被追问的风险点。
- 给出准备面试时需要优先补强的内容。

## 它适合哪些场景

这个 Skill 适合这些情况：

- 你准备投递实习岗位。
- 你准备参加校招面试。
- 你想根据 JD 准备一面或二面。
- 你想知道简历中哪些项目最容易被追问。
- 你想检查自己的项目描述是否可信。

## 它会关注哪些信息

这个 Skill 会重点看这些内容：

- JD 中写到的技术栈。
- JD 中暗含的能力要求。
- 简历中的项目经历。
- 简历中的个人贡献。
- 简历中的数据和结果。
- 项目是否有真实细节。
- 项目是否有过度包装的风险。

## 安装方式

推荐使用 `npx skills` 安装。

Codex：

```bash
npx skills add https://github.com/Benson7zhang/intern-interview-predictor.git -g --agent codex --skill intern-interview-predictor -y
```

Claude Code：

```bash
npx skills add https://github.com/Benson7zhang/intern-interview-predictor.git -g --agent claude-code --skill intern-interview-predictor -y
```

安装完成后，你需要重启 Codex 或 Claude Code。客户端重启后会重新加载 skills。

## 使用方式

你可以在 Codex 或 Claude Code 中这样使用：

```text
Use $intern-interview-predictor

请根据下面这个 JD 和我的简历，预测实习面试中可能被问到的问题。请重点分析项目真实性风险。

JD：
[粘贴岗位 JD]

简历：
[粘贴简历或项目经历]
```

## 输入建议

这个 Skill 最适合同时读取 JD 和简历。

你可以提供这些内容：

- 岗位名称。
- 岗位职责。
- 任职要求。
- 加分项。
- 教育背景。
- 技术栈。
- 项目经历。
- 实习、比赛或开源经历。

你也可以只提供 JD 或简历。

如果你只提供 JD，这个 Skill 会分析岗位要求和可能问题。

如果你只提供简历，这个 Skill 会分析项目风险和可能追问。

如果你同时提供 JD 和简历，这个 Skill 会分析匹配程度、面试问题和淘汰风险。

## 示例输入

```text
Use $intern-interview-predictor

我准备投一个 AI 应用开发实习岗位。请根据这个 JD 和我的项目经历，预测面试中可能被问到的问题。请重点看项目真实性。

JD：
- 参与 AI Web 产品开发。
- 熟悉 Vue、TypeScript 和 RESTful API。
- 熟悉 MySQL。
- 了解 LangChain、RAG 和 AI API 调用。
- 有完整项目经验者优先。

简历：
- 我做过一个 RAG 知识库项目。
- 项目使用 LangChain、OpenAI API、向量数据库和 Vue。
- 项目支持文档上传、文本切分、向量检索和问答页面。
- 简历中写到“优化检索准确率并降低响应延迟”。
- 项目目前是个人 Demo。
```

## 可能的输出内容

这个 Skill 可能会输出这些内容：

- JD 信号分析。
- 简历信号分析。
- JD 和简历的匹配分析。
- 面试阶段预测。
- 高概率问题。
- 项目深挖问题。
- 风险点分析。
- 准备建议。

输出内容会根据输入变化。输入越具体，分析越具体。

## 注意事项

这个项目只提供面试准备参考。它不能保证预测结果一定出现。它也不能代表任何公司的官方面试标准。

如果输入信息很少，这个 Skill 会做一些合理推断。你需要自行判断这些推断是否适合你的情况。

## License

MIT
