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
├── prompt-library/      # 可复用 Prompt 组件
├── experiments/         # 实验记录
├── references/          # 视觉分析资料
└── templates/           # 研究模板
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
