# 以 GitHub Flow 理解 OpenViking 协作

Git 是记录代码历史的工具，GitHub 是托管仓库与审查改动的平台；Flow 是团队约定的协作流程，不是必须安装的软件。

## 先用 GitHub Flow 理解一次贡献

在目标分支上开一个短期分支，修改并提交，推送到自己的仓库，提 PR 请人审查。根据反馈继续提交，检查通过且获得批准后合并，最后清理已完成的短期分支。不同问题分开做，不要让一个小修复夹带另一项重构。

这是 [GitHub 官方介绍的轻量流程](https://docs.github.com/en/get-started/using-github/github-flow)。实际项目可以指定其他集成分支，不必每次都向 `main` 提交。

```mermaid
flowchart LR
  A[确认目标分支] --> B[新建工作分支]
  B --> C[修改与验证]
  C --> D[推送并提 PR]
  D --> E[审查与修改]
  E --> F[通过后合并]
```

## Git Flow 多了什么

传统 Git Flow 保留稳定分支 `main`（原文叫 `master`）与开发分支 `develop`，另外使用功能分支、发布准备分支和紧急修复分支。它适合需要组织版本发布、多版本维护的团队，但分支更多，同步也更复杂。

[提出者的原文及后续说明](https://nvie.com/posts/a-successful-git-branching-model/)明确提醒：不要把它当万能标准，持续交付项目可以选择更简单的 GitHub Flow。OpenViking 有功能分支，不代表它采用完整 Git Flow；不要自行创建 `develop` 或改变项目发版流程。

## 在 OpenViking 里怎么用

按“工作分支 → PR → 审查 → 合并”的主线学习，再落实到[OpenViking 贡献规则](openviking-contributing.md)。这里用 GitHub Flow 解释日常协作，不把所有长期分支或发版操作都归成一套固定模型。

准备 PR 时确认 base 仓库、base 分支、head 分支。修改还未完成可以开 Draft；审查意见在同一 PR 下逐条回应，修复后推送同一分支即可更新 PR。CI 失败先看日志，不能通过删除相关检查来换绿灯。批准、合并、发布是不同状态，报告时分别说清。

具体命令见[Git 日常使用](../tools/git-daily.md)，缩写见[沟通术语](../communication/terms.md)。
