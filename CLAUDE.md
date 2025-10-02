# ReaderMaster - プロジェクト開発ガイド

## 📋 プロジェクト概要

**プロジェクト名**: ReaderMaster
**目的**: スクリーンショットやPDFから抽出した情報を、物理的なテーブルで作業するような直感性で編集できるアプリケーションの開発
**現在のフェーズ**: 要件定義フェーズ（Phase 1完了）

### コアコンセプト
1. **ファイルアップロード**: PDF/画像のアップロード
2. **AI/OCR抽出**: 文章・表・図形をオブジェクトとして自動抽出
3. **インタラクティブ編集**: テーブル上でのドラッグ&ドロップ編集
4. **エクスポート**: 編集後のデータを各種形式で出力

---

## 🚨 厳守事項：ファイル配置ルール

### 必ず守るべきディレクトリ使用ルール

#### 1. 一時ファイルの配置先
```bash
/Users/tohga/Myapp/ReaderMaster/tmp/
```

**用途**:
- デバッグスクリプト
- 一時的な検証用ファイル
- 作業中の下書き
- テスト用データ
- 変換処理の中間ファイル

**ルール**:
- ✅ すべての一時ファイルは必ず`tmp/`に作成すること
- ✅ 作業完了後は不要なファイルを削除すること
- ❌ プロジェクトルートや他のディレクトリに一時ファイルを作成しない

**例**:
```bash
# ✅ 正しい
tmp/debug_script.py
tmp/test_data.json
tmp/conversion_temp.csv

# ❌ 間違い
debug.sh
test.py
temp_file.txt
```

#### 2. レポートの配置先
```bash
/Users/tohga/Myapp/ReaderMaster/report/
```

**用途**:
- 分析レポート
- 進捗報告書
- 技術調査結果
- 意思決定記録
- パフォーマンス測定結果
- レビュー記録

**ルール**:
- ✅ すべてのレポート類は必ず`report/`に配置すること
- ✅ ファイル名には日付を含めること（例: `analysis_2025-10-02.md`）
- ✅ Markdown形式を推奨
- ❌ requirements/配下にレポートを混在させない

**例**:
```bash
# ✅ 正しい
report/phase1_completion_2025-10-02.md
report/tech_stack_analysis_2025-10-03.md
report/performance_review_2025-10-05.md

# ❌ 間違い
requirements/analysis.md
phase1_report.md（ルート直下）
```

---

## 📁 プロジェクト構造

```
ReaderMaster/
├── CLAUDE.md                   # このファイル - プロジェクト開発ガイド
├── README.md                   # プロジェクト概要
├── .gitignore                  # Git除外設定
│
├── requirements/               # 要件定義フレームワーク（48ファイル）
│   ├── README.md              # 全体構造説明
│   ├── QUICKSTART.md          # 5分クイックスタート
│   ├── COMPLETION_REPORT.md   # 構築完了レポート
│   ├── PHASE1_COMPLETION.md   # Phase 1完了レポート
│   │
│   ├── 01_vision/             # プロダクトビジョン
│   ├── 02_users/              # ユーザー分析
│   ├── 03_features/           # 機能要件
│   ├── 04_ux_design/          # UX/UI設計
│   ├── 05_technical/          # 技術仕様
│   ├── 06_non_functional/     # 非機能要件
│   ├── 07_data/               # データ仕様
│   ├── 08_integration/        # 外部連携
│   ├── 09_development/        # 開発計画
│   ├── 10_risks/              # リスク管理
│   │
│   ├── _master/               # 統合管理ツール
│   │   ├── PROGRESS_TRACKER.md
│   │   ├── NEXT_ACTIONS.md
│   │   ├── DEPENDENCY_MAP.md
│   │   ├── DECISION_LOG.md
│   │   └── REQUIREMENTS_MASTER.md
│   │
│   └── _templates/            # 共通テンプレート（Phase 2用）
│
├── tmp/                        # 🚨 一時ファイル専用（厳守）
│   └── .gitkeep
│
└── report/                     # 🚨 レポート専用（厳守）
    └── .gitkeep
```

---

