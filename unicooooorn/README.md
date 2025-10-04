# 🦄 ユニコーン - パチスロのあの音

「ユニコーーーーン！」でタスク完了を盛り上げよう！

## 🎵 音源について

この音声ファイルはパチスロの「ユニコーン」告知音です。
タスクが完了するたびに熱い演出が脳内で展開されます。

## 📋 セットアップ手順

### 1. 音声ファイルのコピー

```bash
cp unicooooorn/unicorn.m4a ~/.claude/
```

### 2. settings.jsonの設定

`~/.claude/settings.json`に以下を追加：

```json
{
  "hooks": {
    "Stop": [
      {
        "matcher": "",
        "hooks": [
          {
            "type": "command",
            "command": "afplay ~/.claude/unicorn.m4a"
          }
        ]
      }
    ]
  }
}
```

### 3. 動作テスト

設定を反映させる前に、音声ファイルが正しく配置されているか確認：

```bash
# 音声ファイルが正しくコピーされているか確認
ls -la ~/.claude/unicorn.m4a

# 音声が再生されるかテスト
afplay ~/.claude/unicorn.m4a
```

### 4. Claude Codeを再起動

設定を反映させるためにClaude Codeを再起動してください。

## 🎉 使い方

1. セットアップ完了後、Claude Codeでタスクを実行
2. タスク完了時に自動的に「ユニコーーーーン！」音が再生される
3. 激アツ演出で脳汁ドバドバ！🦄

## 🎚️ 音量調整

音量を調整したい場合：

```json
{
  "type": "command",
  "command": "afplay -v 0.5 ~/.claude/unicorn.m4a"
}
```

`-v`の値は0.0〜1.0で指定（0.5 = 50%音量）

## 📝 注意事項

- macOSの`afplay`コマンドを使用しているため、macOS環境でのみ動作します
- 他のOSを使用している場合は、適切な音声再生コマンドに変更してください：
  - Windows: `powershell -c (New-Object Media.SoundPlayer "path/to/unicorn.wav").PlaySync()`
  - Linux: `aplay unicorn.wav` または `paplay unicorn.wav`

## 💡 Tips

- この音は結構大きいので職場での使用は要注意
- イヤホン強く推奨
- 深夜帯は絶対に音量注意
- 周りに人がいる時は控えめに
