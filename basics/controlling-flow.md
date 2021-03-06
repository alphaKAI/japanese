# 制御構造

アプリケーションにおける処理フローは `if` .. `else` 文によって条件づけて制御できます:

    if (a == 5) {
        writeln("Condition is met");
    } else if (a > 10) {
        writeln("Another condition is met");
    } else {
        writeln("Nothing is met!");
    }

`if` や `else` に続くブロックが単一の文のみからなるなら、カッコは省略できます。

変数などの等価性をテストしたり比較したりする演算子として、D言語は C/C++ や Java と同じものを提供しています:

* `==` および `!=`: 等価性および非等価性のテスト
* `<`, `<=`, `>` および `>=`: 大小関係 (等しいことを含む) のテスト

複数の条件を組み合わせるには、論理 **和** `||` および論理 **積** `&&` を用います。

D言語には **1つの** 変数の値に基づいて1つのケースを実行する `switch`..`case` 文もあります。
`switch` は **文字列も含む** すべての基本型に使うことができます。
また、`case START: .. case END:` という構文を用いて整数の範囲に基づくケースを定義することもできます。
ぜひサンプルコードを見てください。

### 掘り下げる

#### ベーシック・リファレンス

- [Logical expressions in _Programming in D_](http://ddili.org/ders/d.en/logical_expressions.html)
- [If statement in _Programming in D_](http://ddili.org/ders/d.en/if.html)
- [Ternary expressions in _Programming in D_](http://ddili.org/ders/d.en/ternary.html)
- [`switch` and `case` in _Programming in D_](http://ddili.org/ders/d.en/switch_case.html)

#### アドバンスト・リファレンス

- [Expressions in detail](https://dlang.org/spec/expression.html)
- [If Statement specification](https://dlang.org/spec/statement.html#if-statement)

## {SourceCode}

```d
import std.stdio;

void main()
{
    if (1 == 1)
        writeln("You can trust math in D");

    int c = 5;
    switch(c) {
        case 0: .. case 9:
            writeln(c, " is within 0-9");
            break; // 必要です!
        case 10:
            writeln("A Ten!");
            break;
        default: // どのケースにも当てはまらなかった場合
            writeln("Nothing");
            break;
    }
}
```
