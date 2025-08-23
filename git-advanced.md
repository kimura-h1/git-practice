🧠 Git 練習手順【応用編】の内容案


## 1. .gitignore を使った管理対象外ファイルの設定

```bash
echo "node_modules/" > .gitignore
echo ".env" >> .gitignore
git add .gitignore
git commit -m ".gitignore を追加"
```


## 2. コミットの取り消し

直前のコミットメッセージを修正

```bash
git commit --amend -m "修正後のコミットメッセージ"
```

ステージングを解除
```bash
git reset HEAD <ファイル名>
```

コミットそのものを取り消す（履歴を残さない）

```bash
git reset --hard HEAD^
```

## 3. マージとコンフリクト解消

```bash
git checkout main
git merge feature/new-task
```

コンフリクト発生時：

```bash
# 手動でファイル修正後
git add <ファイル名>
git commit -m "コンフリクト解消"
```

## 4. Rebase を使った履歴の整理

```bash
git checkout feature/new-task
git rebase main
```

## 5. Tag を使ったバージョン管理

```bash
git tag -a v1.0 -m "初回リリース"
git push origin v1.0
```

## 6. stash で一時保存

```bash
git stash
# 復元
git stash pop
```

## 7. log・diff を使った詳細な履歴確認

```bash
git log --stat
git diff HEAD~1
```

