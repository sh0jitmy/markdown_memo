## 最近未経験新人の育成を始めて感じたこと

できることとできないことがはっきりと分かれていることに気が付いた。

できること

- 既存のソースコードをコピペしてきて、ちょっと書き換えればできる処理のとき。

できないこと

- コピペできる既存のソースコードがない処理のとき

## 未経験新人が苦手な部分はどこか？

つまり、言われた仕様通りのコードが書けない。
特に、未経験でオンラインとかスクールとかの「とりあえずプログラミング研修やりました」の新人には多い。
研修を受けているのだから、変数代入など、プログラムの書き方の部分で困る人はいない。
では、その新人はどこで困っているのか？

---

経験豊富なエンジニアは、プログラミングをするうえでどのように考えているのか。
まず、ユーザーの要件がプログラムになるまでにはいくつか過程がある。

1. 要件を整理する
2. 要件にあった機能を考える
3. 機能にあった処理フローを考える
4. 処理フローにあったプログラムコードを考える

つまり、要件定義→外部設計→内部設計→開発と同じである。

このような話をすると、ウォーターフォールなんか古いとか言いだす人がいるかもしれないが、アジャイルだって、スクラムだって、どのような開発方法であっても、この部分がなくなっているわけではない。
それぞれをガチガチのドキュメントにすることはなくなっただけで、各個人の頭の中では同じことが行われている。

では、経験豊富なエンジニアと、新人エンジニアの違いの大きな差は、なにか？
コードの書き方をある程度分かっているのだとすれば、「機能にあった処理フローを考える」の部分になることになる。

新人の多くは、プログラミング＝ソースコードを書く考えており、それ以外のことをおろそかにしやすい傾向にある。
それに対して、経験豊富なエンジニアは、頭の中で完結させてしまうので、新人エンジニアの手本となりにくい。

---

ここから本題である、経験豊富なエンジニアが、この「機能にあった処理フローを考える」方法は何かをまとめる。

基本的には大きな処理を段階を踏んで細かくしているだけである。具体的には、

1. 入力と出力をはっきり定義する
2. 機能を分岐のない3~4個程度の大きなフローに分解する
3. 分解したフローの入力と出力を定義する
4. 大きな処理フローを分岐のある小さい処理フローに分ける

となる。ほとんどやっていることは1番と3番・2番と4番で同じである。
巨大な機能の場合さらに3番4番のフローを何回も行い細かくしていくことになる。

---

まずは、「入力と出力をはっきり定義する」ところである。
要求されている機能の入力と出力をはっきりさせないとその先の処理は書きようがない。

例として、「スーパーのPOSレジ」で考えてみる。
客がレジで買い物をするには以下の動作が必要である。

1. 店員がバーコード（複数）を読み取る
2. 客が代金を払う
3. 店員がお釣りを払う

で、POSレジが担当するのは、合計金額を計算して、お釣りを計算するところである。

では、この部分の入力は何か？出力は何になるか？
入力になるのは、「バーコード（複数）」と「代金」である。
出力になるのは「お釣り」である。

---

次に、「機能を分岐のない3~4個程度の大きなフローに分解する」ところである。
できるだけ直列のわかりやすい単位で分解するのがおすすめである。

例の場合は

1. バーコードの読み取りを行い単品額を求めるの繰り返し
2. 合計額を計算する
3. 投入された代金をよみとりお釣り額を計算する
4. お釣りを排出する

---

次に、「分解したフローの入力と出力を定義する」ところである。
未経験の新人はここを特におろそかにしやすい。自分で分解したフローなのだから自分が一番把握しているはずである。
その入力と出力が定義できないということは、そもそもフロー自体が間違っている可能性が高い。

例の1番「バーコードの読み取りを行い単品額を求める」を考えると、入力：バーコード（一個）、出力：単品額、となる。
当然すべてのフローで定義しこれで全体の入力・出力と一致するかまで確認する。

1. バーコードの読み取りを行い単品額を求めるの繰り返し
    - 入力：バーコード（一個）
    - 出力：単品額
2. 合計額を計算する
    - 入力：単品額の集まり
    - 出力：合計金額
3. 投入された代金をよみとりお釣りを計算する
    - 入力：合計金額
    - 入力：投入された代金
    - 出力：お釣り額
4. お釣りを排出する
    - 入力：お釣り額
    - 出力：○○円札何枚
    - 出力：□□円玉何枚

入力一つで、出力が複数になる場合も、入力が複数で、出力が一つになる場合もある。

---

最後にやることは、「大きな処理フローを分岐のある小さい処理フローに分ける」である。
この段階で分岐を含む細かい処理を決めていく。
どの言語を使うかによりどのくらい細かい粒度で書くかが変える必要があるが、処理自体は変化しない。
経験豊富なエンジニアはこのレベルは無意識でやってしまっていることが多い。

例の「お釣りを排出する」の場合は、

- 入力のお釣り額が○○より大きいなら、○○円札を1枚追加、お釣り額から○○引く、の繰り返し
- 入力のお釣り額が□□より大きいなら、□□円玉を1枚追加、お釣り額から□□引く、の繰り返し

となり、ソースコードに近いものとなる。

---

## 最後に

つまり、新人が仕様を読んで、コードが書けないのは、その間にある処理フローをそもそも作れないところにある。
処理フローを考えることこそがプログラミング上達の一番の近道である。


