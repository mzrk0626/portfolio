# 研究プロフィールサイト テンプレート

プロフィールサイトのテンプレートです。

## 🚀 使い方

### 1. ファイルの準備

```
my_study_page/
├── index.html      # メインHTMLファイル
├── styles.css      # メインスタイルシート
├── config.css      # カスタマイズ設定ファイル
├── script.js       # JavaScript
├── profile.jpg     # プロフィール画像（追加してください）
└── README.md       # このファイル
```

### 2. プロフィール画像の追加

`profile.jpg` という名前でプロフィール画像を同フォルダに配置してください。

### 3. 基本情報のカスタマイズ

#### HTML ファイル（index.html）の編集箇所

**1. サイト情報（要カスタマイズ）**

```html
<title>あなたの名前 | 研究プロフィール</title>
<meta name="description" content="あなたの研究紹介..." />
```

**2. プロフィール情報（要カスタマイズ）**

```html
<h1 class="title">
  あなたの名前
  <span class="muted">Your Name</span>
</h1>
<p class="subtitle">所属・研究テーマを記載</p>
```

**3. 研究キーワード（要カスタマイズ）**

```html
<div class="chips">
  <span class="chip">キーワード1</span>
  <span class="chip">キーワード2</span>
  <!-- 必要に応じて追加 -->
</div>
```

**4. 外部リンク（要カスタマイズ）**

```html
<a class="btn link-btn" href="https://github.com/your-username"> GitHub </a>
```

### 4. セクション別カスタマイズ

#### 論文・発表の追加

```html
<article class="item pub">
  <div class="row">
    <span class="badge">会議名</span>
    <span class="meta">年</span>
  </div>
  <h3 class="title">論文タイトル</h3>
  <div class="authors">著者名</div>
</article>
```

#### 受賞歴の追加

```html
<div class="card pad list">
  <div class="t">
    <div class="item">
      <strong>賞の名前</strong>
      <div class="meta">年 / 主催者</div>
    </div>
  </div>
</div>
```

#### 学歴の追加

```html
<div class="t">
  <div class="item">
    <strong>学校名・学部名</strong>
    <div class="meta">期間 | 学位</div>
  </div>
</div>
```

#### 資格の追加

```html
<div class="list">
  <div class="item">
    <div class="row">
      <span class="badge">資格</span>
      <strong>資格名</strong>
    </div>
    <div class="meta">取得年月・詳細情報</div>
  </div>
</div>
```

### 5. 色・デザインのカスタマイズ

このテンプレートでは、2 つの方法でデザインをカスタマイズできます。

#### 方法 1: config.css を使用（推奨）

**簡単なカスタマイズには `config.css` を編集してください。**

`config.css` ファイルには、よく変更される設定項目がまとまっています：

```css
:root {
  /* カラーパレット */
  --custom-accent: #60a5fa; /* アクセント色（青） */
  --custom-accent-2: #22d3ee; /* サブアクセント色（シアン） */
  --custom-bg: #0b1220; /* 背景色 */
  --custom-text: #e6ecf8; /* 文字色 */

  /* サイズ設定 */
  --custom-radius-lg: 20px; /* 角丸サイズ */
  --custom-container-width: 1100px; /* コンテナ最大幅 */

  /* レスポンシブ設定 */
  --custom-breakpoint-mobile: 860px; /* モバイル切り替え幅 */
}
```

**カスタマイズ例:**

```css
/* 赤系のアクセント色に変更 */
--custom-accent: #ff6b6b;
--custom-accent-2: #4ecdc4;

/* よりコンパクトなデザインに */
--custom-radius-lg: 10px;
--custom-container-width: 800px;

/* フォントを変更 */
--custom-font-family: "Times New Roman", serif;
```

#### 方法 2: styles.css を直接編集（上級者向け）

#### 方法 2: styles.css を直接編集（上級者向け）

より詳細なカスタマイズが必要な場合は、`styles.css` の CSS 変数を直接変更できます：

```css
:root {
  /* 色の変更 */
  --acc: #60a5fa; /* アクセント色 */
  --acc-2: #22d3ee; /* サブアクセント色 */
  --bg: #0b1220; /* 背景色 */

  /* サイズの変更 */
  --radius-lg: 20px; /* 角丸サイズ */
}
```

#### ファイル構成とカスタマイズの関係

```
my_study_page/
├── config.css      # 🎨 簡単カスタマイズ用（推奨）
├── styles.css      # 🔧 詳細カスタマイズ用
├── index.html      # 📝 内容変更用
└── script.js       # ⚙️ 機能追加用
```

**カスタマイズの優先順位:**

1. `config.css` の設定が最優先
2. `config.css` に設定がない場合は `styles.css` のデフォルト値を使用

#### よく使われるカスタマイズ例

**1. 緑系の研究テーマに合わせたカラー**

```css
/* config.css に追加 */
--custom-accent: #10b981; /* 緑色 */
--custom-accent-2: #06b6d4; /* 青緑色 */
```

**2. 赤系の医学・生物学テーマ**

```css
--custom-accent: #ef4444; /* 赤色 */
--custom-accent-2: #f59e0b; /* オレンジ色 */
```

**3. 紫系の理論・数学テーマ**

```css
--custom-accent: #8b5cf6; /* 紫色 */
--custom-accent-2: #ec4899; /* ピンク色 */
```

**4. コンパクトなデザイン**

```css
--custom-container-width: 900px; /* 幅を狭く */
--custom-radius-lg: 12px; /* 角丸を小さく */
```

## 🎨 オプション機能

### CV ダウンロードリンク

`cv.pdf` ファイルを同フォルダに配置し、以下の HTML を追加：

```html
<a id="cv-link" class="btn primary">CV ダウンロード</a>
```

### テーマ切替ボタン

以下の HTML を追加すると、手動でテーマを切り替えできます：

```html
<button id="themeToggle" class="btn">テーマ切替</button>
```

### キーワードハイライト機能

論文エントリーにタグを追加すると、キーワードクリックで関連論文がハイライトされます：

```html
<article class="item pub" data-tags="機械学習;深層学習">
  <!-- 論文内容 -->
</article>
```

## 📱 レスポンシブ対応

- **デスクトップ**: 1100px 最大幅
- **タブレット**: 860px 以下で 2 カラム →1 カラム
- **モバイル**: 最適化されたタッチインターフェース

## ♿ アクセシビリティ

- セマンティック HTML
- ARIA ラベル対応
- キーボードナビゲーション
- 色覚多様性対応
- スクリーンリーダー対応

## 🔧 技術仕様

- **HTML5**: セマンティックマークアップ
- **CSS3**: CSS Grid, Flexbox, CSS 変数
- **JavaScript**: ES6+, DOM 操作
- **依存関係**: なし（純粋な HTML/CSS/JS）

## 📄 ライセンス

このテンプレートは自由に使用・改変していただけます。

## 🆘 サポート

問題が発生した場合は、各ファイルのコメントを参考にしてください。カスタマイズ箇所には「要カスタマイズ」のコメントが付いています。

---

**Happy Coding! 🚀**
