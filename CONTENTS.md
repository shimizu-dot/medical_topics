# 医療トピック 資料管理ファイル

`top.html` に表示するコンテンツの一覧です。
新しいファイルを追加・更新した場合は、このファイルと `top.html` の両方を更新してください。

---

## カテゴリ一覧

| カテゴリ ID | 表示名 | フォルダ | アイコン | 色コード |
|------------|--------|----------|----------|---------|
| dermatology | 皮膚科 | `dermatology/` | 🩹 | `#c0392b` |
| diabetes | 糖尿病 | `diabetes/` | 💉 | `#2471a3` |
| glaucoma | 緑内障 | `glaucoma/` | 👁️ | `#1e8449` |
| gynecology | 婦人科 | `gynecology/` | 🌿 | `#884ea0` |
| dementia | 認知症 | `dementia/` | 🧠 | `#d35400` |
| sleep | 睡眠 | `sleep/` | 🌙 | `#2e86c1` |

---

## 皮膚科 (`dermatology/`)

| ファイル名 | タイトル | 追加日 | 備考 |
|-----------|----------|--------|------|
| `dermatology_oral_meds.html` | 皮膚科でよく使用される内服薬まとめ | 2026-06-10 | |
| `dermatology_acne_rosacea_oral_meds.html` | ざ瘡・酒皶の内服薬まとめ | 2026-06-10 | |
| `acne_treatment_additional_guidance.html` | ニキビ治療 追加情報・使い方の注意点 | 2026-06-10 | |
| `dermatology_antifungals.html` | 皮膚科領域で使用される抗真菌薬まとめ | 2026-06-10 | |
| `dermatology_antivirals.html` | 皮膚科で使用される抗ウイルス薬まとめ | 2026-06-10 | |
| `antihistamine_antiallergy_dermatology.html` | 皮膚科領域で使用される抗ヒスタミン薬・抗アレルギー薬まとめ | 2026-06-10 | |

## 糖尿病 (`diabetes/`)

| ファイル名 | タイトル | 追加日 | 備考 |
|-----------|----------|--------|------|
| `diabetes_injectables_jp_2026.html` | 糖尿病の注射剤まとめ（日本・流通製剤ベース） | 2026-06-09 | |
| `diabetes_injection_vs_oral_comparison.html` | 糖尿病治療薬：内服薬と注射剤の比較 | 2026-06-09 | |

## 緑内障 (`glaucoma/`)

| ファイル名 | タイトル | 追加日 | 備考 |
|-----------|----------|--------|------|
| `glaucoma_guidance.html` | 緑内障 点眼薬 患者指導用まとめ | 2026-06-09 | |
| `glaucoma_eye_drops_summary.html` | 緑内障治療薬と点眼方法まとめ | 2026-06-09 | |
| `glaucoma_counseling_new_pharmacist.html` | 緑内障点眼薬 服薬指導まとめ（新人薬剤師向け） | 2026-06-09 | |

## 婦人科 (`gynecology/`)

| ファイル名 | タイトル | 追加日 | 備考 |
|-----------|----------|--------|------|
| `dysmenorrhea_kampo_and_meds.html` | 生理痛（月経困難症）に使われる漢方薬・鎮痛薬・併用の整理 | 2026-06-09 | |

## 認知症 (`dementia/`)

| ファイル名 | タイトル | 追加日 | 備考 |
|-----------|----------|--------|------|
| `ninchisho_family_checksheet.html` | 認知症が心配なときの家族向けチェックシート | 2026-06-09 | |

## 睡眠 (`sleep/`)

| ファイル名 | タイトル | 追加日 | 備考 |
|-----------|----------|--------|------|
| `sleep_routine_pamphlet.html` | ぐっすり眠るための 夜の黄金ルーティン | 2026-06-09 | |

---

## ファイル追加手順

### 1. 既存カテゴリへの追加

1. 対象フォルダ（例: `dermatology/`）に HTML ファイルを配置する
2. このファイルの該当カテゴリテーブルに行を追記する
3. `top.html` の該当 `<section>` 内に `<div class="card ...">` ブロックを追記する
4. `section-count` の数値を更新する

**card ブロックのテンプレート（`top.html` へコピーして使用）:**

```html
<div class="card cat-CATEGORY">
  <a href="FOLDER/FILENAME.html">
    <span class="card-icon">EMOJI</span>
    <div>
      <div class="card-title">タイトル</div>
      <div class="card-meta">FOLDER/FILENAME.html</div>
    </div>
    <span class="card-arrow">›</span>
  </a>
</div>
```

### 2. 新カテゴリの追加

1. 新しいフォルダを作成する（例: `cardiology/`）
2. このファイルの「カテゴリ一覧」テーブルに行を追記する
3. このファイルに新しいカテゴリセクションを追加する
4. `top.html` に以下を追加する:
   - `<style>` 内に `.cat-NEW { color: #カラーコード; }` を追加
   - `<nav>` 内にアンカーリンクを追加
   - `<main>` 内に `<section class="section cat-NEW" id="NEW">` ブロックを追加
