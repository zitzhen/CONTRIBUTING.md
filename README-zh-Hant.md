# 貢獻至 ZIT Studio

**🌐 語言：** [English](CONTRIBUTING.md) · [简体中文](CONTRIBUTING.zh-Hans.md) · **繁體中文**

感謝您對 **ZIT Studio** 專案的關注與貢獻！🎉

我們歡迎透過 **GitHub Pull Request** 或 **電子郵件論壇（Mailing List）** 提交程式碼、文件、修正和其他改進。

在參與貢獻之前，請閱讀並遵守：

- 本專案的 `LICENSE` 檔案
- [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)
- 專案儲存庫中的其他貢獻指南或開發文件

> **安全性漏洞請勿透過 GitHub Issue、Pull Request 或電子郵件論壇公開提交。**
> 請依照專案提供的安全性漏洞回報流程進行回報。

---

## 1. GitHub Pull Request

如果您擁有 GitHub 帳號，我們推薦使用 **Pull Request（PR）** 提交貢獻。

### 基本流程

1. Fork 本專案儲存庫。
2. 建立用於修改的分支。
3. 完成您的修改。
4. 在本機測試您的修改。
5. 提交 Git commit。
6. 將分支推送到您的 Fork。
7. 建立 Pull Request。
8. 等待 Maintainer 審核。

請盡量保持每個 Pull Request 的目的明確。

例如：

- 一個 Bug 修正對應一個 PR
- 一個功能對應一個 PR
- 不相關的格式化或重構不要與其他修改混在同一個 PR 中

### Commit

請盡量使用清晰、簡潔且具描述性的 commit message。

如果一個修改可以拆分成多個邏輯獨立的 commit，我們鼓勵保持這些 commit 的獨立性。

Maintainer 可能會要求您修改、壓縮（squash）或重新整理 commit。

---

## 2. 電子郵件論壇

ZIT Studio 同時支援透過電子郵件論壇提交貢獻。

這意味著：

> **您不需要擁有 GitHub 帳號，也可以向 ZIT Studio 的專案提交程式碼。**

我們的程式碼貢獻郵件論壇：

**zit-studio-code@googlegroups.com**

