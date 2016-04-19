# 目次

## Part 1. イントロダクション
### 1. イントロダクション
- システム管理者（SysAdmin）のアプローチからサービスマネジメントへ
- Googleのサービスマネジメントへのアプローチ＝Site Reliability Engineering
- SREの教義
- はじめの終わりに

### 2. SRE視点から見るGoogleの本番環境
- ハードウェア
- ハードウェアを統括するシステム・ソフトウェア
- その他のシステム・ソフトウェア
- われわれのソフトウェア基盤
- われわれの開発環境
- サンプルサービス：シェイクスピア

## Part 2. 原則編
### 3. リスクを抱きしめる
- リスク管理
- サービスリスクの計測
- サービスのリスク耐性
- エラーバジェットの動機

### 4. サービスレベル目標
- サービスレベル用語
- 実践指標
- 実践目標
- 実践規約

### 5. 苦役を排除する
- 苦役の定義
- なぜ苦役が少ないほうがよいのか
- エンジニアリングとしての資格はなにか？
- 苦役はつねに悪か？
- 結論

### 6. 分散システムの監視
- 定義
- なぜ監視するのか？
- モニタリングのための合理的な期待値の設定
- 症状 vs 原因
- ブラックボックス vs ホワイトボックス
- 4つのゴールデンシグナル
- Tailの心配（あるいは機材の利用やパフォーマンス）
- 測定の適切な解像度の選択
- よりシンプルにではなく、できるだけシンプルに
- これらの原則をすべて結びつける
- 長期間の監視
- 結論

### 7. Googleの自動化の進化

- 自動化の価値
- GoogleのSREのための価値
- 自動化の事例
- 自分の仕事をなくすために自動化せよ：すべてのものを自動化せよ！
- 痛む場所をなだめる：クラスタ起動部に自動化を適用する
- Borg：倉庫規模のコンピュータの誕生
- 信頼性は基本機能
- おすすめ

### 8. リリースエンジニアリング

- リリースエンジニアの役割
- 哲学
- 継続的ビルドとデプロイ
- 設定管理
- 結論

### 9. シンプルさ

- システムの安定性 vs アジリティ
- 退屈の美徳
- 私は自分のコードをあきらめない！
- 「コードの負の行」メトリック
- 最小限のAPI
- モジュラリティ
- シンプルさをリリースする
- シンプルな結論

## Part 3. 実践編

### 10. 時系列データから取得する実用的なアラート

- Borgmonの台頭
- アプリケーションの計装
- エクスポートされたデータの収集
- 時系列アリーナのにおけるストレージ
- ルール評価
- アラート
- 監視トポロジーをシャーディングする
- ブラックボックス監視
- 設定の保守
- 10年間

### 11. オンコールに生きる

- はじめに
- オンコールエンジニアの生活
- 均衡化されたオンコール
- 心理的安全
- 不適切な運用負荷の回避
- 結論

### 12. 効果的なトラブルシューティング

- 理論
- 実践
- 負の結果は魔法である
- ケーススタディ
- トラブルシューティングを簡単にする
- 結論

### 13.緊急対応

- システムが壊れるときに何が起きているか
- テストが誘発する警報
- 変更が誘発する警報
- プロセスが誘発する警報
- すべての問題には解決策がある
- 過去から学ぶ。繰り返さない。
- 結論

### 14. インシデントの管理

- 管理対象外のインシデント
- 管理対象外のインシデントの解剖学
- インシデント管理プロセスの要素
- 管理されたインシデント
- インシデントを宣言するとき
- まとめ

### 15. ふりかえり(死体解剖)文化：失敗から学ぶ

- Googleのふりかえり哲学
- コラボレーションと知識の共有
- ふりかえり文化の紹介
- 結論と継続的改善

### 16. 追跡の停止

- エスカレーター
- Outalator

### 17. 信頼性のためのテスト

- ソフトウェアテストの種類
- テスト作成と環境構築
- 大規模テスト
- 結論

