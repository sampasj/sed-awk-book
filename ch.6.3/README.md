# 行の保管
```
$ sed -f sed.flip test.flip
2
1
22
11
222
111
$
```
# 大小文字の変換
### ステートメント名を大文字に変換
#### ホールドスペースをうまく使えば、入力行の一部を分離して処理出来るようになるのだ
```
$ cat sample1
find the Match statement
Consult the Get statement.
using the Read statement to retrieve data
$ sed -f sed.cap sample1
find the MATCH statement
Consult the GET statement.
using the READ statement to retrieve data
$
```
# テキストブロック
#### ホールドスペースは、行をブロックにして出力したい場合にも使える
#### プレーンテキストファイルに段落タグを入れる
```
$ sed -f sed.para sample2
<p>My wife won't let me buy a power saw. She is afraid of an
accident if I use one.
So I rely on a hand saw for a variety of weekend projects like
building shelves.
However, if I made my living as a carpenter, I would
have to use a power
saw. The speed and efficiency provided by power tools
would be essential to being productive.</p>

<p>For people who create and modify text files,
sed and awk are power tools for editing.</p>

<p>Most of the things that you can do with these programs
can be done interactively with a text editor. However,
using these programs can save many hours of repetitive
work in achieving the same result.</p>
$
```