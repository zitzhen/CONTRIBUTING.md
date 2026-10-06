# Contributing to ZIT Studio

**🌐 语言：** [English](CONTRIBUTING.md) · **简体中文** · [繁體中文](CONTRIBUTING.zh-Hant.md)

感谢您对 **ZIT Studio** 项目的关注与贡献！🎉

我们欢迎通过 **GitHub Pull Request** 或 **电子邮件列表（Mailing List）** 提交代码、文档、修复和其他改进。

在参与贡献之前，请阅读并遵守：

- 本项目的 `LICENSE` 文件
- [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)
- 项目仓库中的其他贡献指南或开发文档

> **安全漏洞请勿通过 GitHub Issue、Pull Request 或电子邮件列表公开提交。**
> 请按照项目提供的安全漏洞报告流程进行报告。

---

## 1. GitHub Pull Request

如果您拥有 GitHub 账号，我们推荐使用 **Pull Request（PR）** 提交贡献。

### 基本流程

1. Fork 本项目仓库。
2. 创建用于修改的分支。
3. 完成您的修改。
4. 在本地测试您的修改。
5. 提交 Git commit。
6. 将分支推送到您的 Fork。
7. 创建 Pull Request。
8. 等待 Maintainer 审核。

请尽量保持每个 Pull Request 的目的明确。

例如：

- 一个 Bug 修复对应一个 PR
- 一个功能对应一个 PR
- 不相关的格式化或重构不要与其他修改混在同一个 PR 中

### Commit

请尽量使用清晰、简洁且具有描述性的 commit message。

如果一个修改可以拆分成多个逻辑独立的 commit，我们鼓励保持这些 commit 的独立性。

Maintainer 可能会要求您修改、压缩（squash）或重新整理 commit。

---

## 2. 电子邮件列表

ZIT Studio 同时支持通过电子邮件列表提交贡献。

这意味着：

> **您不需要拥有 GitHub 账号，也可以向 ZIT Studio 的项目提交代码。**

我们的代码贡献邮件列表：

**zit-studio-code@googlegroups.com**

