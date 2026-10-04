# Prompt 版本模板

依据 [版本规范](../prompt-versioning.md)。复制到 `prompt-library/<prompt-id>/v<version>.md` 后填写；模板本身不是实际实验或已验收版本。

```yaml
prompt_id: null                  # 稳定的英文标识；实际使用时必填
version: "0.1"                  # 必须是字符串
status: experimental            # experimental / candidate / approved / withdrawn
parent_version: null
promoted_from: null              # 正式版对应的已验收实验/候选版本
created_at: null                 # 实际创建时间，注明时区
updated_at: null

target:
  visual_goal: null
  medium: null                  # 例如：黑白漫画分镜 / 彩色动画单帧
  subject_scope: null
  composition_scope: null
  exclusions: []

model:
  provider: null
  entry_point: null              # 产品界面、API 或本地工作流
  name: null
  revision: null                 # 未公开或不可见则保持 null
parameters:
  seed: null
  resolution: null
  steps: null
  other: {}
unknowns: []                     # 列出未能获取的信息及原因
reference_assets: []             # 文件/来源定位；必要时附哈希及公开授权说明
component_snapshots: []          # 使用的组件路径与版本/提交
experiments: []                  # 实际实验记录路径
repeatability:
  status: not_tested             # not_tested / single_run / repeated_tested
  total_runs: 0
  satisfactory_runs: null        # 尚未评价时不是 0
  criteria: null
approval:
  approved_by: null
  approved_at: null
  user_confirmation: null        # 对具体版本与结果满意的最小必要确认
  evidence: []                   # 确认与被确认图片的可定位记录
  scope: null
```

## 目标与验收关注点

填写人物、线条、墨色/色彩、服装、构图、分镜/镜头以及氛围中真正重要的要求。明确哪些条件不在本次验收范围。

## 完整 Prompt

```text
待填写；不可直接用于实验，也不可标为已验收。
```

## 负面限制及实际发送方式

```text
待填写。注明单独负面提示、并入正文，或未使用；不要假设模型支持某种入口。
```

## 变量、默认值与参考上下文

填写变量替换规则、默认值、参考图顺序及多轮编辑上下文；实验记录要保留展开后的全部文本。无变量时注明“无”。

## 相比父版本的修改

记录改了什么、为什么改、预期影响什么。只有新增反馈或重复生成、没有修改 Prompt/配置时，不必创建新版本。

## 实验与反馈

关联真实实验路径、图片定位、用户反馈、可选评分与失败案例。未生成写“未测试”；未评分留空，不填示例成绩。

## 验收与已知局限

记录满意的具体版本与结果、适用模型和场景、复现状态。没有用户明确验收时，保留 `experimental` 或 `candidate`，所有 approval 字段保持为空。
