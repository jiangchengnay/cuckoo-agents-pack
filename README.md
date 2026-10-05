# 专家子代理包（cuckoo-agents-pack）

为 [Cuckoo Code](https://github.com/wangyongpeng90/cuckoo-code) 增加 5 个专家子代理。

## 包含子代理

| 子代理 | 用途 |
|---|---|
| `code-reviewer` | 系统性代码审查（正确性/边界/安全/性能） |
| `test-engineer` | 编写/补全单元测试，覆盖失败路径 |
| `security-auditor` | 安全审计：注入/密钥泄露/鉴权/路径穿越 |
| `debugger` | 系统化排查报错，定位根因 |
| `doc-writer` | 生成函数注释/README/API 文档 |

## 用法

装并启用后，在主对话里说"用 code-reviewer 审查 xxx"，AI 会自动 `runAgent('code-reviewer', '...')` 委派。

子代理在**独立上下文**执行，只把结果摘要返回主对话，**不污染当前上下文**。

## 安装

插件页搜索 `cuckoo-plugin`，或：

```bash
git clone https://github.com/jiangchengnay/cuckoo-agents-pack.git ~/.cuckoo/plugins/cuckoo-agents-pack
```

## 许可

MIT
