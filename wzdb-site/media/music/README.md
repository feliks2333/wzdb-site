# media/music — 音乐文件放这里

把 **mp3** 直接放进这个目录（不要再建子目录，路径要和 `works.js` 里写的一致）。

## 现在的示例条目对应文件名

| works.js 里的 id | 现在写的路径 | 你要放的文件 |
| --- | --- | --- |
| `MUS-001` | `media/music/01-immersion-protocol.mp3` | `01-immersion-protocol.mp3` |
| `MUS-002` | `media/music/02-cold-start-sequence.mp3` | `02-cold-start-sequence.mp3` |

两种补法，任选一种：

1. **照抄文件名**：把文件改名成上面表格里的名字，放进来就能直接播放，什么都不用改。
2. **改路径**：文件名保持你自己的，去 `assets/js/works.js` 的 `music[]` 里把 `src` 改成你的文件名，
   例如 `src: 'media/music/我的曲子.mp3'`。

## 加新曲子

复制一整段音乐条目对象，改 `id`（不能重复）、`title`、`artist`、`src` 等字段。
想让某个作品关联到它，就在 `works[]` 里那条作品的 `music: []` 里填上这个 `id`。

## 建议

- 采样率 44.1kHz、比特率 128–320kbps 的 mp3 兼容性最好。
- 文件名尽量用英文 + 短横线，避免空格和中文（本地一般没问题，但部署到服务器后偶发编码问题）。
- `duration` 字段不用手填，播放器读到真实文件后会自动覆盖显示。
- 文件还没放进来时，歌单条目会标记 `OFFLINE`，状态显示 `MEDIA_MISSING`，属正常现象。
