# 使用说明

## 适用任务

期中试卷80%题目为记忆题，但测评目标强调应用与分析。

## 准备输入

试卷、答案与评分标准、单元目标、知识点清单、教学课时、学生水平、考试时长。使用前先脱敏姓名、联系方式和与任务无关的敏感信息。

## 操作步骤

1. 明确用途
2. 建立蓝图
3. 标注题目属性
4. 检查覆盖与配比
5. 审查时间与评分
6. 标记风险题
7. 输出修订建议

## 校验命令

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 状态使用

- `completed`：核心成果完整。
- `completed_with_limits`：只完成可验证部分，并说明受阻范围。
- `needs_input`：缺少关键输入。
- `needs_confirmation`：资料冲突或需人工确认。
- `failed`：工具或计算失败，提供恢复动作。

## 人工确认

业务负责人复核输入事实、关键假设和最终成果适用范围后，成果才可进入正式业务使用。