### 18. SREのソフトウェアエンジニアリング

- なぜSREにソフトウェアエンジニアリングが重要なのか？
- Auxon事例：プロジェクトの背景と問題領域
- 意図基準のキャパシティプランニング
- SREにおけるソフトウェアエンジニアリングの育成
- 結論

### 19. フロントエンドでおこなう負荷分散

- 電源は答えではない
- DNSを使用した負荷分散
- 仮想IPアドレスを使用した負荷分散

### 20. データセンターでおこなう負荷分散

- 理想的なケース
- 悪い作業の識別：フロー制御とレームダック
- コネクションプールをサブセット化して制限する
- ロード・バランシング・ポリシー

### 21. 過負荷のあつかいかた

- 「秒間クエリ数」の罠
- カスタマー単位の制限
- クライアントサイドのスロットリング
- 重要度
- 有益なシグナル
- 過負荷エラーのあつかいかた
- コネクションの負荷
- 結論

### 22. カスケード障害への対処

- カスケード障害の原因と回避するための設計
- サーバの過負荷を抑止する
- 低速起動とコールドキャッシング
- カスケード障害のためのトリガ条件
- カスケード障害のためのテスト
- カスケード障害に対処するために今すぐやるべきこと
- 所感

### 23. 緊急度の管理：信頼性のための分散合意手法

- 分散システムの協調障害：分散合意手法の採用を検討する
- 分散合意の仕組み
- 分散合意のためのシステムアーキテクチャパターン
- 分散合意のパフォーマンス
- 分散合意ベースのシステムのデプロイ方法
- 分散合意システムの監視
- 結論

### 24. Cronをつかった分散定期スケジューリング

- Cron
- Cronジョブと冪等性
- Cronの大規模利用
- GoogleにおけるCron構築
- 概要

### 25. データ処理パイプライン

- パイプラインデザインパターンの起源
- シンプルなパイプラインパターン上のビッグデータへの初期の効果
- 定期的なパイプラインパターンにおける挑戦
- 作業量配分のむらによる不具合
- 分散環境での定期的なパイプラインの欠点
- Google Workflowの概要
- Google Workflowでの実行のステージ
- ビジネス継続性の確保
- まとめと所感

### 26. データ整合性：書いたものを読む

- データ整合性の厳格な要件
- データ整合性と可用性の維持におけるGoogle SREの目標
- どのようにGoogle SREはデータ整合性に対する挑戦と向き合っているか
- ケーススタディ(事例)
- データ整合性におけるSREの一般原則
- 結論

### 27. 大規模環境での信頼性高い起動方法

- コー​​ディネーションエンジニアリングの起動
- 起動プロセスの設定
- 起動チェックリストの作成
- 信頼性高い起動のために選択されたテクニック
- LCEの開発
- 結論

## Part 4. マネジメント編

### 28. SREをオンコールやその先に加速する

- 次のSREを雇ったあなた、それで次は？
- 最初に学習する経験：カオスを超えた構造のケース
- 傑出したリバースエンジニアと即興で考えられるものの育成
- 意欲的なオンコール要員のための5つのプラクティス
- オンコールとその先：通過儀礼および継続教育の実践
- 所感

### 29. 割り込みへの対処

- 運用負荷を管理する
- 割り込みの処理方法の決定要素
- 不完全なマシン

### 30. 運用過負荷から回復するSREを埋め込み

- 第1段階：サービスを学び、コンテキストを理解する
- 第2段階：コンテキストを共有する
- 第3段階：Driving Change (チームの変化を導く)
- 結論

### 31. SREにおけるコミュニケーションとコラボレーション

- コミュニケーション：プロダクションミーティング
- SRE内でのコラボレーション
- SREのコラボレーション事例：Viceroy
- SRE外とのコラボレーション
- ケーススタディ：DFPからF1への移行
- 結論

### 32.進化するSREエンゲージメントモデル

