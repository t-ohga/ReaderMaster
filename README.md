# ReaderMaster

スクリーンショットやPDFの内容を、物理的なテーブルで作業するような直感性で編集できるツール

## 🎯 プロダクトビジョン

ドキュメントから情報を抽出して編集したい人々に、物理的な作業空間と同じ直感性を持つデジタル体験を提供する

## 📋 コア機能

1. **ファイルアップロード**: PDF/画像のアップロード
2. **AI/OCR抽出**: 文章・表・図形をオブジェクトとして自動抽出
3. **インタラクティブ編集**: テーブル上でのドラッグ&ドロップ編集
4. **エクスポート**: 編集後のデータを各種形式で出力

## 🏗️ プロジェクト構造

```
AI-orchestration/
├── requirements/          # 要件定義ドキュメント
│   ├── 01_vision/        # プロダクトビジョン
│   ├── 02_users/         # ユーザー分析
│   ├── 03_features/      # 機能要件
│   ├── 04_ux_design/     # UX/UI設計
│   ├── 05_technical/     # 技術仕様
│   ├── 06_non_functional/# 非機能要件
│   ├── 07_data/          # データ仕様
│   ├── 08_integration/   # 外部連携
│   ├── 09_development/   # 開発計画
│   ├── 10_risks/         # リスク管理
│   └── _master/          # 統合管理ツール
└── README.md
```

## 🚀 開発ステータス

**現在のフェーズ**: 要件定義

- ✅ 要件定義フレームワーク構築完了
- ⏳ 要件定義作業中
- ⏳ 技術スタック選定
- ⏳ プロトタイプ開発
- ⏳ MVP開発

## 📖 ドキュメント

### クイックスタート

```bash
cd requirements/
cat QUICKSTART.md
```

### 要件定義の進め方

1. [QUICKSTART.md](requirements/QUICKSTART.md) - 5分で始めるガイド
2. [README.md](requirements/README.md) - 全体構造の説明
3. [NEXT_ACTIONS.md](requirements/_master/NEXT_ACTIONS.md) - 次にやるべきこと

## 🛠️ 技術スタック（予定）

### フロントエンド
- TBD: React/Vue.js + Canvas Library (Fabric.js/Konva.js/Paper.js)

### バックエンド
- TBD: Node.js/Python + AI/OCR Library

### AI/OCR
- TBD: Tesseract.js, Google Cloud Vision API, AWS Textract など

### データベース
- TBD: PostgreSQL/MongoDB

## 📝 ライセンス

TBD

## 👥 コントリビューター

- [@t-ohga](https://github.com/t-ohga)

---

**最終更新**: 2025-10-02
