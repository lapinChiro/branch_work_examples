# ブランチワーク図解集

このドキュメントは、様々なGitブランチ戦略をMermaid形式で図解したものです。

## 目次

### 基本的なブランチ戦略

1. **[GitFlow](diagrams/gitflow.md)**
   - Vincent Driessenによって提案された標準的なブランチモデル
   - main、develop、feature、release、hotfixの5種類のブランチを使用

2. **[GitHubFlow](diagrams/github-flow.md)**
   - GitHubで採用されているシンプルなブランチモデル
   - mainブランチと機能ブランチのみを使用

3. **[GitLabFlow](diagrams/gitlab-flow.md)**
   - GitLabで採用されている環境ベースのブランチモデル
   - production、stagingなどの環境ブランチを使用

### 並列開発に特化したブランチ戦略

4. **[変形GitFlow（並列開発版）](diagrams/parallel-gitflow.md)**
   - 複数のdevelopブランチとreleaseブランチを使用
   - 完全な並列開発を実現

5. **[変形GitFlow２（並列開発版）](diagrams/parallel-gitflow-v2.md)**
   - releaseブランチを省略したシンプルな並列開発モデル
   - developブランチから直接mainにマージ

## 関連ドキュメント

- [ブランチワークの要件](requirement.md)

## 使い方

各リンクをクリックして、それぞれのブランチ戦略の詳細なMermaid図を確認してください。