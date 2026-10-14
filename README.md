# ASS-effects

一组 ASS 字幕特效脚本模板：卡拉OK逐字特效、矢量绘图变形、抖动与残影。

### ⚠️ 部分需要安装Yutils和VSFilterMod




## 文件说明

| 文件 | 效果 |
| --- | --- |
| [`ass/1.ass`](ass/1.ass) | 逐层裁切 + `\move`，文字分条向上推出 |
| [`ass/2.ass`](ass/2.ass) | 逐字随机矩形遮罩 + `\clip` 逐帧模糊闪烁 |
| [`ass/3.ass`](ass/3.ass) | 逐层裁切擦除 + `\jitter` 抖动（**需要 VSFilterMod**） |
| [`ass/4.ass`](ass/4.ass) | 逐字矢量绘图 + `shape.filter` 正弦波纹扭曲 |
| [`ass/5.ass`](ass/5.ass) | 用 Layer 1–120 叠出多层残影拖尾 |
| [`ass/6.ass`](ass/6.ass) | 文字转轮廓后沿贝塞尔曲线飞散 |

应该会持续更新

## 许可

[MIT](LICENSE)
