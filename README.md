# open-design-assistant

[中文](README.md) | [English](README.en.md)

一个只掌控 workflow 的设计技能。Open Design 负责需求理解、设计判断，以及所有中间和最终产物；本技能负责阶段调度、成果展示和用户反馈传递。

## 工作流

需求理解与研究 → 三方向探索 → 用户选择 → 早期对齐 → 深化与迭代 → 评审与验证 → 导出与交付。

默认先展示三个真实视觉方向，由用户选择后深化。用户明确跳过、已批准方向的迭代和机械操作按适用阶段推进。

每个环节在本轮完成「输入 → Open Design 执行 → 等待终态 → 回收 → 检查/补齐 → 展示」，再停在必要的用户决策点。任务记录、显式项目绑定和幂等恢复用于支撑续接；仅显示需求卡或启动任务不算阶段完成，已生成成果无需用户另发「继续」才回传。

## 安装与使用

将本仓库放入运行环境识别的技能目录，目录名保持为 `open-design-assistant`，例如 `~/.agents/skills/open-design-assistant/`。重载技能后调用：

```text
$open-design-assistant 为我的产品制作发布演示，使用已连接的 Open Design。
```

## 前提与边界

需要已连接、具备执行能力的 Open Design MCP，或已安装的 Open Design Codex plugin。调用时使用当前运行环境实际提供的入口和工具名称。

本技能不附带执行器，不自动安装服务，也不固定某个同名 Open Design 产品。只有设计资料库、brief 模板和产物登记功能的入口，不等于具备制作与导出能力。真正的插件执行工作流可以由宿主执行；编排层不能自行解释需求或制作作品后冒称 Open Design 执行。

所有过程和最终文件遵循使用者自己的项目输出规则。资源只读使用。

## 验证状态

已完成独立代理的职责与阶段模拟测试，并针对插件委派和三方向豁免完成修订与复测。尚未完成真实 Open Design 端到端测试，也未验证全部运行环境和模型的兼容性。

逐环节闭环、需求卡能力边界与成果回收规则已完成文档审查和落盘一致性核验；这不等于真实生成流程的端到端验证。

## 参考

流程参考 [huashu-design](https://github.com/alchaincyf/huashu-design)。接入差异可参考 [Open Design agent-kit MCP 说明](https://github.com/feimacode/open-design-agent-kit/blob/main/packages/mcp-server/README.md)。

本项目为独立工作流技能，以上参考项目不是安装依赖。
