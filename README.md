
这是一个基于终端的 AI 编码助手，采用智能体循环（agentic loop）架构。

## 开发命令

```bash
# 安装依赖
npm install

# 开发模式（TypeScript 监听编译）
npm run dev

# 构建（编译 TypeScript）
npm run build

# 运行 CLI（构建后）
bin/codeai

# 或者在开发期间
npm run dev  # 在一个终端
bin/codeai   # 在另一个终端
```

## 环境变量

必需的环境变量：
- `CODEAI_BASE_URL`: AI 模型 API 端点的基础 URL
- `CODEAI_AUTH_TOKEN`: API 访问认证令牌
- `CODEAI_MODEL_ID`: 模型标识符（可选，调用 API 时必须提供）

