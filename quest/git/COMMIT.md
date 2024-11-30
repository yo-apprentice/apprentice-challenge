# コミットができる

## 1. ローカルリポジトリの新規作成

任意の場所に git_practice という名前の新規ディレクトリを作成してください。作成したディレクトリに移動して、Git のローカルリポジトリを新規作成してください。
mkdir git_practice

## 2. 変更をステージに追加

作成したディレクトリの下に README.md というファイルを作成してください。次に、作成したファイルをステージに追加してください。
1. touch README.md
2. git init --initial-branch main
3. git switch -c quest-11
4. git add .
5. git status

## 3. 変更を記録

ステージに追加した変更をローカルリポジトリに記録してください。なお、変更の記録のことを「コミット」と言います。
1. git commit -m"first commit"
