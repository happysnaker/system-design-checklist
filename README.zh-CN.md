# system-design-checklist（简体中文）

[English](./README.md) | 简体中文

一个面向后端工程师的 **系统设计检查清单**。  
它既适合：

- 系统设计面试
- 架构评审
- 设计文档撰写
- 上线前的生产就绪性检查
- 分布式系统方向的自学与复盘

这个仓库的核心思路不是“背答案”，而是提供一个可以复用的 **思考框架**：

- 先明确问题和约束
- 再拆 API、数据模型、读写路径
- 然后补齐一致性、可靠性、可观测性、安全和上线策略

## 这个仓库里有什么

- 一份可直接复用的系统设计 checklist
- 一份轻量级设计文档模板
- 一页常见架构 tradeoff 速查
- 一组适合面试 / 评审的追问问题
- 两个 worked example（完整示例）

## 适合怎么用

### 1. 系统设计面试

面试时最常见的问题不是“不知道怎么设计”，而是：

- 漏掉关键约束
- 只会画图，不会讲 tradeoff
- 忘记可用性、扩容、缓存、一致性和运维问题

你可以把这份清单当作答题骨架，保证回答有层次，不容易漏项。

### 2. 架构评审

当你在 review 一个方案时，可以按清单逐项检查：

- 哪些假设最容易先失效？
- 哪些地方会成为瓶颈？
- 是否为了“看起来高级”而过度设计？
- 这个方案 6 个月后运维会不会很痛苦？

### 3. 设计文档

如果你要写一个轻量设计文档，可以直接配合模板一起用：

- [`docs/service-design-template.md`](./docs/service-design-template.md)

## Checklist 的主要结构

这份清单覆盖以下几个部分：

1. 问题定义
2. 功能与非功能约束
3. 规模估算
4. API 与边界设计
5. 数据模型与存储
6. 读路径设计
7. 写路径设计
8. 异步流程 / 队列 / 事件
9. 一致性与正确性
10. 可靠性与弹性
11. 可观测性与运维
12. 安全与滥用防护
13. 交付与灰度发布
14. 最终评审追问

## 附加资料

- [`docs/common-tradeoffs.md`](./docs/common-tradeoffs.md) — 常见架构取舍
- [`docs/review-questions.md`](./docs/review-questions.md) — 评审 / 面试追问清单
- [`docs/service-design-template.md`](./docs/service-design-template.md) — 轻量设计文档模板

## Worked examples（完整示例）

如果你不想只看 checklist，而是想看“这套方法怎么真正落地”，可以直接看下面两个例子：

- **[短链接系统](./docs/examples/url-shortener.md)**  
  适合看读多写少系统、缓存、热点 key、存储模型和扩容思路。

- **[通知系统](./docs/examples/notification-service.md)**  
  适合看异步队列、扇出、多通道投递、重试、死信队列、用户偏好和第三方通道故障处理。

## 这个仓库适合谁

如果你属于下面任意一种，这个仓库会比较有用：

- 准备后端 / 基础架构 / 分布式系统面试
- 经常写 API、服务或平台设计文档
- 想提升自己做架构 review 的能力
- 带新人，需要一套可复用的系统设计框架

## 相关仓库

- [`backend-engineer-checklist`](https://github.com/happysnaker/backend-engineer-checklist) — 后端成长路线与知识清单
- [`go-service-starter`](https://github.com/happysnaker/go-service-starter) — 更偏工程落地的 Go 服务脚手架

## 支持

如果这个仓库对你有帮助，可以：

- 点一个 Star
- 分享给其他后端工程师
- 通过支持页支持持续的开源整理与维护：
  [happysnaker.github.io/support](https://happysnaker.github.io/support/)

