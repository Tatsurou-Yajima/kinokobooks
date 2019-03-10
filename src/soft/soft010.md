# 【10】定量化を求めよ{#e10}

<div class="author">キース・ブレイウェスト</div>

　「速い」は、要件にはなりません。「反応がいい」とか「拡張性がある」もそうです。 これらが要件にならないのは、要件を満たすかどうかを判断するための客観的な指標がないからです。しかし、ユーザーは、こういう要求をしてきます。アーキテク卜の役割は、広く言えば、こうした要求を実現することであり、あれこれの要求のバランスを取って矛盾や摩擦を抑えることです。客観的な指標がなければ、「まだ全然速くないのでこれではダメだ」と言う気まぐれなユーザーや、「まだ全然速くないのでリリースできない」と言うこだわりの強いプログラマーにもみくちゃにされてしまいます。

　こういった要求も、要件と同じように紙に書き出しましょう。すると、「柔軟な」とか「メンテナンス性の高い」といった曖昧な形容詞が登場してきます。「使いやすさ」というようなことでも、定量化し、限界値を設定しなくてはいけません。定量化しなければ、ユーザーはシステムを受け入れる基準をなくし、プログラマーは上司からの指示を的確に把握できず、アーキテクトのビジョンがぼやけることになります。

　定量化するには、簡単な質問をしていきます。いくつ？　いつまでに？　どのくらい頻繁に？　どれくらい速く？　増える？　それとも減る？　どのくらいの割合で？　こういった質問に答えられないようであれば、そのニーズは受け入れられません。ユーザー要件には、こうした質問への答えが含まれていなければなりません。そうでないなら、よく考える必要があります。あなたがアーキテクトで、ビジネスサイドの人々がこれらの数字を言わない、あるいは言おうとしないなら、なぜ言わないのかを考えましょう。そして、行動を起こすのです。今度誰かが「システムは拡張性が高くなくてはならない」と言うようなら、その人物に、利用者がいつ、どんな理由で増えるのか聞きましょう。いつ何人が増えるかです。「たくさん」とか「すぐに」という答えを受け入れてはなりません。

　はっきりさせられない場合には、最小値と最大値の範囲を決めてもらいます。最小値は形ばかりで無視していいでしょう。もし、この範囲すら与えられないなら、要求は理解不能です。

　あとはアーキテクチャーが形になってきたときに、この指標を使ってシステムが許容範囲にあるかチェックします。開発が進んで指標を満たせなくなってきたら、それまでの作業に問題があるという意味のあるフィードバックが得られます。指標化し、チェックすることは、時間もコストのかかる仕事です。もし、「システムはパフォーマンスが良くなければならない」という要件とは言えない要求を見て誰も何とも思わないようなら、おそらくパフォーマンスはどうでもいいのです。他のもっとがんばりがいのあることにアーキテクチャーの力点を置けばよいでしょう。

　要件として認められるのは、このような形のものです。「1500 ミリ秒以内にユーザーの入力に反応しなければならない。通常の負荷（この定義も必要ですね）のもとでは、平均的な応答時間は 750 ミリ秒から 1250 ミリ秒の間でなければならない。応答時間が 500 ミリ秒以下になっても、ユーザーからは見分けがつかないので、それ以上苦労しても意味がない」