
### Cat

Awodey:

> **定義 1.2.** 函手 (functor)<br>
> F: **C** => **D**<br>
> は、圏 **C** と圏 **D** の間で以下の条件が成り立つように対象を対象に、また射を射に転写する:
>
> - F(f: A => B) = F(f): F(A) => F(B)
> - F(1<sub>A</sub>) = 1<sub>F(A)</sub>
> - F(g ∘ f) = F(g) ∘ F(f)
>
> つまり、*F* はドメインとコドメイン、恒等射、および射の合成を保存する。

ついにきた。函手 (functor) は 2つの圏の間の射だ。以下が外部図式となる:

![functor](../files/day16-a-functor.png)

*F(A)*、 *F(B)*、 *F(C)* の位置が歪んでいるのは意図的なものだ。*F* は上の図を少し歪ませているけども、射の合成関係は保存している。

この圏と函手の圏は **Cat** と表記される。

ここで表記規則をおさらいしておこう。
大文字、斜体の *A*、*B*、*C* は対象を表す (**Sets** において、これらは `Int` や `String` に対応する)。
一方、大文字、太字の **C** と **D** は圏を表す。圏は、これまでに見てきた `List[A]` を含み色んな種類のものでありうる。つまり、函手 *F*: **C** => **D** はただの関数ではなく、**2つの圏の間の射**だということに注意してほしい。

そういう意味では、プログラマが「`Functor`」と言った場合は、**C** 側が **Sets** に決め打ちされた非常に限定された種類の函手を指しているといえる。

![Scala functor](../files/day16-b-scala-functor.png)
