# 图片生成实验记录模板

依据 [Prompt 版本规范](../prompt-versioning.md)。每次实际生成单独建立记录；模板不代表已运行。

## 实验信息与目标

```yaml
experiment_id: null
executed_at: null                # 实际运行时间，注明时区
run_status: not_run              # not_run / completed / failed
prompt_id: null
prompt_version: null             # 字符串，例如 "0.2"
prompt_file: null
prompt_commit: null              # 能获取时记录对应提交
objective: null
comparison_experiment: null
```

## 模型与参数

```yaml
provider: null
entry_point: null
model_name: null
model_revision: null
seed: null
resolution: null
steps: null
other_parameters: {}
reference_assets: []
unknowns: []
```

未知或未公开的参数保持 `null`，并写明原因。更换模型、参数或参考图时，明确比较条件，不把不同配置的结果当成仅由 Prompt 改动引起。

## 实际提交的完整 Prompt

```text
待填写实际文本，包括本次变量展开结果。
```

## 负面限制与多轮编辑

记录负面限制的内容及实际发送位置；有前置图片、历史轮次、追加编辑指令或可见的提示词改写时，一并保存其定位与内容。看不到的内部改写保持未知。

## 输出与执行结果

```yaml
outputs: []                      # 每张输出的路径/可访问定位；必要时附哈希
error: null                     # 失败时记录真实错误，不把失败标为 completed
selection_reason: null          # 多张图中选择某张的理由
```

保留本次所有候选结果或其可追溯定位，不只保留最佳图。公开前检查素材和反馈是否适合公开。

## 结果分析

### 优点

尚未评价。

### 问题与失败案例

尚未评价。

### 用户评价

```yaml
decision: pending               # pending / satisfied / unsatisfied
feedback: null
reviewed_at: null
reviewer: null
confirmation_reference: null
confirmed_outputs: []
```

用户对这次图片满意，不自动代表在其他人物、模型或分镜条件下同样满意。升正式版还需在版本记录中登记验收范围。

### 可选评分

可以分别评价人物、线条、构图、服装和氛围；注明评分人和量表，未评价留空。AI 自评与用户评分分开，任何分数都不自动触发升版。

### 下一次迭代

填写要保留什么、修改什么，以及下一次要验证的问题。未完成实验时不要预写结论。
