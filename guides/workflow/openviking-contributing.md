# 给 OpenViking 贡献改动

本页是入门导读，不是新的项目制度。规则核对基于上游 `feat/vika` 的 `a6c43c1310470e83c77d32b0660a20ea2ef77056`，核对日期 2026-11-08。提交前再看目标分支的最新文件。

- [上游 CONTRIBUTING](https://github.com/volcengine/OpenViking/blob/feat/vika/CONTRIBUTING.md)
- [本次核对的固定版本](https://github.com/volcengine/OpenViking/blob/a6c43c1310470e83c77d32b0660a20ea2ef77056/CONTRIBUTING.md)
- [中文贡献指南](https://github.com/volcengine/OpenViking/blob/feat/vika/docs/repository/CONTRIBUTING_CN.md)
- [安全问题报告方式](https://github.com/volcengine/OpenViking/blob/feat/vika/SECURITY.md)

## 找准问题和目标分支

先搜已有 Issue、PR 和代码。Bug 尽量从真实入口复现，记录版本、步骤、预期和实际结果，再定位负责该行为的模块。涉及公共接口、配置、持久化、身份边界、异步生命周期或大规模重构时，先提设计讨论。

通用贡献指南以最新 `main` 起步，并要求投向合适分支。Vika 当前在 `feat/vika` 开发，Vika 改动应先确认维护者指定的基线；不要从 `main` 开始后把整条功能分支带入 PR。`vika-win` 是下游适配分支的例子，不是所有贡献者都应使用的分支。

目标一定同时核对仓库和分支：向自己的 fork 提 PR，不会自动成为上游 PR。

## 在独立工作分支改一个完整问题

以下示例假定你已 clone 自己的 fork，`origin` 指向自己的仓库，`upstream` 指向 `volcengine/OpenViking`。若名称不同，按实际地址调整，不要覆盖已有 remote。

```bash
git status
git remote -v
git fetch upstream
git switch -c fix/my-focused-change upstream/feat/vika
```

工作区有未保存改动时先处理，不能直接强制切换。修改后运行该组件适用的检查，阅读完整 diff，只暂存本次相关文件，再提交、推送。分支名只是示例。

```bash
git diff --check
git diff
# git add 后跟本次实际修改的文件路径
git diff --cached
git commit -m "fix(vika): describe the observable fix"
git push -u origin fix/my-focused-change
```

到 GitHub 创建 PR：base 仓库选 `volcengine/OpenViking`，base 分支确认 `feat/vika`，head 选择自己的工作分支。草稿 PR 可以提前征求反馈。

## 上游对改动的要求

一个 PR 解决一个连贯问题。行为放在负责它的模块，复用现有规则，避免平行机制、臆测性的兼容分支和与任务无关的重构；替换实现时清掉被替代的代码。

100 行以内通常更容易优先审查，200 行以内优于更大的 PR。这是优先级，不是硬上限，也不是响应时限。计算的是手写源码、测试和文档的新增行加删除行；评估时排除生成文件、vendor 和 lockfile。不要为了压行数丢掉必要验证，也不要拆出无法独立正确工作的半成品。

提交信息和 PR 标题使用 Conventional Commits，例如 `fix(vika): ...`、`docs: ...`。PR 按模板写清修改前后行为、根因与真实路径、影响模块、兼容性、实际验证命令。Human Involvement 如实填写，使用 AI 不免除作者理解和验证代码的责任。

## 验证要证明什么

验证受影响的公开行为和重要失败边界，优先复用有价值的契约测试。上游不要求每个小修改都新增测试文件，但必须解释如何验证。临时诊断、复现和压力脚本按上游约定放 `test_scripts/`。

Python 使用对应路径的 Ruff、mypy 和必要 pytest；其他组件按本组件 README/package manifest 执行。Vika 的检查命令可查 `vika/package.json`，不要把 Python 全量测试当作 Vika 验收。Windows 修改还应检查真实 Windows 入口，并确认 macOS/Linux 原行为未被破坏。

报告中区分通过、失败、未测及原因。CI 绿灯是要求之一，不能替代作者验证与维护者审查。机器权限、runtime、实际安装版本不同，结果也不能直接互相代替。

安全边界包括：不把不可信输入拼成命令，约束实际文件访问和身份权限，明确隔离执行环境。工作目录或提示词不等于沙箱。疑似安全漏洞按 SECURITY.md 私下报告，公开资料不放未修复利用细节、密钥或私人日志。

## 找谁审查，什么时候算完成

按 CONTRIBUTING 的模块表找相关 reviewer，不要所有维护者一起 @。本次核对版本中 Vika 对应 `@krsish`；它是协作路由参考，不是永久、排他的所有权声明，后续以最新文件为准。

逐条处理 review：改了就给对应提交与验证；不同意就解释原因，不要只回复“已处理”。被指出的问题修复后重新检查相关行为。由有权限的维护者依据分支保护和审查结果合并，贡献者不能用自己的 LGTM 替代批准。

Issue 与 PR 也不是同一件事：PR 合并代表代码进入指定分支，不等于已发布或实机验收。只有问题确实解决才关闭；未测、部分修复、仍需证据要说清。GitHub 自动关闭关联 Issue 还受目标分支等条件影响，不要假定向非默认分支合并后一定自动关闭。

合并后清理自己已完成的短期分支前，确认没有未合并工作或其他人依赖。长期适配分支和验收基线不要作为“清理分支”顺手删掉。
