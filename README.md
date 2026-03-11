
这是一个基于终端的 AI 编码助手，采用智能体循环（agentic loop）架构。

# 核心思路
- 观察和规划阶段：根据用户和AI助手消息，让 ai 自行判断接下来要做的事情
- Tools: 根据规划的 tools 拆分为可并行执行的 tools和串行执行的 tools，分别执行
- 递归：在执行完成tools后，递归到下一个Query函数，下一个 Query 函数根据上一个执行结果继续
- 模型提示词：直接使用 claude code 反编译版本

## 开发命令

```bash
# 安装依赖
npm install

# 开发模式（TypeScript 监听编译）
npm run dev

# 构建（编译 TypeScript）
npm run build

# 运行 CLI（构建后）
bin/codeai.js

# 或者在开发期间
npm run dev  # 在一个终端
bin/codeai.js   # 在另一个终端
```

## 环境变量

必需的环境变量：
- `CODEAI_BASE_URL`: AI 模型 API 端点的基础 URL
- `CODEAI_AUTH_TOKEN`: API 访问认证令牌
- `CODEAI_MODEL_ID`: 模型标识符（可选，调用 API 时必须提供）

