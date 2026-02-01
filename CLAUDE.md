# YouTube Script: Volga River Environmental Destruction

## プロジェクト概要

ヴォルガ川の環境破壊についてのYouTube動画脚本を制作するプロジェクトです。ロシアの「生命線」とも呼ばれるヴォルガ川が直面する深刻な環境問題を、わかりやすく解説します。

### テーマ

「ヴォルガ川 - ロシアの生命線が直面する環境危機」

### 主要トピック

- **ヴォルガ川の重要性**: ヨーロッパ最長（3,530km）、ロシア人口の40%が流域に居住
- **産業・農業汚染**: 下水、産業廃棄物、肥料、農薬による水質汚染
- **ダム・貯水池の影響**: 8つの巨大ダムによる生態系・水流への影響
- **化学兵器工場跡地「Beloye Morye」**: 水銀、フェノール、ベンゾピレンによる深刻な汚染
- **環境修復への取り組み**: ロシア政府の「General Cleanup」プロジェクト

### 参考資料

- **主要論文**: Olson, K.R. and Chernyanskii, S.S. (2024) "The Volga River Is Russia's Lifeline and in Need of Maintenance, Mitigation and Restoration." Open Journal of Soil Science, 14, 159-179.
  - DOI: 10.4236/ojss.2024.143009
  - 場所: `docs/ojss_2024030710034147.pdf`

## ディレクトリ構造

```text
yt-script-Volga-river-environmental-destruction/
├── CLAUDE.md                 # プロジェクト設定・開発ルール
├── README.md                 # プロジェクト概要
├── Makefile                  # ビルドコマンド
├── docs/                     # 参考文献
│   └── *.pdf            # ヴォルガ川に関する学術論文
├── instructions/             # 制作ガイドライン
│   ├── video_concept.md      # 動画コンセプト（3分以内、1動画1テーマ）
│   └── youtube_script_guidelines.md  # YouTube脚本ガイドライン
├── slides-jp/                # スライド・動画関連（Reveal.js）
│   ├── index.html            # メインスライド（予定）
│   ├── yt_script.md          # YouTube動画脚本（予定）
│   ├── yt_script_tts.md      # TTS用スクリプト（予定）
│   ├── css/                  # スタイルシート
│   ├── assets/               # 画像等のアセット
│   └── dist/                 # Reveal.jsビルド成果物
└── .github/                  # GitHubテンプレート
```

## 動画フォーマット

- **尺**: 15分前後（長尺動画）
- **構成**: 1動画1テーマ
- **スタイル**: わかりやすく、丁寧に解説

詳細は `instructions/video_concept.md` を参照。

## 言語設定

このプロジェクトでは**日本語**での応答を行ってください。コード内のコメント、ログメッセージ、エラーメッセージ、ドキュメンテーション文字列なども日本語で記述してください。

## 開発ルール

### コーディング規約

- Python: PEP 8準拠
- 関数名: snake_case
- クラス名: PascalCase
- 定数: UPPER_SNAKE_CASE
- Docstring: Google Style

### Manimアニメーション

- アニメーション内のテキスト・ラベルは**日英併記**とする
  - 国際的な視聴者にも理解できるよう、日本語と英語を併記する
- テロップは**簡潔に核心を伝える**ものとする
  - 冗長な説明は避け、要点を端的に表現する
  - ナレーションの補助として機能させる

## Git運用

- ブランチ戦略: feature/*, fix/*, refactor/*
- コミットメッセージ: 英文を使用、動詞から始める
- PRはmainブランチへ

## 開発ガイドライン

### ドキュメント更新プロセス

機能追加やPhase完了時には、以下のドキュメントを同期更新する：

1. **CLAUDE.md**: プロジェクト全体状況、Phase完了記録、技術仕様
2. **README.md**: ユーザー向け機能概要、実装状況、使用方法
3. **Makefile**: コマンドヘルプテキスト（## コメント）の更新
4. **makefiles/**: コマンドヘルプテキスト（## コメント）の更新

### コミットメッセージ規約

#### コミット粒度

- **1コミット = 1つの主要な変更**: 複数の独立した機能や修正を1つのコミットにまとめない
- **論理的な単位でコミット**: 関連する変更は1つのコミットにまとめる
- **段階的コミット**: 大きな変更は段階的に分割してコミット

#### プレフィックスと絵文字

- ✨ feat: 新機能
- 🐞 fix: バグ修正
- 📚 docs: ドキュメント
- 🎨 style: コードスタイル修正
- 🛠️ refactor: リファクタリング
- ⚡ perf: パフォーマンス改善
- ✅ test: テスト追加・修正
- 🏗️ chore: ビルド・補助ツール
- 🚀 deploy: デプロイ
- 🔒 security: セキュリティ修正
- 📝 update: 更新・改善
- 🗑️ remove: 削除

**重要**: Claude Codeを使用してコミットする場合は、必ず以下の署名を含める：

```text
🤖 Generated with [Claude Code](https://claude.ai/code)

Co-Authored-By: Claude <noreply@anthropic.com>
```

## 脚本制作ガイドライン

脚本作成時は `instructions/youtube_script_guidelines.md` を参照。

### 主なポイント

- 話し言葉として書く（「読む」ではなく「聴く」ための最適化）
- 一文は20〜30文字程度
- 句読点による自然な間
- Audio Tags（ElevenLabs v3用）の活用
- 専門用語には補足説明を付ける
