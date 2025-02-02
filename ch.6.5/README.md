# フレーズの結合
### phraseシェルスクリプト
### 複数の単語の並びを、2行にまたがっていても見つけられるようにするgrep風のプログラム
#### サンプルファイルsect3 Windows 11 の2025.2.2時点のCopilotに作ってもらった
```
make sample text include "the procedure is followed" just 20 lines.

Here's a sample text for you:

In our lab, we take great care to ensure that the procedure is followed meticulously. This begins with the initial assessment where the team gathers all necessary materials. Once the initial setup is complete, the safety protocols are reviewed to guarantee compliance. Next, the primary steps of the procedure are laid out and assigned to the responsible team members.

During the implementation phase, each step is checked off to ensure the procedure is followed accurately. Any deviations are immediately addressed, and the necessary corrections are made. This systematic approach helps us maintain high standards.

The final stages involve a thorough review and documentation. We verify that the procedure is followed from start to finish, leaving no room for error. This comprehensive approach not only ensures consistency but also enhances our overall efficiency.

Regular audits are conducted to ensure that the procedure is followed in all future projects. Feedback from these audits is used to refine and improve our processes, ensuring that our work remains at the cutting edge of our field.

I hope this helps! Let me know if you need any more assistance.
```
これに適当に改行を入れたものがこのフォルダーのsect3である。
### phrase 実行例
```
$ ./phrase "the procedure is followed" sect3
In our lab, we take great care to ensure that the procedure is followed meticulously. This
During the implementation phase, each step is checked off to ensure the procedure is
followed accurately. Any deviations are immediately addressed, and the necessary
The final stages involve a thorough review and documentation. We verify that the
procedure is followed from start to finish, leaving no room for error. This comprehensive
Regular audits are conducted to ensure that the procedure is followed in all future
ensuring that our work remains at the cutting edge of our field.
$
```
マッチしていないのに最終行が出力されてしまっている。
