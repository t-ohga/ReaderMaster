# 📝 共通テンプレート集

このディレクトリには、新しいカテゴリやサブカテゴリを追加する際に使用できる**再利用可能なテンプレート**が含まれています。

## 🎯 目的

- 新しいカテゴリを追加する際の一貫性を保つ
- ドキュメント作成の手間を削減
- 抜け漏れのない要件定義を支援

## 📂 テンプレート一覧

| テンプレート | 用途 | 使い方 |
|------------|------|-------|
| **CATEGORY_README_TEMPLATE.md** | カテゴリのREADME作成 | コピーして[カテゴリ番号]_[カテゴリ名]/README.mdとして配置 |
| **CATEGORY_TEMPLATE_TEMPLATE.md** | カテゴリのTEMPLATE作成 | コピーして[カテゴリ番号]_[カテゴリ名]/TEMPLATE.mdとして配置 |
| **CATEGORY_STATUS_TEMPLATE.md** | カテゴリのSTATUS作成 | コピーして[カテゴリ番号]_[カテゴリ名]/STATUS.mdとして配置 |

## 🚀 使い方

### 新しいカテゴリを追加する場合

#### ステップ1: ディレクトリ作成
```bash
mkdir requirements/11_[カテゴリ名]/
```

#### ステップ2: テンプレートをコピー
```bash
cd requirements/11_[カテゴリ名]/
cp ../_templates/CATEGORY_README_TEMPLATE.md README.md
cp ../_templates/CATEGORY_TEMPLATE_TEMPLATE.md TEMPLATE.md
cp ../_templates/CATEGORY_STATUS_TEMPLATE.md STATUS.md
```

#### ステップ3: プレースホルダーを置換

各ファイル内の以下のプレースホルダーを実際の値に置き換えてください:

- `[カテゴリ番号]`: 例: `11`
- `[カテゴリ名]`: 例: `business`
- `[日本語カテゴリ名]`: 例: `ビジネス要件`
- `[カテゴリの目的]`: 例: `ビジネス目標と収益モデルの明確化`
- `[決定事項1]`, `[決定事項2]`, etc.: 具体的な決定事項名
- `[前提カテゴリ1]`, etc.: 依存する他のカテゴリ
- `[次のカテゴリ]`: 依存関係で次に進むべきカテゴリ

#### ステップ4: 内容のカスタマイズ

テンプレートをベースに、カテゴリ固有の内容を追加・編集してください。

#### ステップ5: 統合管理ツールの更新

以下のファイルを更新して、新しいカテゴリを統合してください:

- `_master/PROGRESS_TRACKER.md`: 新カテゴリの進捗行を追加
- `_master/DEPENDENCY_MAP.md`: 依存関係を追加
- `_master/NEXT_ACTIONS.md`: 推奨順序に組み込む
- `README.md`: ディレクトリ構造セクションに追加

---

## 💡 カスタマイズのヒント

### README.mdのカスタマイズ

- **🎯 このカテゴリで決めること**: カテゴリ固有の決定事項を3-5個リストアップ
- **📝 前提条件**: 依存する他のカテゴリを明記
- **💡 検討のヒント**: よくある落とし穴と良い例を追加

### TEMPLATE.mdのカスタマイズ

- **セクション構成**: カテゴリの性質に応じてセクションを追加・削除
- **質問項目**: チェックリスト形式で具体的な質問を用意
- **テーブル**: 比較や選定が必要な場合はテーブル形式を活用

### STATUS.mdのカスタマイズ

- **完了チェックリスト**: カテゴリ固有の完了条件を追加
- **作業ログ**: 実際の進捗に合わせて更新

---

## 📋 カテゴリ追加の例

### 例: 11_business/（ビジネス要件）を追加

```bash
# ディレクトリ作成
mkdir requirements/11_business/

# テンプレートをコピー
cd requirements/11_business/
cp ../_templates/CATEGORY_README_TEMPLATE.md README.md
cp ../_templates/CATEGORY_TEMPLATE_TEMPLATE.md TEMPLATE.md
cp ../_templates/CATEGORY_STATUS_TEMPLATE.md STATUS.md

# プレースホルダーを置換（例: sedコマンド使用）
sed -i '' 's/\[カテゴリ番号\]/11/g' *.md
sed -i '' 's/\[カテゴリ名\]/business/g' *.md
sed -i '' 's/\[日本語カテゴリ名\]/ビジネス要件/g' *.md

# 内容をカスタマイズ（エディタで編集）
```

---

## 🔗 関連ドキュメント

- **../README.md**: 全体構造の説明
- **../_master/PROGRESS_TRACKER.md**: 進捗管理
- **../_master/DEPENDENCY_MAP.md**: 依存関係マップ

---

## 📞 サポート

テンプレートの使い方で困った場合:

1. 既存のカテゴリ（01_vision ~ 10_risks）を参考にする
2. `../README.md`の全体構造を確認する
3. Claude Codeに相談する

---

**次のステップ**: 新しいカテゴリを追加する必要が出たら、このテンプレート集を活用してください。
