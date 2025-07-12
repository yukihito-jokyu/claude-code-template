---
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git commit:*)
description: gitのコミット作成タスク
---

## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10`

## Rule

- コミットメッセージは日本語で作成してください。
- コミットメッセージのテンプレートは @.commit-template を参照してください。
- コミットメッセージの最後に`#Issue番号`を記載してください。
- `#Issue番号`が分からない場合は記載しなくてよいです。
- pre-commit でエラーが出た場合再度同じファイルをステージングし、コミットしなおしてください。

## Your task

1. 作業内容が近しいファイルをステージングする
2. コミットを作成する。
3. 1 と 2 を作業ファイルが無くなるまで繰り返す。
