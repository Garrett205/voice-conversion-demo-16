# 15 组歌声转换试听

[打开在线试听页面](https://garrett205.github.io/voice-conversion-demo-16/)

每组包含 Source、Reference、MIDI、新残差5400和新联合1600，共15组、75条WAV。页面支持按转换方向筛选，以及逐条播放和下载。

| 版本 | 内容 |
| --- | --- |
| ① MIDI | 保留MIDI，使用已修复的自然停顿与内侧Mel12衔接 |
| ② 新残差 · 5400步 | 新方法最佳残差权重，保留原RSA、Pitch Embedding与Best5250 Decoder |
| ③ 新联合 · 1600步 | 新方法最佳联合权重，加载微调后的残差、RSA、Pitch Embedding和Decoder |

十五组配对及音频沿用已验证结果。三版使用相同F0和Reference，三步精修均为20→10→5。

两组新权重先将音素事件段内的20ms软向量求平均，经过冻结PhoneFFT后按时间展开，同时将逐帧软向量输入残差。音素事件流与原版本核对一致；F0按原可见时间复用。页面用于听感比较，不作为新的端到端延迟测量。

[详细试听说明](试听说明.md) · [音频清单](demo_manifest.csv) · [文件与SHA256](manifest.json)
