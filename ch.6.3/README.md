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