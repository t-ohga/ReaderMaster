# 🎯 次に取るべきアクション

最終更新: [未開始]

## 🚀 現在の推奨アクション

### ✅ 今すぐ開始すべきこと

```bash
📍 現在地: プロジェクト開始地点
🎯 次のステップ: 01_vision/ の検討開始
```

**理由**: すべての要件定義は、明確なビジョンから始まります。ビジョンが決まらないと、他の判断基準が定まりません。

### 📋 具体的な作業手順

#### ステップ1: Visionディレクトリに移動
```bash
cd requirements/01_vision/
```

#### ステップ2: READMEを読む
```bash
cat README.md
```
- このカテゴリで何を決めるべきか理解
- 前提条件の確認
- 期待される成果物の把握

#### ステップ3: TEMPLATEをコピーして記入開始
```bash
cp TEMPLATE.md vision_draft.md
```
- `vision_draft.md`を開く
- 各質問項目に回答していく
- チェックボックスを埋めていく

#### ステップ4: 完了後、STATUS更新
```bash
# vision_draft.md の検討完了後
# STATUS.md を更新
# _master/PROGRESS_TRACKER.md も更新
```

## 🗺️ 全体ロードマップ

### 推奨検討順序（依存関係に基づく）

```
Phase 1: 戦略とビジョン (最優先)
├─ 01_vision/           ← 【今ここから開始】
└─ 02_users/            ← visionの完了を待つ

Phase 2: 機能要件
├─ 03_features/
│   ├─ core_functions/  ← usersの完了を待つ
│   ├─ editing/         ← core_functionsの完了を待つ
│   ├─ export/          ← editingの完了を待つ
│   └─ collaboration/   ← 将来的（Phase 2では保留）
└─ 04_ux_design/
    ├─ interaction_patterns/ ← featuresの完了を待つ
    ├─ visual_design/        ← interaction_patternsの完了を待つ
    └─ accessibility/        ← visual_designの完了を待つ

Phase 3: 技術仕様
├─ 05_technical/
│   ├─ architecture/    ← ux_designの完了を待つ
│   ├─ tech_stack/      ← architectureの完了を待つ
│   ├─ infrastructure/  ← tech_stackの完了を待つ
│   └─ api_design/      ← architectureの完了を待つ
└─ 07_data/
    ├─ data_model/      ← architectureの完了を待つ
    ├─ data_flow/       ← data_modelの完了を待つ
    ├─ storage/         ← data_modelの完了を待つ
    └─ privacy/         ← storageの完了を待つ

Phase 4: 品質とエコシステム
├─ 06_non_functional/
│   ├─ performance/     ← technicalの完了を待つ
│   ├─ security/        ← technicalの完了を待つ
│   ├─ scalability/     ← technicalの完了を待つ
│   └─ reliability/     ← technicalの完了を待つ
└─ 08_integration/
    ├─ external_apis/   ← technicalの完了を待つ
    ├─ ecosystem/       ← external_apisの完了を待つ
    └─ plugins/         ← 将来的（Phase 4では保留）

Phase 5: 実行計画
├─ 09_development/
│   ├─ phases/          ← Phase 1-4の完了を待つ
│   ├─ roadmap/         ← phasesの完了を待つ
│   ├─ resources/       ← phasesの完了を待つ
│   └─ testing/         ← phasesの完了を待つ
└─ 10_risks/
    ├─ technical_risks/ ← Phase 1-4の完了を待つ
    ├─ business_risks/  ← Phase 1-4の完了を待つ
    └─ mitigation/      ← risks特定後

最終: 統合
└─ _master/
    └─ REQUIREMENTS_MASTER.md ← すべての完了を待つ
```

## 🎯 MVP（最小実行可能プロダクト）定義のための優先パス

MVPを早期に定義したい場合の**ショートカットパス**：

```
1. 01_vision/ (必須)
   ↓
2. 02_users/ (必須)
   ↓
3. 03_features/core_functions/ (必須)
   ↓
4. 04_ux_design/interaction_patterns/ (必須)
   ↓
5. 05_technical/architecture/ (必須)
   ↓
6. 09_development/phases/ (MVP定義)
```

このパスを完了すれば、**最小限のMVPスコープ**を定義できます。その後、他の詳細を埋めていくことが可能です。

## ⚠️ よくある落とし穴

### 🚫 やってはいけないこと

1. **順序を無視する**
   - ❌ 技術スタックから先に決める
   - ✅ ビジョン → ユーザー → 機能 → 技術の順

2. **並行して複数カテゴリを検討する**
   - ❌ VisionとTechnicalを同時に進める
   - ✅ 依存関係に従って順番に進める

3. **完璧主義に陥る**
   - ❌ 最初のカテゴリで100%を目指す
   - ✅ 80%の完成度で次に進み、後で戻って詳細化

4. **テンプレートを無視する**
   - ❌ 自由記述で要件を書き始める
   - ✅ TEMPLATEの質問項目に沿って検討

## 🔄 各カテゴリ完了後のチェックリスト

カテゴリの検討が完了したら、以下を確認：

- [ ] TEMPLATEのすべての質問項目に回答したか？
- [ ] 決定内容と理由を記録したか？
- [ ] STATUS.mdを更新したか？
- [ ] PROGRESS_TRACKER.mdを更新したか？
- [ ] 次のカテゴリの前提条件を満たしたか？
- [ ] DECISION_LOG.mdに重要な決定を記録したか？

## 📅 セッション管理の推奨

### 1セッションの推奨時間: 30-60分

長時間の連続検討は避け、適切な休憩を取りながら進めることを推奨します。

### セッション例

**セッション1** (30-45分)
- 01_vision/ の検討

**セッション2** (30-45分)
- 02_users/ の検討

**セッション3** (45-60分)
- 03_features/core_functions/ の検討

**セッション4** (45-60分)
- 03_features/editing/ の検討

**以降、同様に継続...**

## 🆘 困ったときの対処法

### 質問に答えられない場合
- その質問をスキップして先に進む
- STATUS.mdに「要再検討」としてマーク
- 他のカテゴリを進めることで答えが見えてくることがある

### 決定に迷う場合
- 複数の選択肢を書き出す
- それぞれのメリット・デメリットを記録
- 「仮の決定」として進め、後で見直す

### 依存関係が不明な場合
- DEPENDENCY_MAP.mdを参照
- 各カテゴリのREADMEの「前提条件」セクションを確認

---

## 🎯 今すぐ始める

準備ができたら、以下を実行してください：

```bash
cd requirements/01_vision/
cat README.md
```

**がんばってください！ 体系的に進めれば、抜け漏れのない完璧な要件定義が完成します。**
