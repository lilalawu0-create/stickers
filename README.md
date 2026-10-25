# stickers

给阿言、小克和其他 AI 使用的表情包仓库。

现有图片路径保持不变；根目录新增机器可读索引，方便 AI 按角色、情绪、动作和使用场景检索表情包。

## 内容

| 目录 | 数量 | 说明 |
|---|---:|---|
| `stickers/` | 25 | 第一批，基础猫猫情绪 |
| `stickers-batch2-part1/stickers/` | 95 | 第二批上半 |
| `stickers-batch2-part2/stickers/` | 94 | 第二批下半 |
| `stickers-batch3/stickers/` | 98 | 第三批，已去除与前两批的已知重复 |

合计 **312 张**。

## 索引

- [manifest.json](manifest.json)：机器可读的完整清单与语义标签
- [STICKERS.md](STICKERS.md)：AI 检索和选图指南
- [第一批说明](stickers/README.md)
- [第二批说明](stickers-batch2-part1/stickers/README-2.md)
- [第三批说明](stickers-batch3/stickers/README-3.md)

## 兼容性

本次整理没有移动、删除或重命名任何图片，因此已有引用不会失效。

## manifest 字段

每张图片包含：

- `id`、`file`、`path`、`batch`、`format`
- `description_zh`
- `roles`
- `emotions`
- `actions`
- `tags`

自动标签用于召回候选；最终选图仍应结合具体语境。
