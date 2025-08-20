# 変形GitFlow２（並列開発版）

releaseブランチを使用せず、developブランチで直接テストを完了してmainにマージするシンプルな並列開発モデルです。

```mermaid
gitGraph
    commit id: "初期コミット"
    commit id: "基本構成"
    
    branch develop-x.y.1
    branch develop-x.y.2
    
    checkout develop-x.y.1
    commit id: "v1開発準備"
    branch feature/issue-1
    checkout feature/issue-1
    commit id: "issue-1: 機能追加"
    commit id: "issue-1: テスト追加"
    commit id: "issue-1: レビュー修正"
    checkout develop-x.y.1
    merge feature/issue-1
    
    branch feature/issue-4
    checkout feature/issue-4
    commit id: "issue-4: 設定機能"
    commit id: "issue-4: バリデーション"
    checkout develop-x.y.1
    merge feature/issue-4
    commit id: "v1統合テスト"
    commit id: "v1最終確認"
    
    checkout main
    merge develop-x.y.1 tag: "v1.0"
    
    checkout develop-x.y.2
    commit id: "v2開発準備"
    branch feature/issue-2
    checkout feature/issue-2
    commit id: "issue-2: API追加"
    commit id: "issue-2: ドキュメント"
    commit id: "issue-2: 最終調整"
    checkout develop-x.y.2
    merge feature/issue-2
    
    branch feature/issue-3
    checkout feature/issue-3
    commit id: "issue-3: UI改善"
    commit id: "issue-3: レスポンシブ対応"
    checkout develop-x.y.2
    merge feature/issue-3
    commit id: "v2統合テスト"
    commit id: "v2パフォーマンス調整"
    
    checkout main
    merge develop-x.y.2 tag: "v2.0"
    
    branch hotfix/critical-bug
    checkout hotfix/critical-bug
    commit id: "緊急バグ修正"
    checkout main
    merge hotfix/critical-bug tag: "v2.0.1"
```