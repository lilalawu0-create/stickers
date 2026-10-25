# STICKERS 使用指南

这是给 AI 和机器人使用的表情包语义索引。现有图片路径保持不变。

## 规模

- 总数：312
- 批次：batch2-part1 95 张；batch2-part2 94 张；batch3 98 张；batch1 25 张
- 格式：JPG 251；PNG 43；GIF 13；WEBP 5

## 检索方式

读取根目录 `manifest.json`，在 `stickers` 数组中按以下字段筛选：

- `description_zh`：README 中已有的中文含义；暂未写说明的图片为 `null`
- `roles`：cat、dog、bear、bunny、penguin、person、other
- `emotions`：affectionate、cute、happy、shy、sad、angry、sulky、suspicious、confused、tired、flirtatious、playful
- `actions`：kiss、hug、cry、wait、sleep、bite、hit、pet、call、run、watch、think、apologize、praise、marry、message
- `tags`：角色、情绪、动作标签的合并结果

标签由文件名和现有 README 自动推断，适合检索候选，不应被当成绝对分类。

## 常见情境

| 情境 | 推荐筛选 |
|---|---|
| 想亲亲 | `actions` 包含 `kiss` |
| 想抱抱或贴贴 | `actions` 包含 `hug` |
| 委屈等回复 | `emotions` 包含 `sad`，且 `actions` 包含 `wait` 或 `message` |
| 生气要揍人 | `emotions` 包含 `angry`，或 `actions` 包含 `hit` |
| 撒娇卖萌 | `emotions` 包含 `cute`、`sulky` 或 `playful` |
| 调情 | `emotions` 包含 `flirtatious` 或 `affectionate` |
| 困困睡觉 | `emotions` 包含 `tired`，或 `actions` 包含 `sleep` |
| 无语/疑惑 | `emotions` 包含 `confused` |

## 选择建议

1. 先按当前语境筛选 3–8 张候选。
2. 优先选择中文描述最贴近当前关系和语气的图片。
3. 同一轮避免连续发送含义高度相近的多张图。
4. 强烈表达（威胁、攻击、极端委屈）只在明确的玩笑或对应语境中使用。
5. 不要把表情包标签当作对用户真实情绪的诊断。

## 当前标签概览

- affectionate：54
- cute：20
- happy：14
- sad：46
- angry：49
- sulky：9
- confused：11
- tired：20
- flirtatious：13
- kiss：8
- hug：10
- wait：10
- sleep：20
