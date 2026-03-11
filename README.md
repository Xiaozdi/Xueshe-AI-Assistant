# 学舌AI智能助手

<<<<<<< HEAD
一个基于deepseek-V3的智能文档问答助手，利用RAG技术让用户可以通过上传文档来轻松搭建私有知识库，支持多种格式文档的上传、向量化处理和智能问答功能。
=======
一个基于 DeepSeek-V3 的智能文档问答助手，利用 RAG 技术让用户通过上传文档轻松构建私有知识库，支持多种格式文档的上传、向量化处理与智能问答功能。

项目说明文档位于当前分支，具体代码请查看 `master` 分支。
>>>>>>> 9e4d43c1087cfbca1799540c5d65ba51be975004

## 功能特点

- 支持多种文档格式
<<<<<<< HEAD
  - Word文档 (.docx)
  - PDF文件 (.pdf)
  - 文本文件 (.txt)，支持UTF-8和GBK编码

- 智能文档处理
  - 基于BAAI/bge-m3的embedding架构
  - 自动文档解析
  - 文本分块处理
  - 向量化存储
  - 相似度匹配
=======
  - Word 文档（`.docx`）
  - PDF 文件（`.pdf`）
  - 文本文件（`.txt`），支持 UTF-8 和 GBK 编码

- 智能文档处理
  - 基于 BAAI/bge-m3 的 Embedding 模型
  - 文档自动解析
  - 文本分块处理
  - 向量化存储
  - 向量相似度匹配
>>>>>>> 9e4d43c1087cfbca1799540c5d65ba51be975004

- 用户系统
  - 微信授权登录
  - 用户信息管理
  - 文档管理
<<<<<<< HEAD
  - 向量库后台管理
=======
  - 向量数据库管理
>>>>>>> 9e4d43c1087cfbca1799540c5d65ba51be975004
  - 聊天历史记录

- 智能对话
  - 基于文档的智能问答
  - 语音输入支持
  - 实时对话界面

## 技术架构

### 前端（微信小程序）
<<<<<<< HEAD
- 基于微信小程序原生框架
- 组件化开发
- TabBar导航（对话页、用户页）

### 后端（云开发）
- 云函数
  - processDocument: 文档处理
  - login: 用户登录
  - checkLogin: 登录状态检查
  - deepseekReply: AI回复生成

- 云数据库
  - users: 用户信息
  - document_vectors: 文档向量
  - user_documents: 用户文档
  - chat_history: 聊天记录

- 云存储
  - 文档存储
  - 用户信息
=======

- 基于微信小程序原生框架
- 组件化开发
- TabBar 导航（对话页、用户页）

### 后端（云开发）

- 云函数
  - `processDocument`：文档处理
  - `login`：用户登录
  - `checkLogin`：登录状态检查
  - `deepseekReply`：AI 回复生成

- 云数据库
  - `users`：用户信息
  - `document_vectors`：文档向量
  - `user_documents`：用户文档
  - `chat_history`：聊天记录

- 云存储
  - 文档文件存储
  - 上传附件存储
>>>>>>> 9e4d43c1087cfbca1799540c5d65ba51be975004

## 核心功能实现

### 文档处理流程
<<<<<<< HEAD
1. 文件上传至云存储
2. 根据文件类型解析内容
3. 文本清理和分块
=======

1. 文件上传至云存储
2. 根据文件类型解析内容
3. 对文本进行清理与分块
>>>>>>> 9e4d43c1087cfbca1799540c5d65ba51be975004
4. 生成向量嵌入
5. 存储到向量数据库

### 智能问答流程
<<<<<<< HEAD
1. 用户输入向量化
2. 相似度匹配
3. 检索相关文档
4. 生成AI回复

## 部署说明

1. 环境要求
   - 微信开发者工具
   - 微信小程序云开发环境

2. 配置步骤
   ```javascript
   // 修改 app.js 中的环境ID
   wx.cloud.init({
     env: 'your-env-id',
     traceUser: true,
   });
   ```

3. 安装依赖
   ```bash
   # 在 cloudfunctions/processDocument 目录下
   npm install mammoth pdf-parse iconv-lite axios
   ```

4. 必要的云开发配置
   - 创建必要的数据库集合
   - 配置安全规则
   - 上传云函数

## 注意事项

- 文件大小限制：单个文件不超过20MB
- 支持的文件格式：.docx, .pdf, .txt
- 个人重新部署需要在云环境中配置相应的API密钥（如SiliconFlow API）

## 贡献指南

欢迎提交Issue和Pull Request来帮助改进项目。

## 许可证

本项目基于MIT协议开源。
=======

1. 对用户输入进行向量化处理
2. 执行向量相似度匹配
3. 检索相关文档内容
4. 生成 AI 回复

## 部署说明

### 1. 环境要求

- 微信开发者工具
- 微信小程序云开发环境

### 2. 配置步骤

在 `app.js` 中修改云开发环境 ID：

```javascript
wx.cloud.init({
  env: 'your-env-id',
  traceUser: true,
});
```

### 3. 安装依赖

在 `cloudfunctions/processDocument` 目录下执行：

```bash
npm install mammoth pdf-parse iconv-lite axios
```

### 4. 必要的云开发配置

- 创建必要的数据库集合
- 配置数据库安全规则
- 上传并部署云函数
- 配置相关 API 密钥

## 注意事项

- 单个上传文件大小不超过 20MB
- 当前支持的文件格式为 `.docx`、`.pdf`、`.txt`
- 重新部署项目时，需要在云环境中配置相应的 API 密钥（如 SiliconFlow API）
- 请确保微信云开发环境已正确开通并关联当前项目

## 贡献指南

欢迎提交 Issue 和 Pull Request 来帮助改进项目。

如果你希望参与贡献，建议按照以下流程进行：

1. Fork 本仓库
2. 新建功能分支
3. 提交修改
4. 发起 Pull Request

## 许可证

本项目基于 MIT License 开源，详情请参见 `LICENSE` 文件。
>>>>>>> 9e4d43c1087cfbca1799540c5d65ba51be975004