## 🔄 要件定義ワークフロー

### Phase 1: 構造整備 ✅ 完了
- フレームワーク構築（10カテゴリ、48ファイル）
- サブディレクトリREADME配置
- 共通テンプレート作成
- リンク整合性確保

### Phase 2: カテゴリ拡張（予定）
- 11_business/: ビジネス要件
- 12_ai_ml/: AI/ML特化要件
- 13_operations/: 運用・サポート要件

### Phase 3: 要件定義実行（今後）
推奨順序：
1. **Vision + Users** (1-2時間)
   - `01_vision/TEMPLATE.md` → `vision_v1.md`
   - `02_users/TEMPLATE.md` → `users_v1.md`

2. **Features + UX** (3-4時間)
   - `03_features/TEMPLATE.md` → `features_v1.md`
   - `04_ux_design/TEMPLATE.md` → `ux_design_v1.md`

3. **Technical + Data** (3-4時間)
   - `05_technical/TEMPLATE.md` → `technical_v1.md`
   - `07_data/TEMPLATE.md` → `data_v1.md`

4. **Non-Functional + Integration** (2-3時間)
   - `06_non_functional/TEMPLATE.md` → `non_functional_v1.md`
   - `08_integration/TEMPLATE.md` → `integration_v1.md`

5. **Development + Risks** (2-3時間)
   - `09_development/TEMPLATE.md` → `development_v1.md`
   - `10_risks/TEMPLATE.md` → `risks_v1.md`

6. **統合** (1-2時間)
   - `_master/REQUIREMENTS_MASTER.md` の完成

---

## 🛠️ 技術スタック（予定）

### フロントエンド
- **TBD**: React/Vue.js + Canvas Library (Fabric.js/Konva.js/Paper.js)
- インタラクティブキャンバスでのオブジェクト操作
- レスポンシブデザイン対応

### バックエンド
- **TBD**: Node.js/Python + AI/OCR Library
- 画像/PDF処理API
- オブジェクトメタデータ管理

### AI/OCR
- **TBD**: Tesseract.js, Google Cloud Vision API, AWS Textract など
- クライアント/サーバーハイブリッド処理検討中

### データベース
- **TBD**: PostgreSQL/MongoDB
- オブジェクトデータとメタデータ管理

### インフラ
- **TBD**: ホスティング戦略未定
- 画像ストレージ（S3/GCS等）検討中

**注**: 技術スタックは`05_technical/`カテゴリで詳細検討予定

---

## 📝 作業フロー

### 1. 要件定義カテゴリに取り組む場合

```bash
# 1. カテゴリのREADMEを確認
cd requirements/01_vision/
cat README.md

# 2. テンプレートをコピー
cp TEMPLATE.md vision_v1.md

# 3. エディタで編集
# vision_v1.md を開いてチェックリストに回答

# 4. 進捗をSTATUSに記録
# STATUS.md を更新

# 5. 重要な決定をログに記録
# ../_master/DECISION_LOG.md に追記
```

### 2. 分析やレビューを実施する場合

```bash
# 1. レポート作成（必ずreport/に配置）
# report/ux_analysis_2025-10-02.md を作成

# 2. 一時的な検証スクリプトが必要な場合
# tmp/verify_data.py を作成

# 3. 作業完了後、一時ファイルを削除
rm tmp/verify_data.py
```

### 3. 進捗確認

```bash
# 全体進捗を確認
cat requirements/_master/PROGRESS_TRACKER.md

# 次のアクションを確認
cat requirements/_master/NEXT_ACTIONS.md

# 依存関係を確認
cat requirements/_master/DEPENDENCY_MAP.md
```

---

## 🔧 Git管理ルール

### コミット前の確認事項
- [ ] 一時ファイルがtmp/に配置されている
- [ ] レポートがreport/に配置されている
- [ ] .gitignoreでtmp/が除外されている
- [ ] 不要な一時ファイルを削除した

### コミットメッセージ規約
```
[Category] Brief description

Detailed explanation if needed

- Specific change 1
- Specific change 2
```