- SREエンゲージメント(約束)：「何を」「どのように」そして「なぜ」
- PRRモデル
- SREエンゲージメントモデル
- 本番準備レビュー：シンプルなPRRモデル
- 進化するシンプルなPRRモデル：早期の約束
- 進化するサービス開発：フレームワークとSREプラットフォーム
- 結論

## Part 5. まとめ

### 33. 他の業界から学ぶ教訓

- 他の業界のベテランとの出会い
- 準備と災害対策テスト
- ふりかえり文化
- 反復作業や運用のオーバーヘッドを避けるための自動化
- 構造化され、合理的な意思決定
- 結論

### 34. まとめ


```
Part I. Introduction

1. Introduction

The Sysadmin Approach to Service Management
Google’s Approach to Service Management: Site Reliability Engineering
Tenets of SRE
The End of the Beginning

2. The Production Environment at Google, from the Viewpoint of an SRE

Hardware
System Software That “Organizes” the Hardware
Other System Software
Our Software Infrastructure
Our Development Environment
Shakespeare: A Sample Service

Part II. Principles

3. Embracing Risk
Managing Risk
Measuring Service Risk
Risk Tolerance of Services
Motivation for Error Budgets

4. Service Level Objectives

Service Level Terminology
Indicators in Practice
Objectives in Practice
Agreements in Practice

5. Eliminating Toil

Toil Defined
Why Less Toil Is Better
What Qualifies as Engineering?
Is Toil Always Bad?
Conclusion

6. Monitoring Distributed Systems

Definitions
Why Monitor?
Setting Reasonable Expectations for Monitoring
Symptoms Versus Causes
Black-Box Versus White-Box
The Four Golden Signals
Worrying About Your Tail (or, Instrumentation and Performance)
Choosing an Appropriate Resolution for Measurements
As Simple as Possible, No Simpler
Tying These Principles Together
Monitoring for the Long Term
Conclusion

7. The Evolution of Automation at Google

The Value of Automation
The Value for Google SRE
The Use Cases for Automation
Automate Yourself Out oJob: Automate ALL the Things!
Soothing the Pain: Applying Automation to Cluster Turnups
Borg: Birth of the Warehouse-Scale Computer
Reliability Is the Fundamental Feature
Recommendations

8. Release Engineering

The Role oRelease Engineer
Philosophy
Continuous Build and Deployment
Configuration Management
Conclusions

9. Simplicity

System Stability Versus Agility
The Virtue of Boring
I Won’t Give Up My Code!
The “Negative Lines of Code” Metric Minimal APIs
Modularity
Release Simplicity
A Simple Conclusion

Part III. Practices

10. Practical Alerting from Time-Series Data. 

The Rise of Borgmon
Instrumentation of Applications
Collection of Exported Data
Storage in the Time-Series Arena Rule Evaluation
Alerting
Sharding the Monitoring Topology Black-Box Monitoring Maintaining the Configuration Ten Years On...

11. Being On-Call

Introduction
Life of an On-Call Engineer
Balanced On-Call
Feeling Safe
Avoiding Inappropriate Operational Load
Conclusions

12. ective Troubleshooting

Theory
In Practice
Negative Results Are Magic
Case Study
Making Troubleshooting Easier
Conclusion

13. Emergency Response

What to Do When Systems Break
Test-Induced Emergency
Change-Induced Emergency
Process-Induced Emergency
All Problems Have Solutions
Learn from the Past. Don’t Repeat It.
Conclusion

14. Managing Incidents

Unmanaged Incidents
The Anatomy of an Unmanaged Incident
Elements of Incident Management Process
A Managed Incident
When to Declare an Incident
In Summary

15. Postmortem Culture: Learning from Failure

Google’s Postmortem Philosophy
Collaborate and Share Knowledge
IntroducinPostmortem Culture
Conclusion and Ongoing Improvements

16. Tracking Outages

Escalator
Outalator

17. Testing for Reliability

Types of Software Testing
CreatinTest and Build Environment
Testing at Scale
Conclusion

18. Software Engineering in SRE

Why Is Software Engineering Within SRE Important?
Auxon Case Study: Project Background and Problem Space
Intent-Based Capacity Planning
Fostering Software Engineering in SRE
Conclusions

19. Load Balancing at the Frontend

Power Isn’t the Answer
Load Balancing Using DNS
Load Balancing at the Virtual IP Address

20. Load Balancing in the Datacenter

The Ideal Case
Identifying Bad Tasks: Flow Control and Lame Ducks
Limiting the Connections Pool with Subsetting
Load Balancing Policies

21. Handling Overload

The Pitfalls of “Queries per Second”
Per-Customer Limits
Client-Side Throttling
Criticality
Utilization Signals
Handling Overload Errors
Load from Connections
Conclusions

22. Addressing Cascading Failures.

Causes of Cascading Failures and Designing to Avoid Them
Preventing Server Overload
Slow Startup and Cold Caching
Triggering Conditions for Cascading Failures
Testing for Cascading Failures
Immediate Steps to Address Cascading Failures
Closing Remarks

23. Managing Critical State: Distributed Consensus for Reliability

Motivating the Use of Consensus: Distributed Systems Coordination Failure
How Distributed Consensus Works
System Architecture Patterns for Distributed Consensus
Distributed Consensus Performance
Deploying Distributed Consensus-Based Systems
Monitoring Distributed Consensus Systems
Conclusion

24. Distributed Periodic Scheduling with Cron

Cron
Cron Jobs and Idempotency
Cron at Large Scale
Building Cron at Google
Summary

25. Data Processing Pipelines

Origin of the Pipeline Design Pattern
Initial Effect of Big Data on the Simple Pipeline Pattern
Challenges with the Periodic Pipeline Pattern
Trouble Caused By Uneven Work Distribution
Drawbacks of Periodic Pipelines in Distributed Environments
Introduction to Google Workflow
Stages of Execution in Workflow
Ensuring Business Continuity
Summary and Concluding Remarks

26. Data Integrity: What You Read Is What You Wrote

Data Integrity’s Strict Requirements
Google SRE Objectives in Maintaining Data Integrity and Availability
How Google SRE Faces the Challenges of Data Integrity
Case Studies
General Principles of SRE as Applied to Data Integrity
Conclusion

27. Reliable Product Launches at Scale

Launch Coordination Engineering
Setting ULaunch Process
DevelopinLaunch Checklist
Selected Techniques for Reliable Launches
Development of LCE
Conclusion

Part IV. Management

28. Accelerating SREs to On-Call and Beyond

You’ve Hired Your Next SRE(s), Now What?
Initial Learning Experiences: The Case for Structure Over Chaos
Creating Stellar Reverse Engineers and Improvisational Thinkers
Five Practices for Aspiring On-Callers
On-Call and Beyond: Rites of Passage, and Practicing Continuing Education
Closing Thoughts

29. Dealing with Interrupts

Managing Operational Load
Factors in Determining How Interrupts Are Handled
Imperfect Machines

30. Embedding an SRE to Recover from Operational Overload

Phase: Learn the Service and Get Context
Phase: Sharing Context
Phase: Driving Change
Conclusion

31. Communication and Collaboration in SRE

Communications: Production Meetings
Collaboration within SRE
Case Study of Collaboration in SRE: Viceroy
Collaboration Outside SRE
Case Study: Migrating DFP to F1
Conclusion

32. The Evolving SRE Engagement Model

SRE Engagement: What, How, and Why
The PRR Model
The SRE Engagement Model
Production Readiness Reviews: Simple PRR Model
Evolving the Simple PRR Model: Early Engagement
Evolving Services Development: Frameworks and SRE Platform
Conclusion

Part V. Conclusions

33. Lessons Learned from Other Industries

Meet Our Industry Veterans
Preparedness and Disaster Testing
Postmortem Culture
Automating Away Repetitive Work and Operational Overhead
Structured and Rational Decision Making
Conclusions

34. Conclusion
```
