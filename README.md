📝 Git 練習手順まとめ
1. リポジトリを作成
mkdir git-practice
cd git-practice
git init

2. ファイルを作成して初回コミット
echo "Hello Git!" > hello.txt
git add hello.txt
git commit -m "初めてのコミット"

3. ファイルを編集してコミット
echo "これは2回目の編集です" >> hello.txt
git add hello.txt
git commit -m "2回目の編集を追加"

4. ブランチを作って作業
git checkout -b feature/new-task
echo "featureブランチからの編集です" >> hello.txt
git add hello.txt
git commit -m "featureブランチからの編集"

echo "Pull Request を作るための追記です" >> hello.txt
git add hello.txt
git commit -m "PR用の追記"

5. 履歴を確認
git log --oneline --graph --decorate --all

6. GitHub と接続

👉 GitHub で新規リポジトリを作成し、URL を登録する

git remote add origin https://github.com/<ユーザー名>/git-practice.git

7. main ブランチを GitHub に反映
git checkout main
git push -u origin main

8. feature ブランチを GitHub に反映
git checkout feature/new-task
git push -u origin feature/new-task

9. GitHub 上で Pull Request を作成

👉 feature/new-task → main に PR を作成する

10. GitHub 上の変更をローカルに取り込む（Pull）
git checkout main
git pull origin main
