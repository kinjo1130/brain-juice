# ⚡ 先バレ - パチスロの先バレ音

先バレ演出でタスク完了を予告！

## 🎵 音源について

この音声ファイルはパチスロの先バレ演出音です。
タスクが完了する前から期待感を煽り、脳汁が溢れ出します。

## 📋 セットアップ手順

### 1. 音声ファイルのコピー

```bash
cp sakibare/sakibare.m4a ~/.claude/
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
            "command": "afplay ~/.claude/sakibare.m4a"
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
ls -la ~/.claude/sakibare.m4a

# 音声が再生されるかテスト
afplay ~/.claude/sakibare.m4a
```

### 4. Claude Codeを再起動

設定を反映させるためにClaude Codeを再起動してください。

## 🎉 使い方

1. セットアップ完了後、Claude Codeでタスクを実行
2. タスク完了時に自動的に先バレ演出音が再生される
3. 期待感MAXで脳汁ドバドバ！⚡

## 🎚️ 音量調整

音量を調整したい場合：

```json
{
  "type": "command",
  "command": "afplay -v 0.5 ~/.claude/sakibare.m4a"
}
```

`-v`の値は0.0〜1.0で指定（0.5 = 50%音量）

## 📝 注意事項

- macOSの`afplay`コマンドを使用しているため、macOS環境でのみ動作します
- 他のOSを使用している場合は、適切な音声再生コマンドに変更してください：
  - Windows: `powershell -c (New-Object Media.SoundPlayer "path/to/sakibare.wav").PlaySync()`
  - Linux: `aplay sakibare.wav` または `paplay sakibare.wav`

## 💡 Tips

- 先バレは期待度が高いので、重要なタスクにおすすめ
- イヤホン推奨
- 深夜帯は音量注意
