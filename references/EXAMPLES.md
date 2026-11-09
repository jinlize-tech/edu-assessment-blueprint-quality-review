# 测评蓝图与试卷质量审查示例

## 典型场景

期中试卷80%题目为记忆题，但测评目标强调应用与分析。

## 具体示例

系统量化题型/认知层级偏差，指出需要补充哪些应用任务，并提示人工试做与学科审题。

## 脱敏输入示例

```json
{
  "contract_version": "1.2.0",
  "data_status": "confirmed",
  "contains_sensitive_data": false,
  "requested_output_language": "zh-CN",
  "assessment_purpose": "测评用途已核对（脱敏示例）",
  "exam_paper": "试卷与题目已核对（脱敏示例）",
  "answer_key": "答案与评分标准已核对（脱敏示例）",
  "learning_objectives": [
    {}
  ],
  "knowledge_points": [
    {}
  ],
  "duration": 45,
  "student_level": "学生群体已核对（脱敏示例）"
}
```

## 预期处理

1. 运行输入契约校验。
2. 逐项核对输入来源、版本和口径。
3. 按`references/PROFESSIONAL_PLAYBOOK.md`完成专业分析。
4. 输出测评蓝图、题目属性表、覆盖缺口等核心成果。
5. 由业务负责人确认输入事实、关键假设和最终成果适用范围后才可作为正式业务结论。

## 不应出现的输出

- 虚构政策、价格、人员、课程或客户事实。
- 以“暂无”“待完善”等占位文本冒充完成。
- 无依据的确定性判断或伪造人工签批。
