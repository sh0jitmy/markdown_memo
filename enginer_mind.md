# はじめに
Qiitaが新人プログラマ応援イベント中ということなので、新人エンジニアに意識してほしいことをまとめてみました。

# １．「意見」と「事実」を混合しない
会話の中に**「意見」**と**「事実」**が混合することで、なんの根拠もない**「意見（推論）」**が**「事実」**であるかのように伝わってしまう危険性があります。
この「意見」と「事実」の混合が相手の勘違いや確認の手間を生み出します。
個人的にですが、エンジニアは特に意見や推論を説明することが多い業種だと思っています。
そんなエンジニアだからこそ、予期せぬトラブルに直結する恐れがある**「意見」**と**「事実」**の混合には特に気をつけた方が良いです。

こんな会話を経験したことのある人もいるのではないでしょうか？

【ケース】
障害対応について、新人が先輩に報告する際の会話。
※「先輩感じ悪いな」と思うかもしれませんがご了承ください。わかりやすくするためです。

=====================

**新人**： 今はもう直ったみたいですけど、Aサーバーが不調でした。

**先輩**： みたいってなんだよ・・・。解決済の障害ってこと？どんな障害だったの？

**新人**： 解決済です！Aサーバーへのリクエストがタイムアウトしてるとユーザーサポート窓口より連絡がありました。

**先輩**： 解決済なのね。原因は？

**新人**： 原因はわからなかったですが、自然に直ってて、今はタイムアウトしてないです。課長にも報告済ですが課長的にも問題なさそうでした。

**先輩**： 原因わからないなら解決してないじゃん。それで課長が問題ないって言ったの？

**新人**： えっと、直接そう言われたわけではないです。障害の内容と今タイムアウトしていないことを伝えたら「わかった。報告ありがとう。」とだけ言っていて特に指摘もなかったので大丈夫かなと思いました。実際すぐに復旧しましたし。

**先輩**： ・・・。ユーザーサポート窓口には連絡したの？

**新人**： しました！一時的なものですって伝えたのですがあまり納得はしてなかったです。

**先輩**： 納得してなかったんだ？どんなこと言われたの？

**新人**： いや特に何を言われたってわけじゃないんですけどそんな感じの喋り方でした。

**先輩**： そんな感じって・・・。

=====================

少し極端な例ですが、この会話では**「意見」**と**「事実」**が混合しています。

最初の「今はもう直ったみたいですけど、Aサーバーが不調でした。」という報告を受けた場合、人によってはもう障害が解決していると錯覚してしまうかもしれません。
しかし、実際には原因も影響範囲もわからずに**「またその障害が発生するリスクのある状態」**のまま放置しているだけです。

また、課長やユーザーサポート窓口の人の言葉を**勝手に解釈して**、言われていないことを言われたことかのように伝えています。

**「意見」**と**「事実」**はどちらも大切です。
報告において**「事実」**だけしか言ってはいけないわけではありません。

大事なのは、どちらなのかをハッキリと**「区別」**することです。

たとえ断定した言い方をしていても、根拠の無いものは**「事実」**とは言えません。
**「事実」**を伝える場合は、そう判断した根拠と共に伝える必要があります。
**「意見」**を伝える場合は、それが**「意見」**であることをしっかりとわかるように伝えなくてはいけません。

# ２．「自分が話したいこと」ではなく「聞かれたこと」を説明する
報告の際に**「自分が話したいこと」**を優先して話すと、報告を受ける側は話の理解が難しくなります。

【ケース】
新人が障害を解決した際の報告。

=====================

**先輩**： さっきの障害の原因ってなんだったの？

**新人**： それがですね、初めログを見たんですけど何も出力されていなくて。途方に暮れて部長に相談したら、「設定見直して」って言われたのでサーバーの設定資料と実際の設定を見比べてみました。いくつか差分があったのでひとつひとつ確認しながら設定を変えていったら直りました。「誰がこの設定したんだ」って部長が怒ってましたよ。

