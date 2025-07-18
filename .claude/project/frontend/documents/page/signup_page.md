# ファイル path

```
src/pages/signup/
├── SignupPage.tsx
├── SignupPage.module.css
└── index.ts
```

# ページの情報

## SignupPage (新規登録ページ)

- 新規登録フォームを表示するページコンポーネント
- メタリックなグラデーション背景とグラスモーフィズムデザイン
- レスポンシブ対応の全画面レイアウト
- ログインページへのモダンなナビゲーション機能

- 依存関係にあるファイル
  - features/auth/SignupForm コンポーネント
  - react-router-dom (useNavigate) - ページナビゲーション
  - SignupPage.module.css (CSS モジュール)
- ページの特徴
  - **デザイン**: グラデーション背景（紫〜ピンク）
  - **レイアウト**: 中央配置のカードデザイン
  - **エフェクト**: ぼかし効果とシャドウによる立体感
  - **アクセス**: /signup パスでアクセス可能

## ナビゲーション機能

- **モダンなボタンデザイン**: ネオモーフィズムスタイルのナビゲーションボタン
- **自動リダイレクト**: 新規登録完了後はログインページへ自動遷移
- **視覚的フィードバック**: ホバー・アクティブ状態のアニメーション
- **ユーザビリティ**: 直感的なページ間遷移
