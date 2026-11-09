# 测评蓝图与试卷质量审查

在试卷生成后或已有试卷上建立测评蓝图并审查覆盖、难度、题型、分值和作答时间。

## 适用用户

教研组长、命题教师、教学主管、测评负责人

## 主要输出

- 测评蓝图
- 题目属性表
- 覆盖缺口
- 难度/时间风险
- 评分一致性问题
- 复核清单

## 安装

将包含`SKILL.md`的根目录导入支持的Skill环境。

本地验证：

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 使用

1. 阅读`USAGE.md`。
2. 按`contract/input.schema.json`准备输入。
3. 调用产品或Agent完成专业处理。
4. 使用`scripts/validate_output.js`检查成果。
5. 高风险结论交由业务负责人确认。

## 边界

- 不使用外部收费API。
- 不依赖其他产品完成核心任务。
- 不自动执行正式审批、退款、人员处罚或系统变更。
- 客户可见内容不包含公司品牌推广或内部研发资料。

## 状态

- 版本：`1.0.0`
- 本地契约与自动化测试：见`test-results/`
- 生成式模型运行：`MODEL_RUNTIME_NOT_VERIFIED`
- WorkBuddy安装、调用、审核、上架：`NOT_EXECUTED`
- 安装包：`dist/edu-assessment-blueprint-quality-review-v1.0.0.zip`

## 许可证

Apache-2.0。详见`LICENSE`。
