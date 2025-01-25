# 複数行のパターンスペース
## 削除コマンド D
### 複数行の空行を1行にする
#### 失敗例  小文字のdコマンドを使用。空行が偶数の場合に空行が全部削除されてしまう
```
# reduce multiple blank lines to one; version using d command
/^$/{
    N
    /^\n$/d
}
```
```
$ sed -f sed.blank-fail test.blank
This line is followed by 1 blank line.

This line is followed by 2 blank line.
This line is followed by 3 blank line.

This line is followed by 4 blank line.
This is the end.
$
```
#### 成功　大文字のDコマンドを使用。
```
# reduce multiple blank lines to one
/^$/{
    N
    /^\n$/D
}
```
```
$ sed -f sed.blank test.blank
This line is followed by 1 blank line.

This line is followed by 2 blank line.

This line is followed by 3 blank line.

This line is followed by 4 blank line.

This is the end.
$
```
## 表示コマンド P