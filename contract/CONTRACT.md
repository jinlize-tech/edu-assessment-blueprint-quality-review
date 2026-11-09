# 输入输出契约

## 输入字段

| 键 | 名称 | 类型 | 必填 |
|---|---|---|---|
| `assessment_purpose` | 测评用途 | string | 是 |
| `exam_paper` | 试卷与题目 | string | 是 |
| `answer_key` | 答案与评分标准 | string | 是 |
| `learning_objectives` | 学习目标 | array | 是 |
| `knowledge_points` | 知识点与课时 | array | 是 |
| `duration` | 考试时长 | integer | 是 |
| `student_level` | 学生群体 | string | 是 |

## 状态

- `completed`：核心成果完整，关键结论人工确认要求满足。
- `completed_with_limits`：至少一项实质成果，说明限制、已完成和受阻范围。
- `needs_input`：必填字段缺失。
- `needs_confirmation`：资料冲突或人工确认未完成。
- `failed`：计算或工具失败。

## 输出

- `测评蓝图`：结构化条目数组，不允许空壳或占位文本。
- `题目属性表`：结构化条目数组，不允许空壳或占位文本。
- `覆盖缺口`：结构化条目数组，不允许空壳或占位文本。
- `难度/时间风险`：结构化条目数组，不允许空壳或占位文本。
- `评分一致性问题`：结构化条目数组，不允许空壳或占位文本。
- `复核清单`：结构化条目数组，不允许空壳或占位文本。

完整机器契约见`contract/input.schema.json`、`contract/output.schema.json`和`contract/runtime_contract.json`。
