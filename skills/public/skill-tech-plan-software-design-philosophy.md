# Skill 技术方案（方案 A：单一综合技能）

## 1. 目标与约束
- 目标：把 `design.md`/`method.md`/`plan.md` 的知识转化为一个可触发、可执行、可复用的 Skill
- 约束：
- `SKILL.md` 精简（只放流程与路由规则）
- 详细内容放 `references/`，避免上下文膨胀
- 输出必须结构化、强调行动项

## 2. 目录结构（方案 A）
```
software-design-philosophy/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── outline.md      # 来自 design.md
    ├── methodology.md  # 来自 method.md
    ├── checklist.md    # 来自 plan.md
    └── examples.md     # 聚合用例（聊天系统、俄罗斯方块、NFT）
```

## 3. Skill 触发与路由规则（核心）
- 触发关键词覆盖范围（写入 frontmatter `description`）：
  - 设计大纲、设计哲学、方法论、最佳实践、评审清单、架构评审
- 路由规则（写入 SKILL.md）：
  - “大纲/章节/结构/目录” → 读 `outline.md`
  - “方法论/落地/步骤/实践/理念+方法+案例” → 读 `methodology.md`
  - “清单/检查/评审/核对” → 读 `checklist.md`
  - 组合请求 → 分段输出（先方法论，再清单）

## 4. SKILL.md 结构（详细）
建议模板结构：
1. Purpose
- 明确该 Skill 的目标与能力边界
2. Routing Rules
- 如何识别用户意图
- 何时加载哪份 reference
3. Output Constraints
- 中文、结构化标题 + 分点、行动项优先
4. Context Adaptation
- 团队规模、系统规模、阶段不同如何调整建议
5. Usage Examples
- 引用 `examples.md` 或直接放 3-5 个最小案例

## 5. References 组织策略
- `outline.md`: 只放设计哲学大纲
- `methodology.md`: 方法论与可执行步骤
- `checklist.md`: 最佳实践清单
- `examples.md`: 聊天系统、俄罗斯方块、NFT 用例

## 6. 生成与验证流程
1. 初始化 Skill
- 使用 `scripts/init_skill.py` 生成目录
2. 写 `SKILL.md`
3. 复制并整理 references
4. 生成 `agents/openai.yaml`
5. 验证
- `scripts/quick_validate.py`

## 7. 测试用例接入
- 直接复用已整理的测试用例文档
- 每次更新 Skill 后，按测试用例做验证
- 输出需要满足“路由正确 + 不混输出 + 格式一致”

## 8. 迭代策略
- 触发内容过杂 → 细化路由规则
- 用户只要某类输出 → 可能拆分为方案 B
- 输出冗长 → 增加“摘要优先”规则
