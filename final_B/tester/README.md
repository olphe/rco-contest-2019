# まわしてそろえる テスター

* これは
[第3回 RCO日本橋ハーフマラソン 本戦](https://atcoder.jp/contests/rco-contest-2019-final/)
の
[B 問題 - まわしてそろえる](https://atcoder.jp/contests/rco-contest-2019-final/tasks/rco_contest_2019_final_b)
のテストケースジェネレータとジャッジのためのプログラムです。これらを用いることで、ローカル環境でプログラムのテストを行うことができます。
* これらのプログラム上で計算された得点は、当コンテストでの得点を保証するものではありません。
* これらのプログラムを使用することによるあらゆる損害は保障しかねますので、予めご了承ください。
* これらのプログラムに関する質問は受け付けていません。予めご了承ください。
* これらのプログラムの一部を、コンテストの解答に流用してもかまいません。

# コンパイル
`Generator.java`, `Judge.java`, `TestCase.java` の 3 つのファイルを同じディレクトリに設置し、以下のコマンドを実行してください。

```bash
javac -encoding UTF-8 Generator.java
javac -encoding UTF-8 Judge.java
```

# テストケース生成
コンパイル後、好きな乱数シードを整数で与えることで、問題文の条件を満たすテストケースを生成できます。以下のコマンドでは `12345` という値を乱数シード値として、`input.txt` というテキストファイルにテストケースを保存しています。

```bash
java Generator -seed 12345 > input.txt
```

シード値に `1`, `2`, `3` を与えて生成したテストケースを、それぞれ `input_1.txt`, `input_2.txt`, `input_3.txt` として置いています。

# 得点計算
コンパイル後、テストケースのテキストファイルと、自分のプログラムの出力結果のテキストファイルから、テストケースに対する得点を計算することができます。以下のコマンドでは、 `input.txt` というテキストファイルに保存されたテストケースに対する `output.txt` というテキストファイル内の出力から得られる得点を計算しています。

```bash
java Judge input.txt output.txt
```
