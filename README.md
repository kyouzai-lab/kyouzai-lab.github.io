# 教材ラボ（仮）

kyouzai-lab の教材一覧サイト。https://kyouzai-lab.github.io/

## 教材を足すとき

1. 教材の画面を撮って `shots/（id）.webp` に置く（横:縦 = 約10:7、幅800pxくらい）
2. `data/kyouzai.json` の `items` の最後に1件足す

```json
{
  "id": "new-kyouzai",
  "title": "教材の名前",
  "kind": "授業で使う",
  "subjects": ["算数"],
  "grades": [5],
  "unit": "単元名",
  "desc": "一行の説明。",
  "url": "https://kyouzai-lab.github.io/new-kyouzai/",
  "image": "shots/new-kyouzai.webp"
}
```

- `kind` は「授業で使う」「クラスで遊ぶ」「授業の道具」のどれか
- `subjects` に「全教科」と書くと、どの教科で絞りこんでも出る
- `grades` に 1〜6 をぜんぶ入れると「全学年」と表示される
- 教科の色は index.html の `--s-国語` などで決めている（新しい教科を足すときは色も1行足す）
- json を直したら index.html の `kyouzai.json?v=` の数字を上げると、すぐ反映される