=====================

上記の例では大変だったのは伝わってきますが、**「聞かれたこと」**より**「自分が話したいこと」**を優先したため聞いたことの答えがわかりづらくなっています。

「さっきの障害の原因ってなんだったの？」という質問の答えは「サーバーの設定○○が××になっていたためです。設定資料と異なっていました。」

で済みます。
もちろん雑談等であれば聞かれた以上のことを話すのはむしろ話し上手なのかもしれません。
しかし、報告の場では聞かれたことを話すべきです。

# ３．「結論」から話す
ビジネスにおいて、相手のためを思うのなら**「結論から話す」**べきです。

**結論　⇒　理由　⇒　理由の詳細**

もしくは

**結論　⇒　理由　⇒　事例　⇒　結論**

といった順番で話すことで、聞き手が**「自分から」**あなたの話を整理しつつ聞いてくれます。
何よりも話が脱線しづらく時短になります。

# ４．「失敗」を隠さない
**「失敗」**は決して悪いことではありません。
それによって会社の業績が傾いたり人を傷付けたりしていない限りなんとでもなります。
（そもそも新人のうちはそんなリスクのあるタスクは担当しないです。）
良く言われているありきたりな言葉ですが、**「失敗の経験が成長の糧となる」**というのは私自身実体験で感じています。
失敗することで適切なアドバイスをもらえ、また次に失敗しないためにどうすれば良いかを考えるようになります。

そもそも失敗を隠すことでのデメリットが多すぎます。
見つかった時のこともそうですが、人に見せる「自分」に完璧を求めるようになってしまいます。

# ５．「指示待ち人間」にならないようにする
「指示待ち人間」より「率先して動ける人間」の方が重宝されるのは感覚的にわかると思います。
指示する側は、指示する手間が省ける分他の仕事が出来るからです。

しかし、「率先して動ける人間」にも注意点があります。
**「指示待ち人間になるな」**は**「勝手にやっていいよ」**ということではないと意識すべきということです。
自分のやっていたタスク、チーム全体のタスクと優先度、タスクの難易度を考えた上で、

「抱えているタスクが終わりました。他に作業がなければ優先度が高く、今までやっていたタスクとの類似性も高いため次に○○をやろうと思いますがよろしいでしょうか？」

といった**「やっていいかの確認」**をすべきです。
これだけで仕事を振る立場の人間は助かります。

# ６．「目的」と「手段」を混合しない
例えば、設計書作成はコーディングをスムーズに行う（もっと突き詰めるとシステムを動かす）という**「目的」**ための**「手段」**です。
設計書作成が目的ではないです。
**「目的」**と**「手段」**を混合することで、**「取れる手段がひとつになる」**という危険性があります。
本来であれば**「ゴール」**に行くための**「道」**は複数あるはずです。
しかし、その道を進むことを目的としてしまうと**他に良い道があったとしても気付くことはありません**。

# ７．問題の深掘りをする
問題が発生した際に、常に**「直接原因」**と**「根本原因」**を考えます。
当然起こっている直接的な原因を知ることは重要です。
しかし、問題の直接的な原因だけを見ていると**「本当の意味での対策」**をたてられないことがあります。
初めのうちは**「なぜなぜ分析」**や**「ロジックツリー」**を書くことで「問題の深掘り」の訓練をすると良いと思います。
このスキルはビジネスだけでなく人生でも武器になります。

# ８．クローズドクエッションを心がける
まず自分で調べて自分なりの答えを持ったうえで「〇〇だと考えていますが合っていますか？」と質問します。
この質問の方法は相手が「はい／いいえ」で答えるだけなので効率が良いです。
さらに、自分で調べて一旦の結論をつける訓練になります。
「何がわからないのかがわからない」なんて時は気軽にオープンクエッションで質問しても良いと思います。

