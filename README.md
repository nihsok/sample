gitのインストール、GitHubアカウント作成などgitとは別の知識が要求されるところは省略
# 一番最初に（のみ）やること
1. `git cofig --global user.email "sample@example.com"`
2. `git config --global user.name "jugemujugemu"`
  - `git config --list` で確認できる

# 既存のリモートリポジトリを手元持ってきて編集する場合


# 新しくリポジトリから作る場合
0. （GiHub等で）リポジトリを作る
1. `mkdir （リポジトリ名）; cd -; git init` で.git/ができる。
  2. `git remote add origin git@github.com:（ユーザー名）/（リポジトリ名）.git` で登録
  1. ファイルの作成、編集を行う。
  2. `git add （編集したファイル）` でステージ
  3. `git commit -m "（コミットメッセージ）"` でコミット