例:
```
[Vision] Complete vision statement v1

Defined core value proposition and differentiation strategy

- Added target user segments
- Clarified key differentiators
- Set success metrics
```

### ブランチ戦略
- `main`: 安定版の要件定義
- `feature/[category-name]`: カテゴリごとの作業ブランチ

---

## 📊 進捗管理

### 現在の完了状況（2025-10-02時点）

| Phase | Status | Files | Description |
|-------|--------|-------|-------------|
| Phase 1 | ✅ 完了 | 48 | フレームワーク構築・構造整備 |
| Phase 2 | ⏳ 未着手 | - | カテゴリ拡張（11_business, 12_ai_ml, 13_operations） |
| Phase 3 | ⏳ 未着手 | - | 要件定義実行（各カテゴリのTEMPLATE記入） |

### マイルストーン

- ✅ 2025-10-02: Phase 1完了（フレームワーク構築）
- ⏳ TBD: Phase 2開始（カテゴリ拡張）
- ⏳ TBD: Vision + Users完了
- ⏳ TBD: MVP機能定義完了
- ⏳ TBD: 技術スタック決定
- ⏳ TBD: 統合要件定義書完成

---

## 🎯 MVP優先パス（最短ルート）

時間制約がある場合は、以下の順序で進めることを推奨：

```
01_vision (1時間)
    ↓
02_users (1時間)
    ↓
03_features/core_functions (2時間)
    ↓
04_ux_design/interaction_patterns (1時間)
    ↓
05_technical/architecture (1時間)
    ↓
09_development/phases (1時間)
```

**合計**: 4-6時間でMVP定義が完了

詳細は `requirements/QUICKSTART.md` を参照。

---

## 🔍 デバッグ・トラブルシューティング

### よくある問題

**Q: テンプレートの質問項目が多すぎる**
- A: すべて埋める必要はありません。80%完成度で次に進み、後で詳細化してください。

**Q: カテゴリ間の依存関係が分からない**
- A: `requirements/_master/DEPENDENCY_MAP.md` を参照してください。

**Q: どこから始めればいいか分からない**
- A: `requirements/QUICKSTART.md` の推奨フローに従ってください。

**Q: 技術的な実現可能性が不明**
- A: まず要件を定義し、技術検証は後回しにしてください。Phase 3の段階で評価します。

---

## 📚 参考リンク

### プロジェクト内ドキュメント
- [README.md](README.md) - プロジェクト概要
- [requirements/README.md](requirements/README.md) - フレームワーク全体構造
- [requirements/QUICKSTART.md](requirements/QUICKSTART.md) - 5分クイックスタート
- [requirements/_master/PROGRESS_TRACKER.md](requirements/_master/PROGRESS_TRACKER.md) - 進捗トラッカー

### GitHub
- リポジトリ: https://github.com/t-ohga/ReaderMaster.git

---

## ✅ チェックリスト：作業開始前

新しい作業を始める前に、以下を確認：

- [ ] 最新のmainブランチをpullした
- [ ] 現在のPhaseとマイルストーンを確認した
- [ ] 依存関係にある前提カテゴリが完了している
- [ ] 一時ファイルは`tmp/`に配置することを理解した
- [ ] レポートは`report/`に配置することを理解した
- [ ] `requirements/_master/NEXT_ACTIONS.md`を確認した

---

## 🚀 次のステップ

### 今すぐ始める場合

```bash
# 1. クイックスタートを読む
cd requirements/
cat QUICKSTART.md

# 2. 最初のカテゴリ（Vision）から開始
cd 01_vision/
cat README.md
cp TEMPLATE.md vision_v1.md

# 3. vision_v1.md を編集して要件定義を開始
```

### Phase 2を実施する場合

```bash
# _templates/の共通テンプレートを使用
cd requirements/
cat _templates/README.md

# 新カテゴリ作成例
mkdir 11_business/
cd 11_business/
cp ../_templates/CATEGORY_README_TEMPLATE.md README.md
# プレースホルダーを置換して内容カスタマイズ
```

---

**最終更新**: 2025-10-02
**メンテナー**: @t-ohga
**ステータス**: Phase 1完了、Phase 2準備完了