# ９．タスクを細分化する
タスクが細分化されることでタスクを定量的に図りやすくなります。
つまり自分でタスクの計画がたてやすくなります。

# １０．振られているタスクの意味（誰がなんのために必要としているか）を聞く
誰がなんのためにそのタスクを必要としているのかを理解することで、成果物のゴールがハッキリとします。
成果物のゴールがハッキリとしないと手戻りや品質が悪くなるリスクを負います。

# １１．優先順位を決める
複数のタスクを与えられた場合、とりあえずタスクの上からこなすのではなく優先順位を決めます。
**「重要度」**と**「緊急度」**で分けて考えると優先順位を決めやすいです。

第１優先：重要度が高く、緊急度の高いタスク
第２優先：重要度が低く、緊急度の高いタスク
第３優先：重要度が高く、緊急度の低いタスク
第４優先：重要度が低く、緊急度の低いタスク

優先度が決められない、もしくは同程度であれば**「難易度の高いもの」**からこなすのが良いです。
難しい仕事は思っている何倍も時間がかかったりするものです。

# １２．納期を確認する
優先順位の話と関連しますが、タスクを振られたらまず**「納期」**を確認する必要があります。
納期がなくいつまでも時間をかけて良いような仕事はありえません。
そして、**「納期」**によって**「緊急度」**が変わってきます。
「それいつまでですか？」を口癖にしても良いくらいです。

# １３．会議で意見を言う
私は**「会議で最低１回は発言する」**という自分ルールを設けています。
実際の会議の内容によっては発言なしの場合も多々あるのですが、**「何を質問しようかな」**という気持ちで会議に臨むと、自然とその会議に向き合うことが出来ます。
常に話の矛盾点や説明の足りない部分を見つけようとする必要はありません。わからないことを質問するだけでも良いです。

# １４．プロ意識を持つ
新人に「プロ意識を持て」なんて言うと「ブラック企業的な考えだ」なんて言われてしまうかもしれません。
しかし、新人で右も左もわからない状態だとしても給料は発生しています。
**「給料をもらって働いている以上、最低限給料分はプロとして行動すべき」**だと私は考えています。
やる気がなくても、仕事が面倒臭いと思っていても、それはその人のスタイルなので良いのかなと思います。ただ、労働の対価としての給料なので、もらった分くらいはきちんと働いた方が良いのではという心掛けの話です。
新人のうちは**「早く仕事を覚えて戦力になる」**がプロとしてやるべきことです。

# １５．人と比べない
人間はどうしても自分と人とを比較してしまいます。
「あいつは全然出来ていない」と**「安心感」**を得たり、「あいつはすんなり出来て良いよな」と**「劣等感」**を感じたり。

私自身、すぐ自分と人を比べてしまいます。それによって心が穏やかでなくなることもあります。
劣等感を払拭するために承認欲求が強くなったり、その劣等感をバネに成長しようと考えたこともあります。
しかし、劣等感をバネに成長したとしてもさらに上の存在が必ずいます。それこそ自分が一番にならなければその劣等感からは解放されません。
そんなデメリットが多い行為で心を乱すよりも**「他人との差は気にしない」**方が健全な精神を保てます。

もし何かと比較をしたくなったら、**「過去の自分」**や**「過去こうなろうと思っていた自分」**と**「今の自分」**を比較しましょう。

# さいごに
本記事には書いていないですが他にも意識すべきものがたくさんあります。
これらはあくまでも私流の新人から成長するための方法であって、当然正解というわけではないです。
他にも「こんなこと意識した方が良いよ。」ということがあれば教えてください。

今回は新人向けの記事ですが、先輩社員向けの記事も書いてます。

https://qiita.com/shinkai_/items/c94791a1c4e0279417af

評価の上げ方についても書いています。

https://qiita.com/shinkai_/items/56f451141eaebb679d98

以上です。誰かの参考になれば幸いです。

