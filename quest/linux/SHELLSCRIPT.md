# シェルスクリプトを書くことができる

## 1. Hello

「シェルスクリプトのファイルを作成し、「Hello!」と出力してください。」
1. nano hello.sh
2. ファイルの中身を以下とする。
    #!/bin/bash
   echo "Hello!"
3. 実行権限を付与する chmod +x hello.sh
4. スクリプトを実行する ./hello.sh or bash hello.sh

なお、シェルスクリプトを実行する際にはファイルに実行権限が付与されている必要があることに気を付けてください。

## 2. 標準入力から値を受け取る

「シェルスクリプトのファイルに「What's your name?」と出力し、ユーザーに名前の入力を求めます。その後ユーザーが入力した名前に対して、「Welcome, $name!」（$name は入力された名前）と出力する処理を追加してください。」
1. hello.shを開く
2. 以下を記述する
   echo "What's your name?"
   read name
   echo "Welcome, $name!"
3. hello.shを実行する

## 3. 条件分岐

「四則演算を行う電卓を作成してください。実行すると以下の挙動になります。」

```bash
Enter two numbers:
10 # ユーザーが入力
11 # ユーザーが入力
Choose an arithmetic operation (+, -, *, /):
+ # ユーザーが入力
The result:21
```
以下コード
#!/bin/bash
echo "Enter two numbers:"
read number1
read number2
echo "Choose an arithmetic operation(+, -, *, /):"
read operation
if [ "$operation" = "+" ]; then
        result=$((number1 + number2))
elif [ "$operation" = "-" ]; then
        result=$((number1 - number2))
elif [ "$operation" = "*" ]; then
        result=$((number1 * number2))
elif [ "$operation" = "/" ]; then
        result=$((number1 / number2))
fi
echo "The result: $result"

なお、割り算の時の割る数が 0 であるケースや、演算子の記号 +, -, *, / が合致しないケースを考慮するかは任意とします。

## 4. 繰り返し処理

for 文 または while 文を利用して、1~100までのうち、偶数の数字を表示する処理を書いてください。以下の結果が出力されます。

```bash
2 4 8 ... 100
```
以下コード
#!/bin/bash
for ((i=1; i<=100; i++)); do
        if ((i % 2 == 0)); then
                echo "$i"
        fi
done
