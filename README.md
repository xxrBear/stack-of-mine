# 我的开发技术栈 - 2025

## 简介

本项目整理了我当前使用的语言和开发工具，所谓工欲善其事必先利其器，希望可以在大家开发时提供一些参考

## 数据库

### PostgreSQL

PostgreSQL 是世界上最强大的开源关系型数据库。它开源、稳定，迄今为止以及发展超过三十年，可以说是久经考验。配合相应插件，能替代消息队列、缓存和全文搜索等组件，有时候一个 PostgreSQL 就能解决后端开发的大部分需求


### Redis

Redis 意为远程字典服务器，自 2009 年诞生以来，它迅速成为最著名的非关系型数据库之一，虽然近些年来受到开源协议变更的影响，Redis 是否是一个开源软件现在有点儿争议，但这并不影响它的地位，它依旧广泛用于各类公司的系统中

## Python 开发

### uv

uv 是基于 Rust 开发的，性能优异，不仅能安装第三方库，还能下载安装不同版本的 Python 解释器。它可以取代 pip 和 virtualenv，并提供并发下载等强大的功能

uv 的设计哲学之一就是不需要激活虚拟环境就可以执行对应包

```shell
# 查看当前已安装的 python 版本和可以安装的版本
uv python list 

# 创建一个 .venv 虚拟环境
uv venv .venv   

# 下载指定库
uv add [package]

# 删除指定库
uv remove [package]

# 安装指定版本的 python
uv install python 3.14 

# 运行 main.py 不用激活环境
uv run python main.py  
```

### Ruff

Ruff 是一个用 Rust 开发的 Python 代码检查和格式化工具，可以自定义和修正代码风格。它在团队开发中非常有用，能保证代码风格统一、减少不必要的争论

- 基本操作

```shell
# 安装
uv add ruff

# 检查代码
uv run ruff check

# 修复
uv run ruff check --fix
```

### Pydantic

这是一个用 Rust 编写的数据验证工具，可以帮你检查和验证数据格式

### pytest

这是一个现代的 Python 测试框架，比内置的 unittest 更符合 Python 开发风格，功能更丰富

### FastAPI

这是目前最流行的 Python 框架，能让你快速、高效地开发后端 API

### Django

个人最喜爱的 Python Web 框架，具有强大的能力和悠久的历史，是 Instagram 的早期支柱

## 消息队列

### RabbitMQ

RabbitMQ 是用 Erlang 编写的消息队列，性能稳定，功能强大。它可以处理大量异步任务和消息传递

## 容器

### Docker

经典的容器化工具，使用广泛。它可以把应用及其依赖打包在容器中，实现快速部署和一致运行环境，同时简化运维管理，提高系统的可靠性和可移植性

