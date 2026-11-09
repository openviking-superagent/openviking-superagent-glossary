# OpenViking SuperAgent 术语表

给刚接触开源、Agent 和软件开发的朋友看的“大白话词典”。遇到 `cc`、`btw`、`LGTM` 不必猜，也不必觉得自己是行业外。

这是社区维护的术语表，不是 OpenViking 官方规范。首版整理自维护者目前可见的社区讨论，不代表已穷尽全部历史消息。只发布通用解释和改写示例，不发布聊天记录、成员身份或私人配置。

更新日期：2026-11-09。大小写通常不改变聊天缩写的意思，但具体含义必须看上下文。示例均为编写示例，不是成员原话。

## 按场景阅读

| 领域 | 入口 | 解决什么问题 |
|---|---|---|
| 流程 | [GitHub Flow](guides/workflow/github-flow.md)、[OpenViking 协作规则](guides/workflow/openviking-contributing.md) | 怎么从一个问题走到 PR 合入，Git Flow 仅作补充 |
| 沟通 | [术语与缩写](guides/communication/terms.md)、[职场黑话](guides/communication/workplace-language.md) | 看懂别人说什么，把要求讲具体 |
| 工具 | [Git 日常使用](guides/tools/git-daily.md) | 查改动、开分支、同步上游、处理冲突和撤销 |

技术词典继续保留在下方，完整目录见 [学习入口](guides/README.md)。

## 沟通

[术语与缩写](guides/communication/terms.md)：cc、btw、LGTM、FYI、ASAP、TL;DR 等。

[职场黑话翻译](guides/communication/workplace-language.md)：对齐、颗粒度、闭环等，以及怎样换成具体要求。

## Agent 和模型

