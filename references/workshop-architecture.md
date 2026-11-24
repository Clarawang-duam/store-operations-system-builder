# 手作工坊架构示例

| 职责 | 项目划分 |
|---|---|
| 展示、交互、提交用户动作 | UI，位于 app 和 components |
| 编排订单、预约等业务流程 | Business，位于 domains，可调用引擎与仓储 |
| 根据输入计算费用、判定状态 | Engine，位于 engines，纯逻辑且无数据库访问 |
| 集成支付等外部能力 | Service，位于 services |
| 封装订单、座位等数据读写 | Repository，位于 repositories |
| 提供数据库连接等底层能力 | Infrastructure，位于 infrastructure |

前后端都需要的纯函数和纯类型可放 shared。简单项目可以合并文件和目录，同时保留职责边界。

## Next.js 和 Prisma

- 通过服务端入口发起写入。客户端组件避免导入 Prisma、数据仓储、仅服务端的 Domain 和依赖 Prisma 的序列化模块。
- 用 server-only 标明数据库连接与数据访问模块的执行边界。
- 服务端把传给浏览器的数据转换为可序列化的对象。手作工坊用 toPlain 将 Prisma.Decimal 转为字符串，保留金额精度。
