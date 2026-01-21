# Insurance Data AI Project - KPI Analysis & Automation

## 1. プロジェクト概要
本プロジェクトは、保険業界における「顧客満足度（推奨度）の可視化」および「支払いプロセスの自動化」をテーマとしたDX推進シミュレーションプロジェクトです。
自身の職務経験に基づき、単なるデータ集計に留まらず、ビジネスの意思決定（営業戦略の立案）に直結する一気通貫のデータパイプラインを構築しています。

### 解決する課題とビジネスインパクト
* **市場ポジションの把握**: 自社（A社）と競合他社のNPSを比較し、客観的な立ち位置を可視化。
* **戦略的セグメンテーション**: 販売チャネルや年代別の傾向を特定し、リソース投入の最適化を支援。
* **LTV（顧客生涯価値）の向上**: NPS分析に基づき、解約率の低減やロイヤリティ向上に繋がる施策立案の根拠を提供。
* **オペレーションの効率化**: AIを活用した支払い判定の自動化による、業務コスト削減のシミュレーション（順次実装予定）。

## 2. システム構成（アーキテクチャ）


```mermaid
graph LR
    subgraph "Data Generation Layer"
    A[Python: Dummy Data Gen] --> B[Pandas: Preprocessing]
    end

    subgraph "Storage Layer"
    B --> C[(Processed CSV/DB)]
    end

    subgraph "Visualization & Insight Layer"
    C --> D[Power BI: DAX / Modeling]
    D --> E{Business Dashboard}
    E --> F[Strategy Planning]
    end
    3. 実装済み/実装予定のKPI（推奨度分析）指標定義推奨度（NPS）: (推奨者数 - 批判者数) / 全体回答者数推奨者: スコア 9-10中立者: スコア 7-8批判者: スコア 0-6分析軸契約会社比較: 自社（A社）vs 競合他社（B社、C社等）セグメント分析: 性別、年代（10歳刻み）、販売チャネル（営業・ネット）4. 技術スタックLanguage: Python 3.10+Library: Pandas (データ前処理), NumPy (数値計算)BI Tool: Power BI DesktopEnvironment: VS Code (venv)5. データ構造カラム名説明備考customer_id顧客一意識別子company契約会社自社(A社), B社, C社channel販売チャネル営業, ネットage_group年代10代〜80代（10歳刻み）nps_score推奨度スコア0-10の整数nps_segmentNPS区分推奨, 中立, 批判（Pythonにて算出）6. 開発ロードマップ[x] プロジェクト設計・環境構築[x] README.md によるドキュメント整備[ ] ダミーデータ生成スクリプトの開発 (01_dummy_data_generation.ipynb)[ ] PythonによるNPS算出ロジックの実装[ ] Power BIダッシュボードの構築[ ] 支払いプロセス自動化（AI抽出）機能の追加7. 使用方法（環境構築手順を追記予定）
---

### 次のステップへの提案
これで「設計」と「見せ方（README）」が完璧に整いました！

次はロードマップの第2段階、**`01_dummy_data_generation.ipynb`** の作成です。
このデータ構造に基づいたダミーデータを生成するPythonコードを作成しましょうか？（各会社やチャネルご