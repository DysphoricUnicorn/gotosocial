# Beta 版路线图

本文档包含了 GoToSocial 为其首个正式稳定版本发布而制定的路线图。

文档中的所有信息仅为预测。这为参与开发的人提供了粗略的时间表，但过程中难免会有变动；请不要对文档中的任何事项抱有太强烈的期望！

感谢 [NLnet](https://nlnet.nl) 对 GoToSocial alpha 与 beta 阶段开发的资助！

非常感谢我们所有的 [Open Collective](https://opencollective.com/gotosocial) 和 [Liberapay](https://liberapay.com/gotosocial) 赞助者们，他们的赞助使 GoToSocial 项目能够持续前行！ 💕

## 目录

- [Beta 目标](#beta-目标)
- [时间节点](#时间节点)
  - [2023 年中](#2023-年中)
  - [2023 年中到年底](#2023-年中到年底)
  - [2024 年初](#2024-年初)
  - [BETA 里程碑](#beta-里程碑)
  - [2024 年余下时间至 2025 年初](#2024-年余下时间至-2025-年初)
  - [BETA 发布到稳定版发布期间](#beta-发布到稳定版发布期间)
- [愿望单](#愿望单)

## Beta 目标

每个软件项目对“beta”都有不同的理解。对于我们来说，GoToSocial 的 beta 版本应提供一套与现有流行的 ActivityPub 服务端实现大致相当的功能集。

换句话说，你应该能使用 GoToSocial 的 beta 版本作为你的主要社交实例，关注他人、发布动态，而不会遇到功能缺失或工作不正常的情况。

我们的 beta 目标还包括一些我们认为对用户安全与健康至关重要的功能，如关闭评论区、黑名单订阅、白名单模式支持等。

一旦我们实现了足以使 GoToSocial 进入 “beta” 的功能，我们将利用 beta 阶段来修复漏洞、调整性能，并新增一些需要在稳定基础上实现的额外功能。

我们希望在进入 beta 阶段后，客户端 API 能保持相对稳定，以便开发者能自信地基于 GoToSocial 构建应用，而无需担心 API 发生重大变化。

我们预计在 2024 年初进入 beta 阶段，但这个时间点只是预计，可能会更改。

## 时间节点

以下是我们迈向 beta 的功能开发大致时间表。时间表的推演基于以下假设：

- 我们的开发速度将与过去两年类似。
- 我们的总工作量大致相当于一个人全职参与该项目。
- 一个独立的“功能”需要一个人 2-4 周的时间来开发和测试，具体取决于功能的复杂度。
- 在实现各种功能的过程中还需要修复其他 bug，因此不应安排过于密集的功能计划。

**这只是预估的时间节点，具体功能发布的顺序并未固定。根据我们遇到的挑战和社区贡献的代码数量，开发速度可能会更快或更慢。此时间线也未包含实现新功能之外的任务，如管理、完善现有功能、重构代码、版本管理及确保与其他 AP 实现的兼容性。**

### 2023 年中

- [x] **话题标签** -- 实现话题标签的联合与查看，让用户发现他们可能感兴趣的帖文。（完成！ https://github.com/superseriousbusiness/gotosocial/pull/2032）。

### 2023 年中到年底

- [x] **投票** -- 实现对投票的解析、创建和参与功能。（完成！ https://github.com/superseriousbusiness/gotosocial/pull/2330）
- [x] **静音帖文/贴文串** -- 取消订阅贴文串的回复通知；不在时间线上显示特定帖文。（完成！ https://github.com/superseriousbusiness/gotosocial/pull/2278）
- [x] **有限联合/白名单** -- 允许实例管理员默认阻止与其他实例的联合。（完成！ https://github.com/superseriousbusiness/gotosocial/pull/2200）

### 2024 年初

- [x] **账户迁移** -- 使用 ActivityPub 的 `Move` 活动支持用户账户在服务器之间的迁移。
- [x] **注册流** -- 允许用户提交注册申请；允许管理员审核注册请求。

### BETA 里程碑

完成以上所有功能即表明我们进入了 GoToSocial 的 BETA 阶段。我们预计在 2024 年 2 月到 3 月之间实现这一阶段。编辑：最终在 2024 年 9 月到 10 月之间实现，抱歉！

### 2024 年余下时间至 2025 年初

这些功能按无特定顺序提供。

- [x] **v2 过滤规则** -- 实现过滤器 API 的第二版。
- [x] **静音账户** -- 静音账户以防止其帖文出现在主页时间线上（可选：限制时间段）。
- [x] **无评论区的帖文** -- 设计无评论区帖文的相关逻辑，让用户创建无评论区的帖文。
- [ ] **屏蔽/允许列表订阅** -- 允许实例管理员订阅纯文本的示例屏蔽/允许列表。（大部分工作已经完成）
- [x] **私信对话视图** -- 让用户能够轻松浏览他们参与的所有私信对话。
- [ ] **Oauth 令牌管理** -- 通过设置面板创建/查看/吊销 OAuth 令牌。
- [ ] **贴文编辑支持** -- 编辑已创建的贴文，而无需删除并重新编辑。并正确地将编辑传播出去。
- [ ] **Fediverse 中继支持** -- 与中继通信，发布和接收帖文。
- [ ] **两步验证 (2fa)** -- 允许用户通过设置面板为其账户启用 2FA，并在登录时实施 2FA。
- [ ] **管理：附加内容警告/将所有内容标记为敏感内容**。

更多内容待定！

### BETA 发布到稳定版发布期间

待定。

## 愿望单

如果时间允许，我们将实现以下这些很酷的功能（因为我们真的很想要）：

- **群组** 与群组发帖！
- 基于声誉的“慢速”联合。
- 联合及管理操作的社区决策。
- 用户可选择自定义模板来渲染公开帖文：
  - 推特风格
  - 博客帖文
  - 图库
  - 等其它风格