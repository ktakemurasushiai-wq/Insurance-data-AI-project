# Insurance Data AI Project - KPI Analysis & Automation

## 1. プロジェクト概要
本プロジェクトは、保険業界における「顧客満足度（推奨度）の可視化」および「支払いプロセスの自動化」をテーマとしたDX推進シミュレーションプロジェクトです。
自身の職務経験に基づき、単なるデータ集計に留まらず、ビジネスの意思決定（営業戦略の立案）に直結する一気通貫のデータパイプラインを構築しています。

### 解決する課題とビジネスインパクト
* **市場ポジションの把握**: 自社（A社）と競合他社のNPSを比較し、客観的な立ち位置を可視化。
* **戦略的セグメンテーション**: 販売チャネルや年代別の傾向を特定し、リソース投入の最適化を支援。
* **LTV（顧客生涯価値）の向上**: NPS分析に基づき、解約率の低減やロイヤリティ向上に繋がる施策立案の根拠を提供。
* **オペレーションの効率化**: AIを活用した支払い判定の自動化による、業務コスト削減のシミュレーション（順次実装予定）。

# Insurance Data AI Project - KPI Analysis & Automation

## 1. プロジェクト概要
本プロジェクトは、保険業界における「顧客満足度（推奨度）の可視化」および「支払いプロセスの自動化」をテーマとしたDX推進シミュレーションプロジェクトです。
自身の職務経験に基づき、単なるデータ集計に留まらず、ビジネスの意思決定（営業戦略の立案）に直結する一気通貫のデータパイプラインを構築しています。

### 解決する課題とビジネスインパクト
* **市場ポジションの把握**: 自社（A社）と競合他社のNPSを比較し、客観的な立ち位置を可視化。
* **戦略的セグメンテーション**: 販売チャネルや年代別の傾向を特定し、リソース投入の最適化を支援。
* **LTV（顧客生涯価値）の向上**: NPS分析に基づき、解約率の低減やロイヤリティ向上に繋がる施策立案の根拠を提供。

## 2. システム構成（アーキテクチャ）

![Dashboard Screenshot](r("reports\summary_report.png"))

```mermaid
graph LR
    subgraph "Data Generation Layer"
    A[Python: Dummy Data Gen] --> B[Pandas: Preprocessing]
    end
    ...
 ```

## 3. 実装済み/実装予定のKPI（推奨度分析）

### 指標定義
* **推奨度（NPS）**: $(推奨者数 - 批判者数) / 全体回答者数$
* **推奨者**: スコア 9-10
* **中立者**: スコア 7-8
* **批判者**: スコア 0-6

### 分析軸
* **契約会社比較**: 自社（A社）vs 競合他社（B社、C社等）
* **セグメント分析**: 年代（10歳刻み）、販売チャネル（営業・ネット）、契約年数

## 4. 技術スタック
* **Language**: Python 3.10+
* **Library**: Pandas (データ前処理), NumPy (数値計算)
* **BI Tool**: Power BI Desktop
* **Environment**: VS Code (venv)

## 5. ディレクトリ構成
```text
.
├── data/               # CSVデータ（生データ・集計済みデータ）
├── notebooks/          # Pythonスクリプト(Jupyter Notebook)
│   ├── 01_dummy_data_generation.ipynb   # 1. データ生成
│   └── 02_nps_analysis.ipynb            # 2. KPI集計・前処理
├── reports/            # Power BI関連ファイル(.pbix)
└── README.md
```
## 6. 開発ロードマップ
- [x] プロジェクト設計・環境構築
- [x] README.md によるドキュメント整備
- [x] ダミーデータ生成スクリプトの開発 (`01_dummy_data_generation.ipynb`)
- [x] PythonによるNPS算出ロジックの実装 (`02_nps_analysis.ipynb`)
- [x] Power BIダッシュボードの構築


## 7. 使用方法
1. `notebooks/01_dummy_data_generation.ipynb` を実行し、`data/` 内に生データを生成します。
2. `notebooks/02_nps_analysis.ipynb` を実行し、分析用集計データ（KPI）を生成します。
3. `reports/` 内のPower BIファイル（作成予定）を開き、可視化されたレポートを確認します。