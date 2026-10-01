# media/video — 视频文件放这里

把 **mp4** 直接放进这个目录（不要再建子目录）。

## 现在的示例条目对应文件名

| works.js 里的 id | 现在写的路径 | 你要放的文件 |
| --- | --- | --- |
| `VID-001` | `media/video/01-field-test.mp4` | `01-field-test.mp4` |
| `VID-002` | `media/video/02-terminal-loop.mp4` | `02-terminal-loop.mp4` |

两种补法，任选一种：

1. **照抄文件名**：把文件改名成上面表格里的名字，放进来即可播放。
2. **改路径**：去 `assets/js/works.js` 的 `videos[]` 里把 `src` 改成你自己的文件名。

## 封面（poster）

封面图放在 **`media/cover/`**，不是这个目录。
在 `videos[]` 里用 `poster` 字段指向它，例如 `poster: 'media/cover/vid-001.jpg'`。

## 编码建议

- 容器 `mp4`，视频 `H.264 (AVC)`，音频 `AAC`；这是浏览器兼容性最好的组合。
- H.265 / HEVC、AVI、MKV 在多数浏览器里放不了，需要先转码。
- 时长较长的片子建议码率控制在 3–6 Mbps，否则本地加载会卡。
- 需要自动循环播放的展场片段，把 `runtime` 写清并配合影像室的 `LOOP:ONE` 使用。

## 读不到文件时

条目会标记 `OFFLINE`、状态显示 `MEDIA_MISSING`，监视器上会保留封面占位块，页面不会出错。