[ZIT Studio Code Mailing List](https://groups.google.com/g/zit-studio-code?utm_source=chatgpt.com)

您可以透過電子郵件傳送 Git patch、程式碼審查請求，以及其他與程式碼貢獻相關的內容。

### 2.1 提交修補程式

在傳送修補程式之前，請先確認：

- 您的修改符合本專案的貢獻指南。
- 您的修改符合專案所使用的授權條款。
- 您沒有提交與專案授權條款不相容的程式碼或其他受限制的內容。
- 您已在本機完成必要的測試。
- 您沒有在電子郵件論壇中公開提交安全性漏洞。

如果您知道相關專案的 Maintainer，可以直接將郵件傳送給對應的 Maintainer，並將：

`zit-studio-code@googlegroups.com`

加入收件者或副本（Cc）清單。

如果您不知道應該聯絡哪位 Maintainer，可以直接聯絡：

**Oliver Lin — <oliver@liuxiaozhen.dev>**

---

## 3. 郵件修補程式格式

我們推薦使用 Git 原生的郵件修補程式工作流程，例如：

```bash
git format-patch
git send-email
```

郵件修補程式應盡可能保留 Git commit 的完整資訊，包括：

- Author
- Commit message
- Commit body
- Patch
- Signed-off-by（如果專案要求）

如果專案另有具體要求，請以專案儲存庫中的說明為準。

---

## 4. 郵件主旨

為了方便電子郵件論壇中的成員識別和處理修補程式，請在郵件主旨中包含：

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

如果您使用 `git format-patch` 或 `git send-email`，請盡量保持 Git 自動產生的 patch 資訊，不要手動破壞其格式。

---

## 5. 郵件格式

提交程式碼修補程式時，請優先使用 **純文字（Plain Text）**。

請避免傳送僅包含 HTML 格式的修補程式，因為 HTML 郵件可能影響 Git 對郵件修補程式的識別和處理。

### 回覆郵件

回覆郵件時：

- 請勿附上完整的上一封郵件原文。
- 請勿複製郵件用戶端產生的完整 HTML 內容。
- 如有必要，請使用 `>` 引用之前的內容。
- 請盡量只引用與目前回覆相關的部分。

例如：

```text
> This patch needs additional tests.

Added the missing tests in the new commit.
```

請避免：

```text
> > > > > > > > > > > > > > > > > > > > >
> 大量完整的歷史郵件內容……
> 大量完整的歷史郵件內容……
> 大量完整的歷史郵件內容……
```

這樣可以減少電子郵件論壇中的雜訊，並方便其他 Contributors 閱讀和審查。

---

## 6. GitHub 與 Mailing List 的關係

GitHub Pull Request 和電子郵件論壇是 **兩種等價的貢獻入口**。

您可以根據自己的情況選擇：

| 方式 | 是否需要 GitHub 帳號 | 推薦情境 |
| --- | --- | --- |
| GitHub Pull Request | 是 | 一般開發、程式碼審查 |
| Email Mailing List | 否 | 郵件工作流程、沒有 GitHub 帳號的 Contributors |

透過電子郵件論壇提交的修補程式同樣會經過 Maintainer 的審核。

Maintainer 可以要求 Contributor：

- 修改修補程式
- 補充測試
- 修改 commit message
- 拆分或合併 commit
- 重新傳送 patch
- 透過 GitHub Pull Request 提交後續修改

---

## 7. Code Review

所有程式碼貢獻都需要經過適當的審核。

Maintainer 可能會從以下方面進行檢查：

- 功能是否正確
- 是否存在明顯 Bug
- 是否存在安全性問題
- 是否有足夠的測試
- 程式碼是否符合專案風格
- API 或行為是否保持相容
- 相依性及授權條款是否合適
- commit 歷史是否清晰

提交貢獻並不代表貢獻一定會被接受。

Maintainer 有權要求修改或拒絕不符合專案目標、品質標準或授權條款要求的貢獻。

---

## 8. 授權條款與著作權

提交貢獻時，您必須確保自己有權提交這些內容。

除非專案另有說明，您提交的程式碼應當能夠在本專案所使用的授權條款下合法散布。

請勿提交：

- 未經授權的第三方程式碼
- 與專案授權條款不相容的程式碼
- 從其他專案複製但沒有確認授權條款相容性的程式碼
- 您沒有權利重新散布的資源

如果您的貢獻包含第三方程式碼，請在提交前確認其授權條款以及與本專案授權條款的相容性，並依照相應授權條款要求保留必要的著作權及授權聲明。

---

## 9. Developer Certificate of Origin

如果專案要求 Developer Certificate of Origin（DCO），請在 commit 中加入：

```text
Signed-off-by: Your Name <your@email.example>
```

例如：

```bash
git commit -s -m "Add GitLab patch support"
```

如果具體專案啟用了 DCO，請以該專案的要求為準。

---

## 10. 安全性問題

**請勿透過以下公開管道回報安全性漏洞：**

- GitHub Issues
- GitHub Pull Requests
- Mailing List
- 公開的專案討論區

安全性漏洞應透過專案提供的安全性回報管道進行回報。

如果您不確定應該向哪裡回報安全性問題，請先聯絡專案 Maintainer，而不要將漏洞細節公開發布。

---

## 11. 行為準則

所有 Contributors、Maintainers 和其他社群成員都必須遵守：

**Contributor Covenant Code of Conduct**

我們希望 ZIT Studio 成為一個開放、友善、尊重且適合協作的開源社群。

---

## 12. 聯絡方式

### Code Mailing List

**zit-studio-code@googlegroups.com**

[Google Groups — ZIT Studio Code](https://groups.google.com/g/zit-studio-code?utm_source=chatgpt.com)

### Maintainer

**Oliver Lin**

<oliver@liuxiaozhen.dev>

---

感謝您的貢獻！❤️

無論您透過 GitHub Pull Request 還是電子郵件論壇參與，我們都非常歡迎您的貢獻。

**ZIT Studio**

05 October 2026
