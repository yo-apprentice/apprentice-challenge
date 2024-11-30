# パーミッションを操作できる

## 1. ファイルのオーナーとグループ

「ホームディレクトリの直下に、README.md という名前の空ファイルを作成してください。」
touch README.md

「その上で、README.md ファイルのオーナーとグループを確認してください。」
ls -l ~/README.md
-rw-r--r--  1 yosuke  staff  0 11 30 17:53 /Users/yosuke/README.mdとなる。
ファイルのオーナー：yosuke
グループ：staff

## 2. ファイルのパーミッション

「README.md ファイルのパーミッションを確認し、誰に何の権限が付与されているかを説明してください。」
オーナー：rw-　読み取り権限あり、書き込み権限あり、実行権限なし
グループ：r--　読み取り権限あり、書き込み権限なし、実行権限なし
その他：r--　　読み取り権限あり、書き込み権限なし、実行権限なし

## 3. ファイルのパーミッションの設定

「README.md ファイルのオーナーに対して、読み取り、書き込み、実行の全ての権限を付与してください。」
1. chomd u+x README.md
2. ls -l ~/README.md

## 4. ディレクトリのパーミッションの設定

「ホームディレクトリの直下に、permission という名前の空ディレクトリを作成してください。」
1. mkdir permission

「permission ディレクトリのグループに対して、書き込み権限を付与してください。」
1. 権限をチェックする　ls -ld permission
2. chomd g+w permission
3. ls -ld permission

## 5. スーパーユーザー

「スーパーユーザーとして、ホームディレクトリの直下に superuser という名前の空ディレクトリを作成してください。」
1. sudo mkdir superuser

「作成後、superuser ディレクトリのオーナーが誰かを確認してください。」
1. ls -ld superuser
2. drwxr-xr-x  2 yosuke  staff  64 11 30 18:12 superuser
   オーナー：yosuke
