# 休憩後の予定時間

Ankiを毎日使用していると、カードが正しく回答されるたびに間隔が長くなります。例えば、「良い」を選択すると、間隔が約2倍になります。したがって、5日待ち、次に10日待ち、20日、40日と続きます。

数週間または数ヶ月間学習を中断した後にデッキに戻ると、間隔が非常に長くなっていることに驚くことがあります。これは、Ankiがカードが実際に見られなかった時間を考慮し、予定されていた時間だけを考慮しないためです。したがって、カードが5日後に予定されていたが、1ヶ月間学習しなかった場合、次の間隔は10日よりも60日に近くなります。

これは良いことです。1ヶ月待った後にカードを覚えていた場合、さらに長い間隔でも覚えている可能性が高いです。通常の使用でSRS（間隔反復システム）が効果的であるのと同じ原理が、遅延後の学習にも適用されます。また、1ヶ月待った後に簡単に答えられたカードを10日後に予定するのは意味がありません。逆戻りしてしまいます。

デッキをリセットするのはさらに悪い解決策です。長期間の不在後にデッキに戻ると、多くのカードを忘れているかもしれませんが、すべてを忘れているわけではありません。デッキ全体をリセットすると、すでに知っている内容を学習するために時間を無駄にすることになります。

今、予定より遅れているカードがあり、それを思い出すことができたが、予定通りに復習されなかったために快適ではなかった場合があります。これに対処するために、Ankiはあなたの回答に応じて遅延を異なる方法で処理します。カードが簡単だと感じた場合、最後の間隔と完全な遅延が合計され、次の間隔を計算するために使用されます。「良い」と答えた場合、遅延の半分だけが使用されます。「難しい」と答えた場合、追加の遅延は使用されません。したがって、カードが5日後に予定されていて、20日遅れて回答された場合、次の予定時間はおおよそ次のようになります：

- 難しい: 5 \* 1.2 = 6日

- 良い: (5 + 20/2) \* 2.5 = 37.5日

- 簡単: (5 + 20) \* 3.25 = 81.25日

正確な数値は、過去のカードのパフォーマンスやデッキの設定によって異なります。

カードが難しいと感じた場合、次の間隔は控えめで、追加の遅延は無視されます。カードが良いと感じた場合、次の間隔は約50%だけ長くなります。簡単だと感じた場合、通常通り積極的に間隔が延長されます。

したがって、Ankiにしばらく戻ってきたときは、通常通りに学習することをお勧めします。しかし、どうしてもデッキをリセットする必要がある場合は、ブラウザでリセットするカードを選択し、カード > 忘れる を使用できます。