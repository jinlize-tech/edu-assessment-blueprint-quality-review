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

本地校验（安装包不包含`examples/`或`test-results/`）：

```powershell
node scripts/validate_input.js input.json
node scripts/validate_output.js output.json
```

`input.json`需根据`contract/input.schema.json`自行准备；`output.json`是产品生成的待校验成果。`prepare_result.js`可生成处理前检查结果：

```powershell
node scripts/prepare_result.js input.json
```

## 安装包内容说明

安装包包含运行所需的产品定义、契约Schema、模板、参考资料、校验脚本、许可证和说明文档。安装包不包含仓库中的`examples/`、`tests/`、`test-results/`或研发审计材料。

首次使用请先依据`contract/input.schema.json`准备自己的`input.json`，不要引用安装包中不存在的示例文件。

## 使用

1. 阅读`USAGE.md`。
2. 按`contract/input.schema.json`准备输入。
3. 调用产品或Agent完成专业处理。
4. 将产品生成的最终JSON保存为`output.json`，运行`node scripts/validate_output.js output.json`。
5. 高风险结论交由业务负责人确认。

## 边界

- 不使用外部收费API。
- 不依赖其他产品完成核心任务。
- 不自动执行正式审批、退款、人员处罚或系统变更。
- 客户可见内容不包含公司品牌推广或内部研发资料。

## 状态

- 版本：`1.0.1`
- 契约与自动化测试证据：保存在[GitHub仓库](https://github.com/jinlize-tech/edu-assessment-blueprint-quality-review/blob/main/test-results/v1.0.1.json)，不随安装包分发。
- 生成式模型运行：`MODEL_RUNTIME_NOT_VERIFIED`
- WorkBuddy安装、调用、审核、上架：`NOT_EXECUTED`
- 安装包：`dist/edu-assessment-blueprint-quality-review-v1.0.1.zip`

## 许可证

Apache-2.0。详见`LICENSE`。
