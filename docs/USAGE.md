# 🚀 Skeleton 使用指南

本文档介绍如何使用简化的 Makefile 命令来管理项目。

## 📋 常用命令

### 🏗️ 构建项目
```bash
make build      # 构建所有服务
make api        # 只构建 API 服务
make consumer   # 只构建消费者服务
make scheduler  # 只构建调度器服务
```

### 🐳 Docker 操作
```bash
make up         # 启动 Docker 环境
make down       # 停止 Docker 环境
make restart    # 重启 Docker 环境
make logs       # 查看服务日志
make ps         # 查看容器状态
```

### 🚀 运行服务
```bash
make run                # 运行 API 服务
make run-consumer       # 运行消费者服务
make run-scheduler      # 运行调度器服务
```

### 📊 数据库操作
```bash
make migrate    # 运行数据库迁移
make seed       # 运行数据库种子
make db-reset   # 重置数据库
make db-shell   # 进入数据库容器
```

### 🧪 测试命令
```bash
make test       # 运行测试
make test-api   # 测试 API 端点
make test-mq    # 测试消息队列
```

### 🔧 开发工具
```bash
make shell      # 进入 API 容器
make fmt        # 格式化代码
make lint       # 代码检查
make clean      # 清理构建产物
```

## 🎯 快速开始

### 1. 启动开发环境
```bash
# 启动所有服务
make up

# 查看服务状态
make ps

# 查看日志
make logs
```

### 2. 初始化数据库
```bash
# 运行数据库迁移
make migrate

# 添加种子数据
make seed
```

### 3. 测试 API
```bash
# 测试健康检查
curl http://localhost:8080/health

# 或使用 Makefile 命令
make test-api
```

### 4. 开发调试
```bash
# 进入 API 容器
make shell

# 查看数据库
make db-shell
```

## 🎨 命令特色

- **简洁**：使用最短的命令名
- **直观**：命令名称与功能对应
- **一致**：Docker 和本地开发使用相同的命令模式
- **高效**：减少输入时间，提高开发效率

## 🔗 相关文档

- [项目 README](../README.md)
- [消息队列文档](MESSAGE_QUEUE.md)

## 💡 提示

1. 使用 `make help` 查看所有可用命令
2. 使用 `make` 或 `make all` 执行完整构建流程
3. 开发时建议使用 `make up` 启动环境，`make logs` 查看日志
4. 生产环境使用 `make prod` 部署

享受简化的开发体验！🎉 