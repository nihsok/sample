gitのインストール、GitHubアカウント作成、公開鍵登録などgitとは別の知識が要求されるところは省略
# 一番最初に（のみ）やること
1. `git cofig --global user.email "sample@example.com"`
2. `git config --global user.name "jugemujugemu"`
  - `git config --list` で確認できる

# 既存のリモートリポジトリを手元に持ってきて編集する場合
- 困ったときは`git status`
- `git clone git@github.com:（ユーザー名）/（リポジトリ名）.git; cd （リポジトリ名）`

  （間違えたときは`rm -rf （リポジトリ名）`）
  - ファイルの作成、編集

    削除するときは`rm （ファイル）`ではなく`git rm （ファイル）`

  - `git add （編集したファイル）`: ステージ（保存するたびにするくらいがいい？）
  
    `git add .`でまとめてステージ出来る。
    - `git resotre （編集したファイル）`: ステージの撤回
  - `git commit -m "コミットメッセージ"`: コミット（コミットメッセージはつけるようにする）

    下の方のディレクトリでコミットしても効かない？（上でやり直すことになる）

    - `git commit --amend -m "コミットメッセージ"`: コミットメッセージの上書き
  - `git push`: プッシュ（手元の変更をリモートへ反映）
  - `git pull`: プル（リモートの変更を手元へ反映）
  
    ここで編集の衝突があって、ややこしいことになる。

# 新しくリポジトリから作る場合
- （GiHub等で）リポジトリを作る
- `mkdir （リポジトリ名）; cd -; git init` : .git/ができる。
  - `git remote add origin git@github.com:（ユーザー名）/（リポジトリ名）.git` : 登録
  - ファイルの作成、編集
  - `git add （編集したファイル）`: ステージ
  - `git commit -m "（コミットメッセージ）"`: コミット