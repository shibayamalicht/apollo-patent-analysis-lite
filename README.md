# 🚀 APOLLO Lite: Simple Patent Map Generator

**APOLLO Lite** is a lightweight, browser-based patent analysis tool. No server or installation required - just open the HTML file to start analyzing patent data instantly.

**APOLLO Lite** は、ブラウザだけで動作する軽量な特許分析ツールです。サーバーやインストール不要で、HTMLファイルを開くだけで特許データの分析をすぐに開始できます。

---

## 💡 Inspiration (インスピレーション)

The browser-based approach of APOLLO Lite was inspired by **[ARTEMIS](https://github.com/ipscience/artemis)** by Hajime Kumami ([@ipscience](https://github.com/ipscience)). ARTEMIS demonstrated the powerful potential of running patent analysis tools entirely in the browser using PyScript/Pyodide, without requiring any server-side infrastructure.

APOLLO Lite のブラウザベースアプローチは、Hajime Kumami氏（[@ipscience](https://github.com/ipscience)）による **[ARTEMIS](https://github.com/ipscience/artemis)** からインスピレーションを受けています。ARTEMISは、PyScript/Pyodideを活用し、サーバーサイドのインフラを必要とせずにブラウザ上で特許分析ツールを実行できるという大きな可能性を示しました。

---

## ✨ Features (特徴)

- 🌐 **Fully Browser-Based**: No server, no installation, no dependencies.
  * *完全ブラウザ動作*: サーバー不要、インストール不要、依存関係なし。
- 📁 **Single HTML File**: Everything in one portable file.
  * *シングルHTMLファイル*: すべてが1つのポータブルなファイルに。
- 🔒 **Privacy-First**: Your data never leaves your browser.
  * *プライバシー保護*: データはブラウザ外に一切送信されません。
- ⚡ **Instant Analysis**: Upload CSV and start visualizing immediately.
  * *即座に分析開始*: CSVをアップロードしてすぐに可視化。

---

## 🧩 Analysis Modules (分析モジュール)

### 1. 📁 Data Import (データ読込)
The entry point for all analyses.
全ての分析の出発点です。
* **CSV Upload**: Drag & drop or click to upload patent data.
  * *CSVアップロード*: ドラッグ＆ドロップまたはクリックでアップロード。
* **Smart Mapping**: Automatically detects column mappings (Date, Applicant, IPC, Title).
  * *スマートマッピング*: カラム（日付、出願人、IPC、名称）を自動検出。
* **Flexible Settings**: Configurable delimiter for multi-value fields.
  * *柔軟な設定*: 複数値フィールドの区切り文字を設定可能。

### 2. 📈 Timeline (時系列分析)
Visualizes filing trends over time.
出願件数の時系列推移を可視化します。
* **Chart Types**: Bar chart or Line chart.
  * *グラフ種類*: 棒グラフまたは折れ線グラフ。
* **Status Breakdown**: Stacked chart by legal status (if available).
  * *ステータス内訳*: 法的状態別の積み上げ表示（設定時）。
* **Year Range Filter**: Adjustable start/end year.
  * *年範囲フィルタ*: 開始年・終了年の調整。

### 3. 👥 Applicant Ranking (出願人ランキング)
Identifies top patent filers.
主要な特許出願人を特定します。
* **Top N Display**: Show top 5/10/15/20/30 applicants.
  * *Top N表示*: 上位5/10/15/20/30社を表示。
* **Status Breakdown**: Stacked chart by legal status.
  * *ステータス内訳*: 法的状態別の積み上げ表示。
* **Click-to-Detail**: Click a bar to see the patent list.
  * *クリック詳細*: バーをクリックして公報リストを表示。

### 4. 🏷️ IPC Ranking (IPC分類ランキング)
Analyzes technology distribution by IPC.
IPC分類による技術分布を分析します。
* **Hierarchy Levels**: Subclass (A01B) or Main Group (A01B1/00).
  * *階層レベル*: サブクラス（A01B）またはメイングループ（A01B1/00）。
* **Top N Display**: Configurable ranking depth.
  * *Top N表示*: ランキング表示件数を設定可能。

### 5. 🔥 Matrix Analysis (マトリクス分析)
Cross-tabulation analysis with multiple axes.
複数の軸を使ったクロス集計分析です。
* **Flexible Axes**: Year, Applicant, IPC, Technology, Problem, Solution, Status.
  * *柔軟な軸設定*: 年、出願人、IPC、技術分類、課題、解決手段、ステータス。
* **Visualization**: Heatmap or Bubble chart.
  * *可視化*: ヒートマップまたはバブルチャート。
* **Click-to-Detail**: Click a cell/bubble to see the patent list.
  * *クリック詳細*: セル/バブルをクリックして公報リストを表示。
* **Smart Labels**: Dynamic margin adjustment to prevent label overlap.
  * *スマートラベル*: ラベル重複を防ぐ動的マージン調整。

### 6. 🌳 Treemap (ツリーマップ)
Hierarchical composition visualization.
階層的な構成比を可視化します。
* **IPC Hierarchy**: Section → Class → Subclass drill-down.
  * *IPC階層*: セクション→クラス→サブクラスのドリルダウン。
* **Applicant Share**: Top N applicant composition.
  * *出願人シェア*: Top N出願人の構成比。

### 7. 🔄 Lifecycle Map (ライフサイクルマップ)
Technology maturity assessment.
技術の成熟度を評価します。
* **X-Axis**: Number of applications (technology activity).
  * *横軸*: 出願件数（技術活動量）。
* **Y-Axis**: Number of applicants (market players).
  * *縦軸*: 出願人数（参入プレイヤー数）。
* **Trajectory**: Year-by-year evolution path.
  * *軌跡*: 年次推移の軌跡表示。

---

## 📋 Data Requirements (データ要件)

### Required Columns (必須カラム)
| Column | Description | 説明 |
|--------|-------------|------|
| Date | Filing or Publication date | 出願日または公開日 |
| Applicant | Applicant/Assignee name | 出願人/権利者名 |
| IPC | IPC Classification | IPC分類 |
| Title | Invention title | 発明の名称 |

### Optional Columns (任意カラム)
| Column | Description | 説明 |
|--------|-------------|------|
| Application Number | For detail display | 詳細表示用 |
| Technology Class | Custom classification | 独自の技術分類 |
| Problem Class | Problem-based classification | 課題分類 |
| Solution Class | Solution-based classification | 解決手段分類 |
| Status | Legal status | 法的状態・ステータス |

### Supported Formats (対応形式)
* **File**: CSV (UTF-8 / Shift_JIS)
* **Delimiter**: Comma
* **Multi-value Separator**: Semicolon (;) - configurable

---

## 🚀 How to Use (使い方)

1. **Download** `apollo_lite_v1.0.0.html`
   * `apollo_lite_v1.0.0.html` をダウンロード
2. **Open** in a modern browser (Chrome/Edge/Firefox recommended)
   * モダンブラウザで開く（Chrome/Edge/Firefox推奨）
3. **Upload** your patent CSV file
   * 特許データのCSVファイルをアップロード
4. **Configure** column mappings (auto-detected)
   * カラムマッピングを設定（自動検出）
5. **Analyze** using each tab
   * 各タブで分析を実行

---

## 🛠️ Technical Stack (技術スタック)

* **PyScript 2024.1.1** - Python in the browser
* **Plotly.js 2.27.0** - Interactive visualizations
* **Pandas** - Data manipulation (via Pyodide)

---

## ⚠️ Notes (注意事項)

* Initial startup may take 30-60 seconds (loading Python runtime).
  * 初回起動には30〜60秒かかる場合があります（Pythonランタイムの読み込み）。
* Large datasets (10,000+ records) may require additional processing time.
  * 大量データ（1万件以上）は処理に時間がかかることがあります。
* Internet connection required only for initial load.
  * インターネット接続は初回読み込み時のみ必要です。

---

## 🔗 Related Projects (関連プロジェクト)

* [APOLLO](https://github.com/shibayamalicht/apollo-patent-analysis) - Full-featured patent analysis platform (Streamlit)
  * フル機能版の特許分析プラットフォーム（Streamlit）

---

## 📝 Changelog (変更履歴)

### v1.0.0 (2026-02-02)
* 🎉 Initial release
* 📊 7 analysis modules: Timeline, Applicant, IPC, Matrix, Treemap, Lifecycle
* 🔍 Click-to-detail for Applicant and Matrix charts
* 📋 Application number column support
* 🎨 Status breakdown for Timeline and Applicant charts
* 🗺️ Dynamic margin adjustment for Matrix labels

---

## 📄 License (ライセンス)

MIT License

---

© 2026 しばやま (shibayamalicht)
