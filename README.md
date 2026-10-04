# Anime Prompt Lab

漫画与动画风格生成 Prompt 研究库。

目标：通过系统化实验分析不同漫画风格的视觉语言，并建立可复用的 AI 绘画 Prompt 参数库。

## Research Direction

- Artist visual language analysis
- Line art and inking
- Character design
- Costume design
- Panel composition
- Camera language
- Prompt engineering experiments

## Structure

```
anime-prompt-lab/
├── styles/              # 漫画家/动画风格分析
├── prompt-library/      # 可复用 Prompt 组件与独立版本
├── experiments/         # 实验记录与变更记录
├── references/          # 视觉分析资料
├── templates/           # 研究与版本模板
└── prompt-versioning.md # Prompt 版本与验收规范
```

## Methodology

不直接依赖“模仿某位作者”的描述，而是拆解视觉特征：

- line quality
- character anatomy
- facial design
- shading system
- composition
- costume language
- atmosphere

然后组合生成新的视觉风格。

## Prompt 版本与验收

**满意前是 `0.x`，用户明确认可生成结果后才发布 `1.0`。** 每个独立 Prompt 单独编号，保留完整文本、模型/参数、输出和反馈，不覆盖旧版本。已有正式版之后，小优化经重新验收发布 `1.x`，重大重构经重新验收发布 `2.0`；未验收的新候选使用 `-rc.N` 后缀。

操作顺序：建立版本记录 → 实际生成 → 保存实验与用户反馈 → 按验收结果继续迭代或升版。用户满意不等于已经证明稳定复现，两者分别记录。提交文档、同意方案、AI 评分都不能代替效果验收。

入口：[版本规范](prompt-versioning.md) · [版本模板](templates/prompt-version-template.md) · [实验模板](experiments/experiment-template.md) · [变更记录](experiments/prompt-changelog.md)。

风格分析和人物名单属于研究资料，不自动视为已验证的 Prompt。未知信息保留为空；未测试写“未测试”，未验收不得创建正式 `1.0`。人工编辑及 AI/Codex 操作都应先阅读版本规范。
