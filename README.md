# Postman - Swatch Group 企业费控 API

本仓库使用 Postman 本地工作区（Local Workspace）管理企业费控系统的 API 集合。

## 📁 目录结构

```
postman/
  collections/        # API 集合（A～T，按业务模块分类）
  environments/       # 环境变量
  globals/            # 全局变量（本地运行时，不提交）
```

## 🚀 快速开始

### 1. 配置凭证

复制示例文件并填入真实凭证：

```bash
# 该文件已被 .gitignore 忽略，不会提交到 Git
postman/environments/credentials.secret.environment.yaml
```

将以下字段替换为真实值：
- `appKey` — 应用 Key
- `appSecurity` — 应用密钥

> 参考模板：`credentials.secret.environment.yaml.example`

### 2. 获取授权 Token

打开集合 **A、开始使用** → **获取授权**，发送请求后：
- `accessToken` 和 `refreshToken` 会自动保存到全局变量
- 后续所有接口请求会自动使用这些 token

### 3. 调用业务接口

从 B～S 集合中选择对应的业务接口即可。

## 🔒 安全说明

以下文件**不会**被提交到 Git（已在 `.gitignore` 中配置）：

| 文件 | 原因 |
|------|------|
| `*.secret.environment.yaml` | 包含 appKey、appSecurity 等敏感凭证 |
| `*.local.environment.yaml` | 个人本地配置 |
| `postman/globals/workspace.globals.yaml` | 包含运行时 accessToken、refreshToken |
| `.env` / `.env.local` | 通用密钥文件 |

**请勿将真实凭证提交到 Git！**

## 📋 集合说明

| 集合 | 功能 |
|------|------|
| A、开始使用 | 授权认证（必须先执行） |
| B、企业通讯录 | 查询员工、部门、角色 |
| C、通讯录同步 | 新增/修改/删除员工和部门 |
| D、自定义档案 | 档案类别和档案项管理 |
| E、档案关系 | 档案关系数据管理 |
| F、费用类型 | 费用类型配置 |
| G、单据模板 | 单据模板管理 |
| H、单据 | 核心：创建/提交/审批/查询单据 |
| I、委托授权 | 委托授权管理 |
| J、企业收付款账户 | 收付款账户管理 |
| K、预算 | 预算包和预算节点管理 |
| L、自建应用 | 自建应用和业务对象 |
| M、扩展中心 | 发票、成本中心等扩展功能 |
| N、出站消息 | 外部服务回调 |
| O、附件 | 附件上传下载 |
| P、城市管理 | 城市组管理 |
| Q、币种汇率 | 币种和汇率管理 |
| R、基础数据 | 城市列表等基础数据 |
| S、工具接口 | 工具类接口 |
| T、历史版本（不推荐） | 旧版接口，请勿使用 |
