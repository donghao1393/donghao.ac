---
title: mcp-dbutils（数读）
summary: 让大模型安全连接工业数据库的 MCP 协议工具——11 个工具、多数据库支持、只读安全架构
tags:
  - MCP
  - Database
  - AI Agent
  - Python
  - Industrial AI
date: '2025-06-01T00:00:00Z'

links:
  - type: site
    url: https://github.com/donghao1393/mcp-dbutils
    icon: github
    icon_pack: fab
    name: GitHub
  - icon: hero/video-camera
    icon_pack: hero
    name: B站教程
    url: https://www.bilibili.com/video/BV1pBNXexETM/
---

## 解决了什么问题

工业企业的数据库里躺着大量有价值的数据——生产日志、设备状态、质检记录。但让大模型直接访问数据库是危险的。mcp-dbutils 作为 MCP 协议的安全中间层，让 AI 能**读**数据、**分析**数据，但**绝不修改**数据。

## 怎么用

11 个 MCP 工具，覆盖数据库分析全流程：

| 工具 | 做什么 |
|------|--------|
| `list-connections` | 列出所有可用数据库连接 |
| `list-tables` | 浏览所有表 |
| `describe-table` | 查看表结构（列、类型、约束） |
| `get-ddl` | 获取建表 DDL 语句 |
| `run-query` | 执行只读 SQL（SELECT、JOIN、GROUP BY） |
| `explain-query` | 获取查询执行计划 |
| `analyze-query` | 分析查询性能并给出优化建议 |
| `list-indexes` | 查看表上的索引 |
| `list-constraints` | 查看主键、外键、唯一约束 |
| `get-stats` | 获取表的统计信息（行数、大小等） |
| `get-performance` | 获取连接性能指标 |

## 安全架构

- **只读强制**：所有 SQL 在发送到数据库前经过语法分析，只允许 SELECT
- **连接隔离**：每个数据库连接独立管理，按需连接，自动超时
- **凭证保护**：密码等敏感信息在日志和输出中自动屏蔽
- **本地处理**：数据在本地流转，不上传到任何云端服务

## 技术栈

Python 3.10+ · MCP Protocol · SQLAlchemy · asyncio

支持数据库：SQLite · MySQL · PostgreSQL

## 分布与采用

- PyPI 发布：[mcp-dbutils](https://pypi.org/project/mcp-dbutils/)（`pip install mcp-dbutils`）
- Smithery 一键部署：[smithery.ai](https://smithery.ai/server/@donghao1393/mcp-dbutils)
- Docker 镜像支持
- 多语言文档：中 / 英 / 法 / 西 / 阿 / 俄

## 工业场景方向（规划中）

mcp-dbutils 正在向「数读」工业 AI Agent 演进。目标场景：

- **生产数据库问答**：工厂车间主任用自然语言问"上周哪条产线良率最低"，Agent 直接查数据库给出答案，不需要等 IT 部门写 SQL
- **设备状态巡检**：Agent 定时扫描设备运行日志表，发现异常自动告警，附带历史趋势分析
- **供应链库存洞察**：多表 JOIN 分析——库存水位、交付周期、供应商历史履约率——一个提问，Agent 完成查询 + 可视化 + 建议

如果你来自工业企业，对以上场景有需求或想法，[联系我](/contact)。
