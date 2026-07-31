---
title: mcp-dbutils
summary: 让大模型直接分析数据库的开源 MCP 工具
tags:
  - MCP
  - Database
  - AI Agent
  - Python
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

mcp-dbutils 是一个 MCP (Model Context Protocol) 数据库工具，旨在让大语言模型（如 DeepSeek、千问 QWQ 等）能够直接连接和分析数据库。

## 核心特性

- **只读安全**：默认只读模式，保护生产数据安全
- **统一配置**：单一配置文件管理多个数据库连接
- **性能管理**：内置查询超时和结果集大小限制
- **元数据管理**：自动发现数据库 schema 和表结构
- **多数据库支持**：支持 SQLite、PostgreSQL、MySQL 等主流数据库

## 技术栈

Python · MCP Protocol · SQLAlchemy · asyncio
