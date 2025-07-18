# ファイル path

```
src/pages/flowchart/
├── FlowchartPage.tsx
├── FlowchartPage.module.css
└── index.ts
```

# ページ の情報

## フローチャート描画ページ（FlowchartPage）

- **ページの説明**:
  - プロジェクト固有のフローチャートを作成・編集するためのページ
  - メタリックデザインによる高級感のあるUI
  - React Flowライブラリを使用したインタラクティブなフローチャート編集機能

- **主要機能**:
  - **ノード追加**: 5種類（IF・FOR・WHILE・不明・通常）のカスタムノードを配置
  - **ノード操作**: ドラッグ&ドロップによる移動、Deleteキーによる削除
  - **エッジ操作**: ノード間の接続線の作成・削除
  - **保存・クリア**: フローチャートの保存とクリア機能
  - **使い方ガイド**: 初回利用時の操作説明表示
  - **ミニマップ**: フローチャート全体の表示とナビゲーション
  - **コード入力機能**: プロジェクトコードの作成・編集・管理

- **デザイン特徴**:
  - **メタリック背景**: ダークグラデーション（#0f1419 → #718096）
  - **ガラス効果**: backdrop-filter による半透明エフェクト
  - **グラデーションテキスト**: タイトルのメタリック風テキスト
  - **ホバーエフェクト**: ボタンの浮上アニメーション
  - **放射状オーバーレイ**: 背景の光彩効果

- **ルーティング**:
  - パス: `/flowchart/{projectId}`
  - パラメータ: `projectId` - 対象プロジェクトのUUID

- **状態管理**:
  - ローカル状態: 説明パネルの表示・非表示、コード入力エリアの表示・非表示
  - フローチャート状態: `useFlowchart` フックで管理
  - プロジェクトコード状態: Redux による状態管理
  - 通知: `useNotification` フックで成功・エラー通知

- **アクセシビリティ**:
  - キーボード操作対応（Deleteキーでノード削除）
  - 操作説明の提供
  - 明確なボタンラベルとツールチップ

- **パフォーマンス最適化**:
  - `useCallback` によるイベントハンドラーの最適化
  - ReactFlowProvider による描画最適化
  - レスポンシブデザイン対応

- **カスタムノード詳細**:
  - **IF文ノード**: ひし形デザイン、条件分岐用（true/false エッジ）
  - **FOR文ノード**: 六角形デザイン、ループ処理用
  - **WHILE文ノード**: 円形デザイン、繰り返し処理用
  - **不明ノード**: 角丸四角形、警告アニメーション付き
  - **通常ノード**: 四角形デザイン、一般的な処理用

- **依存関係にあるファイル**:
  - `@xyflow/react`: React Flow コアライブラリ
  - `@/features/flowchart`: フローチャート機能（カスタムノード含む）
  - `@/components/CodeInput`: プロジェクトコード入力コンポーネント
  - `@/hooks/useNotification`: 通知機能
  - `react-router-dom`: ルーティング（useParams）

# 最新の更新内容 (feature/#25 ブランチ)

- **コード入力機能の統合**:
  - `CodeInput` コンポーネントをページに統合
  - コード入力エリアの表示・非表示状態管理 (`showCodeInput`)
  - プロジェクトUUIDをCodeInputコンポーネントに渡してコード管理
  - フローチャートとコード入力機能の連携基盤を構築

- **今後の拡張予定**:
  - コードからフローチャートの自動生成機能
  - フローチャートからコードの生成機能
  - コード解析によるノードの自動配置