| 写法 | 英文或来源 | 大白话 | 例子 / 容易误解的地方 |
|---|---|---|---|
| AI | Artificial Intelligence | 人工智能 | 大模型是 AI 技术的一类 |
| LLM | Large Language Model | 大语言模型 | 主要处理语言相关任务；不等于整个 Agent 系统 |
| VLM | Vision-Language Model | 能处理图像和语言的模型 | 能看图，不代表任意模型接口都能传图片 |
| RAG | Retrieval-Augmented Generation | 先查资料，再让模型结合资料回答 | 不等于重新训练模型 |
| A2A | Agent to Agent | 智能体之间协作、交换任务或信息 | 泛指协作时，不代表已使用某个具体 A2A 协议 |
| MCP | Model Context Protocol | AI 应用连接工具、资料等外部能力的协议 | [官方介绍](https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro)；不是模型本身 |
| ACP | Agent Client Protocol | 编辑器或客户端与编程 Agent 沟通的协议 | [官方介绍](https://agentclientprotocol.com/get-started/introduction)；这里指 Agent Client Protocol，不是所有同名缩写 |
| SDK | Software Development Kit | 给其他程序使用的开发工具包 | `SDK 模式` 通常意味着让程序接入；具体能力取决于项目 |
| OV | OpenViking | 本社区讨论的 OpenViking 项目 | [项目仓库](https://github.com/volcengine/OpenViking) |
| OVSA | OpenViking SuperAgent | OpenViking SuperAgent 的社区简称 | Vika 也是其名称，不需要硬拆成英文首字母 |
| DSH | DeepSeek Harness | DeepSeek 的 Agent harness 项目 | [项目仓库](https://github.com/deepseek-ai/deepseek-harness)；不等于 pi-durable |
| dpsk | DeepSeek 的非正式省写 | 聊天时少打几个字 | 不是精确模型 ID，不能据此判断模型版本 |
| TPS | Tokens Per Second（模型生成语境） | 每秒生成多少 token | 数据库里也可能指 Transactions Per Second，不能混用 |

## 程序接口、数据和页面

| 写法 | 英文或来源 | 大白话 | 例子 / 容易误解的地方 |
|---|---|---|---|
| API | Application Programming Interface | 程序之间调用功能的接口 | 有 API 不等于当前账号有调用权限 |
| CLI | Command-Line Interface | 在终端敲命令使用的界面 | `ov`、`gh` 都是命令行工具 |
| UI | User Interface | 用户界面 | 按钮、页面、交互布局等 |
| GUI | Graphical User Interface | 图形界面 | 和纯命令行界面相对 |
| IM | Instant Messaging | 即时通信 | 飞书、Slack 之类的聊天渠道 |
| JSON | JavaScript Object Notation | 一种结构化数据格式 | JSON 对象和“内容看起来像 JSON 的字符串”不是同一类型 |
| JSONL | JSON Lines | 每一行各放一条 JSON 数据 | 常用来存逐条事件或记录 |
| RPC | Remote Procedure Call | 像调用函数一样请求另一端办事 | 不一定经过公网，也可以在本机进程之间通信 |
| JSON-RPC | 基于 JSON 的 RPC 协议 | 用 JSON 表达请求、结果和错误 | 不是“任何 JSON 请求”都符合这个协议 |
| HTTP | Hypertext Transfer Protocol | 常用的网络请求协议 | URL 用 `http://` 开头不等于请求有加密 |
| HTTPS | HTTP over TLS | 使用 TLS 保护传输的 HTTP | 仍需校验服务器证书 |
| URL | Uniform Resource Locator | 资源地址 | 网页链接是一种常见 URL |
| URI | Uniform Resource Identifier | 资源标识符 | 比 URL 概念更广，如系统中的资源标识 |
| HTML | HyperText Markup Language | 描述网页结构的标记语言 | 不是图片格式 |
| CSS | Cascading Style Sheets | 控制网页样式 | 字体、颜色、布局等 |
| MD / .md | Markdown | 用简单文本标记写文档的格式 | 中文聊天里的同字母感叹词未必指 Markdown |
| PNG | Portable Network Graphics | 常见无损图片格式 | 放大低分辨率原图不等于补回真实细节 |

## 部署、权限和工程

| 写法 | 英文或来源 | 大白话 | 例子 / 容易误解的地方 |
|---|---|---|---|
| CI | Continuous Integration | 每次改代码后自动检查、测试、构建 | CI 绿了不代表所有真实使用场景都测过 |
| TOS / tos | Torch Object Storage；部分官方资料也写 Tinder Object Storage | 火山引擎的对象存储服务，用来保存安装包、图片、备份等文件，并按权限提供下载 | 例如把发布包放到 TOS，安装脚本从下载地址取包；上传本身不会自动生成一键安装流程，也不代表文件默认公开。见[官方产品文档](https://docs.volcengine.com/docs/torch-object-storage?lang=zh)；这里不是 Terms of Service（服务条款） |
| K8s | Kubernetes：K 与 s 之间省去 8 个字母 | 管理容器化应用的平台 | 不是 Windows 系统的别称 |
| ACL | Access Control List | 谁能访问什么的权限清单 | 文件 ACL、业务资源 ACL 不是同一个配置入口 |
| ACE | Access Control Entry | ACL 中的一条权限记录 | 可表示允许或拒绝某个主体的某项权限 |
| DACL | Discretionary Access Control List | Windows 中决定允许或拒绝访问的列表 | 与审计用 SACL 区别开 |
| SACL | System Access Control List | Windows 中用于审计等系统安全信息的列表 | 更改相关内容可能需要额外权限 |
| UAC | User Account Control | Windows 的提权确认机制 | 普通终端与管理员终端权限不同 |
| TLS | Transport Layer Security | 保护网络传输的安全协议 | 私有 CA、自签名证书涉及信任配置 |
| CA | Certificate Authority | 签发证书的机构或信任体系角色 | 不要和证书本身混为一谈 |
| OAuth | OAuth 授权框架名称 | 让应用获得用户授权的机制 | 不硬编首字母全称；OAuth 本身不是完整身份认证协议 |
| PID | Proportional–Integral–Derivative（控制工程） | 比例、积分、微分控制 | 在操作系统语境中又常指 Process ID，进程编号 |
| SLDD / .sldd | Simulink Data Dictionary | Simulink 的数据字典文件 | 常用于保存模型数据定义；不是普通 Markdown |

## 常被当成缩写，其实是普通术语

| 词 | 大白话 |
|---|---|
| Agent | 能围绕任务调用工具、执行步骤的智能体 |
| harness | 组织模型、工具、会话与执行过程的运行框架 |
| runtime | 实际运行 Agent 的执行环境或引擎；具体指代看项目 |
| Skill | 一组任务方法、说明及配套资源；不是缩写 |
| hook | 在某个运行阶段插入处理逻辑的挂钩 |
| profile | 一套配置；不同 profile 不一定启用相同插件 |
| headless | 不带交互图形界面的运行方式；是否常驻由项目决定 |
| session | 会话，用来组织连续交互和状态 |
| steer | 给正在进行的任务追加输入或调整方向，行为取决于 runtime |
| fork | 从别人的仓库派生出自己名下的仓库 |
| branch | 分支，同一仓库中的一条开发线 |
| commit | 一次记录在 Git 中的改动快照 |
| diff | 两个版本之间的差异 |
| merge | 合并分支或改动 |
| rebase | 变基：把当前分支的一串提交，依次重新应用到另一条分支的新起点上。例如把 Windows 适配改动接到最新上游之后；可能需要解决冲突，重放的提交通常会产生新的 commit ID。对别人也在用的共享分支，不要未经协调直接 rebase 后强推 |
| worktree | 给一个 Git 仓库开另一个工作目录，可检出另一分支 |
| issue | 用来记录问题、需求或讨论的条目 |
| owner | 对某个模块负责的人；不等于 GitHub 仓库所有者 |
| token | 模型处理文本的单位；在鉴权语境又可指访问凭据，需分清 |

## 社区简称与版本简称

| 写法 | 对应名称 | 大白话 / 使用边界 |
|---|---|---|
| MA | 火山方舟 Managed Agents | 火山引擎的托管 Agent 服务，管理 Agent 配置、会话、工具调用和运行环境。见[官方概述](https://docs.volcengine.com/docs/ark/overview?lang=en)及[官方更新记录中的 MA 用法](https://console.volcengine.com/ark/region%3Acn-beijing/docs/product-update-announcements)；不是某个模型的名称 |
| OCG | OpenCode Go | 本社区用于指 OpenCode Go 模型套餐的简称；根据社区补充确认，不代表套餐中所有模型都是同一个版本 |
| 1017 | DeepSeek v4.1 Flash 的 1017 版本（本社区语境） | 根据社区补充确认的版本简称，不是完整 API 模型 ID，也不是官方版本信息的独立核验；排障时仍需提供实际通道和完整模型 ID，不能套用到其他模型或日期 |

## 如何补词

参见 [贡献说明](CONTRIBUTING.md)。有新写法时先确认意思：已有缩写的新含义补充到原条目；真正的新缩写增加一行；不确定的先列为待澄清。不要把玩笑或某个人的一次说法写成行业标准。

欢迎通过 Issue 或 PR 补充。更新在维护者实际收到相关消息并确认含义后进行；本仓库没有监听或采集群聊的后台程序，不保证实时自动更新。

文档采用 [MIT License](LICENSE)。