[ZIT Studio Code Mailing List](https://groups.google.com/g/zit-studio-code?utm_source=chatgpt.com)

您可以通过电子邮件发送 Git patch、代码审查请求以及其他与代码贡献相关的内容。

### 2.1 提交补丁

在发送补丁之前，请先确认：

- 您的修改符合本项目的贡献指南。
- 您的修改符合项目所使用的许可证。
- 您没有提交与项目许可证不兼容的代码或其他受限制的内容。
- 您已经在本地完成必要的测试。
- 您没有在邮件列表中公开提交安全漏洞。

如果您知道相关项目的 Maintainer，可以直接将邮件发送给对应的 Maintainer，并将：

`zit-studio-code@googlegroups.com`

加入收件人或抄送列表。

如果您不知道应该联系哪位 Maintainer，可以直接联系：

**Oliver Lin — <oliver@liuxiaozhen.dev>**

---

## 3. 邮件补丁格式

我们推荐使用 Git 原生的邮件补丁工作流，例如：

```bash
git format-patch
git send-email
```

邮件补丁应尽可能保留 Git commit 的完整信息，包括：

- Author
- Commit message
- Commit body
- Patch
- Signed-off-by（如果项目要求）

如果项目另有具体要求，请以项目仓库中的说明为准。

---

## 4. 邮件主题

为了方便邮件列表中的成员识别和处理补丁，请在邮件主题中包含：

```text
[repository-name]
```

例如：

```text
[patchsplit] Add GitLab patch support
```

或者：

```text
[CoCo-Community] Fix XSS sanitization
```

如果您使用 `git format-patch` 或 `git send-email`，请尽量保持 Git 自动生成的 patch 信息，不要手动破坏其格式。

---

## 5. 邮件格式

提交代码补丁时，请优先使用 **纯文本（Plain Text）**。

请避免发送仅包含 HTML 格式的补丁，因为 HTML 邮件可能影响 Git 对邮件补丁的识别和处理。

### 回复邮件

回复邮件时：

- 请勿附带完整的上一封邮件原文。
- 请勿复制客户端生成的完整 HTML 内容。
- 如有必要，请使用 `>` 引用之前的内容。
- 请尽量只引用与当前回复相关的部分。

例如：

```text
> This patch needs additional tests.

Added the missing tests in the new commit.
```

请避免：

```text
> > > > > > > > > > > > > > > > > > > > >
> 大量完整的历史邮件内容……
> 大量完整的历史邮件内容……
> 大量完整的历史邮件内容……
```

这样可以减少邮件列表中的噪音，并方便其他 Contributors 阅读和审查。

---

## 6. GitHub 与 Mailing List 的关系

GitHub Pull Request 和电子邮件列表是 **两种等价的贡献入口**。

您可以根据自己的情况选择：

| 方式 | 是否需要 GitHub 账号 | 推荐场景 |
| --- | --- | --- |
| GitHub Pull Request | 是 | 普通开发、代码审查 |
| Email Mailing List | 否 | 邮件工作流、没有 GitHub 账号的 Contributors |

通过邮件列表提交的补丁同样会经过 Maintainer 的审核。

Maintainer 可以要求 Contributor：

- 修改补丁
- 补充测试
- 修改 commit message
- 拆分或合并 commit
- 重新发送 patch
- 通过 GitHub Pull Request 提交后续修改

---

## 7. Code Review

所有代码贡献都需要经过适当的审核。

Maintainer 可能会从以下方面进行检查：

- 功能是否正确
- 是否存在明显 Bug
- 是否存在安全问题
- 是否有足够的测试
- 代码是否符合项目风格
- API 或行为是否保持兼容
- 依赖及许可证是否合适
- commit 历史是否清晰

提交贡献并不意味着贡献一定会被接受。

Maintainer 有权要求修改或拒绝不符合项目目标、质量标准或许可证要求的贡献。

---

## 8. 许可证与版权

提交贡献时，您必须确保自己有权提交这些内容。

除非项目另有说明，您提交的代码应当能够在本项目所使用的许可证下合法分发。

请勿提交：

- 未经授权的第三方代码
- 与项目许可证不兼容的代码
- 从其他项目复制但没有确认许可证兼容性的代码
- 您没有权利重新分发的资源

如果您的贡献包含第三方代码，请在提交前确认其许可证以及与本项目许可证的兼容性，并按照相应许可证要求保留必要的版权及许可证声明。

---

## 9. Developer Certificate of Origin

如果项目要求 Developer Certificate of Origin（DCO），请在 commit 中添加：

```text
Signed-off-by: Your Name <your@email.example>
```

例如：

```bash
git commit -s -m "Add GitLab patch support"
```

如果具体项目启用了 DCO，请以该项目的要求为准。

---

## 10. 安全问题

**请勿通过以下公开渠道报告安全漏洞：**

- GitHub Issues
- GitHub Pull Requests
- Mailing List
- 公开的项目讨论区

安全漏洞应通过项目提供的安全报告渠道进行报告。

如果您不确定应该向哪里报告安全问题，请先联系项目 Maintainer，而不要将漏洞细节公开发布。

---

## 11. 行为准则

所有 Contributors、Maintainers 和其他社区成员都必须遵守：

**Contributor Covenant Code of Conduct**

我们希望 ZIT Studio 成为一个开放、友善、尊重且适合协作的开源社区。

---

## 12. 联系方式

### Code Mailing List

**zit-studio-code@googlegroups.com**

[Google Groups — ZIT Studio Code](https://groups.google.com/g/zit-studio-code?utm_source=chatgpt.com)

### Maintainer

**Oliver Lin**

<oliver@liuxiaozhen.dev>

---

感谢您的贡献！❤️

无论您通过 GitHub Pull Request 还是电子邮件列表参与，我们都非常欢迎您的贡献。

**ZIT Studio**

05 October 2026
