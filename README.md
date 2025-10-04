# 🎰 Brain Juice - Claude Code Sound Effects

Claude Codeのタスク完了時に脳汁を出すためのジョークリポジトリです。

> **💡 Inspired by:** このリポジトリは [guchey/buhi](https://github.com/guchey/buhi) からアイデアをいただきました。素晴らしいジョークリポジトリに感謝します！

## 🎵 概要

このリポジトリは、Claude Codeのhooks機能を使用してタスク完了時に音声ファイルを再生する設定を提供します。
パチスロの効果音でタスク完了を祝い、脳汁が溢れ出します。

## 🎰 利用可能な効果音

各ディレクトリに音源ファイルと詳しい設定方法のREADMEが含まれています：

- **[puchun](./puchun/)** - パチスロのボーナス確定音「プチュン」
- **[unicooooorn](./unicorn/)** - パチスロの告知音「ユニコーーーーン！」
- **[sakibare](./sakibare/)** - パチスロの先バレ演出音
- **[sevenfura](./sevenfura/)** - パチスロのセブンフラッシュ演出音

## 📋 基本的なセットアップ手順

### 1. Claude設定ディレクトリの準備
```bash
mkdir -p ~/.claude
```

### 2. 音声ファイルの配置
好きな効果音ディレクトリから音声ファイルをコピー：
```bash
# 例: プチュン音の場合
cp puchun/puchun.m4a ~/.claude/
```

### 3. settings.jsonの設定
`~/.claude/settings.json`に設定を追加（詳細は各ディレクトリのREADMEを参照）

### 4. Claude Code再起動
設定を有効にするためにClaude Codeを再起動してください。

## 🚀 使用方法

1. 上記のセットアップを完了
2. Claude Codeでタスクを実行
3. タスク完了時に自動的に効果音が再生され、脳汁ドバドバ！

## 📝 注意事項

- macOSの`afplay`コマンドを使用しているため、macOS環境でのみ動作します
- 他のOSを使用している場合は、適切な音声再生コマンドに変更してください：
  - Windows: `powershell -c (New-Object Media.SoundPlayer "path/to/sound.wav").PlaySync()`
  - Linux: `aplay sound.wav` または `paplay sound.wav`

## 🎉 今後の追加予定

お好みのパチスロ効果音をリクエストしてください！
- リーチ音
- 告知音
- フリーズ音
- レバーON音
- その他、脳汁が溢れる効果音

## 🛠️ トラブルシューティング

詳しい設定方法やトラブルシューティングは、各効果音ディレクトリのREADMEを参照してください。

## ⚠️ 免責事項

これはパチスロ好きのためのジョークリポジトリです。職場や静かな環境での使用は十分にご注意ください！
音が鳴るたびに脳汁が溢れても責任は取れません🎰# brain-juice
