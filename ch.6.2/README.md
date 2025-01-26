# ケーススタディ
#### 失敗 @f1( からその行の最後の閉じかっこまでのすべての文字にマッチしてしまう
```
$ sed 's/@f1(\(.*\))/\\fB\1\\fR/g' test
I want to see \fBwhat will happen\fR if we put the
font change commands \fBon a set of lines\fR. If I understand
things (correctly), the \fBthird) line causes problems. (No?\fR.
Is this really the case, or is it (maybe) just something else?

Let's test having two on a line \fBhere) and @f1(there\fR as
well as one that begins on one line and ends @f1(somewhere
on another line). What if \fBis here\fR on the line?
$
```
#### 失敗 2行にまたがっている部分だけは失敗している
```
 sed 's/@f1(\([^)]*\))/\\fB\1\\fR/g' test
I want to see \fBwhat will happen\fR if we put the
font change commands \fBon a set of lines\fR. If I understand
things (correctly), the \fBthird\fR line causes problems. (No?).
Is this really the case, or is it (maybe) just something else?

Let's test having two on a line \fBhere\fR and \fBthere\fR as
well as one that begins on one line and ends @f1(somewhere
on another line). What if \fBis here\fR on the line?
$
```