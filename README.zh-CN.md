# 镜语：电影感视觉叙事

[English](README.md)

一个面向 Codex 的电影感视觉生成技能。它把故事节点、人物、场景或产品创意转化为具有镜头语言的图像生成提示词，重点是叙事、真实光线和人物连续性，而不是堆叠“电影感”滤镜词。

适用于微电影分镜、故事板、剧情关键帧、人物氛围图和高质感产品叙事图。

## 能做什么

- 把情节转化成明确的镜头、构图、光线与情绪方向。
- 根据叙事目的选择景别、视角、可用光、色彩和材质细节。
- 为多镜头序列锁定人物、服装、道具、地点、时间和画面基调。
- 使用“克制独立电影”基线减少 AI 味：生活化地点、自然曝光、非摆拍动作、正常皮肤和略不完美的构图。
- 提供室内戏、雨夜外景、动作、史诗空间和产品图的可复用镜头配方。

## 安装

将技能目录复制到 Codex 技能目录：

```powershell
Copy-Item -Recurse .\cinematic-visual-generation "$HOME\.codex\skills\cinematic-visual-generation"
```

刷新或重启 Codex 后即可发现该技能。

## 使用方式

显式调用：

```text
Use $cinematic-visual-generation to create a 6-shot micro-film storyboard about a night-shift worker returning a lost key.
```

也可以直接用自然语言描述：

```text
生成一张克制、真实的电影感画面：一个人在雨夜等末班车。
```

如果已有信息，尽量提供人物、动作、地点和情绪；其余普通制作细节由技能补全。

## 去 AI 味：克制独立电影模式

当画面显得过度精致、像海报或“AI 味”太重时，使用下面的约束：

- 采用平视 35–50 mm，允许前景遮挡、微妙歪斜或不完全对称的构图。
- 只使用窗光、路灯、荧光灯、车厢灯等可解释的现场光源。
- 保持低饱和、正常肤质和真实曝光，不把雨、雾或泪水夸张化。
- 捕捉整理围巾、擦雨、停步、回头等小动作，避免时尚摆拍与戏剧化表情。

示例：

```text
Use $cinematic-visual-generation. A woman waits alone at a worn suburban station in light rain. Keep it observational and low-saturation: available fluorescent light, an off-centre 40 mm frame, chipped paint, wet tiles, unretouched skin, no glamour or poster composition.
```

## 项目结构

```text
cinematic-visual-generation/
├── SKILL.md                    # 触发描述与核心工作流
├── agents/openai.yaml           # Codex 界面元数据
└── references/shot-recipes.md   # 可复用镜头配方与修正策略
```

## 限制与迭代

图像模型仍可能在人物一致性、小道具和文字渲染上出现偏差。迭代时先定位最大的一个问题——例如构图、动作、光线或角色一致性——再做针对性修改，不要不断叠加泛化形容词。

请不要要求模仿在世艺术家的可识别风格；用可观察的画面特征替代，例如克制对称、自然实用光、低饱和或缓慢紧张感。

## 参与贡献

参见 [CONTRIBUTING.md](CONTRIBUTING.md)。请保持 `SKILL.md` 简洁，把可复用的长示例和类型配方放入 `references/`。

## 许可证

本项目采用 [MIT License](LICENSE)。
