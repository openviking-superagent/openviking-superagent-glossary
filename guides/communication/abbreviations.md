# 缩写速查

群里看到不认识的英文缩写，按字母找就行。这里收的是聊天和社区里真出现过的写法，含义确认过才进表；全称拿不准的宁可不收，也不猜一个上去。

大小写一般不改变意思，具体指什么还得看上下文。技术名词（TLS、JSON、K8s 这类）不在这里，见[根目录术语表的各领域表格](../../README.md)；礼貌用法和改写示例见[术语与缩写](terms.md)。

| 缩写 | 全称 | 出现场景 |
|---|---|---|
| ACK | Acknowledgement，确认收到 | 别人安排事情后回一句，表示“看到了”；不等于已经做完 |
| ACL | Access Control List，访问控制清单 | 讨论谁能访问哪些知识库、资源时；文件系统的 ACL 和业务资源的 ACL 不是同一个配置入口 |
| anw | anyway，反正、随便 | 讨论跑偏后接回正题，或表示“这个不重要”；不是人名，也不是某个工具 |
| API | Application Programming Interface，程序调用接口 | 说“调接口”“走消息接口”时；有 API 不等于当前账号有调用权限 |
| ASAP | As Soon As Possible，尽快 | 催一件事，但没给具体时间；要排期还是得问清截止时间 |
| btw | By The Way，顺便说一句 | 补充一个旁支话题，通常不要求别人处理 |
| cc | Carbon Copy，抄送 | `cc 某人`是让他也知道，不等于把任务交给他；同一段里聊编程 Agent 时，CC 也可能指 Claude Code |
| CI | Continuous Integration，持续集成 | “CI 绿了”“CI 挂了”指自动检查、测试、构建的结果；绿了不代表真实场景都测过 |
| CLI | Command-Line Interface，命令行界面 | 说 `ov`、`gh` 这类命令时；和图形界面相对 |
| CR | Code Review，代码审查 | 请人看改动、约 CR 时；有 CR 意见不等于已经改完 |
| DSH | DeepSeek Harness | 讨论 worker runtime、Agent 执行框架时；和 pi、Codex 是并列的可选运行方式，会话和缓存行为各不一样 |
| dpsk | DeepSeek 的非正式省写 | 聊模型、对比体验时；不是精确模型 ID，不能据此判断版本 |
| ETA | Estimated Time of Arrival，预计完成时间 | 问“多久能好”时；是估计，不是承诺 |
| FYI | For Your Information，供你了解 | 转一条信息，通常不要求行动；要对方做事请直接写任务 |
| LGTM | Looks Good To Me，我看着没问题 | 代码评审里表示认可；不等于已经合并，也不替代仓库要求的正式审查 |
| LLM | Large Language Model，大语言模型 | 聊模型能力、上下文、生成类任务时；不等于整个 Agent 系统 |
| MA | 火山方舟 Managed Agents | 讨论托管 Agent 服务时；是服务名，不是模型名 |
| MCP | Model Context Protocol | 给 Agent 接工具、资料时；是协议，不是模型 |
| mk2 | 没有确认的通用全称，社区里当某个工具或机器人的代称用 | 群里提到那个机器人或它的产出时；具体指哪个只能看上下文，不要照字面猜 |
| OCG | OpenCode Go，模型套餐的社区简称 | 讨论 OpenCode 套餐时；不代表套餐里所有模型都是同一个版本 |
| OV | OpenViking | 几乎每条项目相关讨论都会出现 |
| ovpack | OVPack，OpenViking 的可恢复内容包 | 讨论导出、迁移、备份知识库时；是数据快照不是安装包，导入会校验 manifest 和 checksum |
| OVSA | OpenViking SuperAgent | 说“参考 ovsa”“sa 那边的 worker”时；Vika 也是它的名字 |
| PR | Pull Request | 提改动、请人 review 时；提 PR 不等于合并 PR |
| RAG | Retrieval-Augmented Generation，检索增强生成 | 讨论召回效果、知识库检索时；不等于重新训练模型 |
| RFC | Request for Comments，征求意见稿 | 先写方案让大家提意见时；某份 RFC 是不是正式标准要看它的状态 |
| SA | SuperAgent，指 OpenViking SuperAgent | “新的 sa harness”“sa 那边”；这个社区里基本都指它，不是 Service Agreement |
| SDK | Software Development Kit，开发工具包 | 说“SDK 模式”“接 SDK”时；具体能力取决于项目 |
| TL;DR | Too Long; Didn't Read，长文摘要 | 长文开头给一句话结论；单独回别人一句 TL;DR 容易被当成不想读 |
| TOS | Torch Object Storage，火山引擎对象存储 | 把安装包、图片放上去，让脚本从下载地址取包时；不是 Terms of Service（服务条款） |
| TPS | Tokens Per Second，每秒生成多少 token | 比较模型速度时；数据库语境里也可能指每秒事务数，别混用 |
| WIP | Work In Progress，还在做 | 说改动还没完成、先别验收时；不等于可以反复改口 |

## 怎么补一条

看到新的缩写，先确认含义再加，一行一个：

1. 问清楚或者查到全称，拿不准就先放着，别按字面猜。
2. 在表里按字母序插一行，三列写全：缩写、全称、出现场景。出现场景写“在什么讨论里会看到它”，不写谁在哪天说过。
3. 同一个写法有新含义时，在原行补一句语境区分，不另起一行同名条目。

不加人名、群号、聊天原文、消息链接和内部地址，解释通用写法不需要这些。改动提 PR 或 issue 都行，格式见[贡献说明](../../CONTRIBUTING.md)。
