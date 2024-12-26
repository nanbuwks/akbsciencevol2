---
title: Microsoft Wordの数式をQiita記事用のTeX形式に変更する話
tags: Microsoft Word TeX
author: kazueda
slide: false
---
## はじめに
秋葉原ロボット部の理論グループでは、勉強会に関する内容の記事をQiitaのAdvent Calendarにまとめています。

https://qiita.com/advent-calendar/2024/akbrobot_theory

　原稿作成時には、使い慣れたMicrosoftのWord上の「記号と特殊文字」内の「数式」を用いて数式を作成しています。
　完成した原稿の内容をそのままQiitaの編集画面にコピー・ペーストするだけでは、数式が表示されません。
 　締め切りの厳しい状況では、Wordで表示される数式のキャプチャー画像を貼り付けることにより、締め切りに間に合わせています。
  　投稿されたAdvent Calandarの記事は、公開後、冊子体の形で頒布されます。 
　冊子体用原稿に編集する際には、数式のレイアウトをするためにTeX形式での表記に修正することとなります。
　Texの書式を睨みながら修正するのを回避するために、Wordファイルを色々触ってみたところ、不完全ながら、Word上の数式をQiitaのmath書式に変換することができました。

## Wordの数式からQiitaのmath形式への変換
　ここでは、「一次元人の世界を理解するための接続係数の使い方を妄想してみた」内の式を例に説明します。

https://qiita.com/kazueda/items/df180a8ae0116b2aba3c

　Word上の数式をクリックすると、Window上部のタブに「数式」が表示されます。
 　「数式」をクリックすると、「変換」の部分に「LaTex」ボタンが表示されます。
　この「LaTeX」をクリックしたのち、右隣の「変換」をクリックします。
　どのように変換するのかが選択できるので、「現在‐行形式」をクリックすることで、数式がLaTex形式に変換されます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/693019/ce4a70c3-3618-08d4-cc10-f656e89bf8bc.png)

　
　変換後の文字列と、math形式を使ったときの表示を示します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/693019/ed3c86c8-f57c-7ab9-e9a0-de29aa7a81a4.png)
  上記の数式を「行形式」に変換すると、以下の文字列となります。

e_p=\frac{\partial\\mathbf{mathbit}{\mathbf{x}}}{\partial 
p}=\left(\begin{matrix}1\\0\\\end{matrix}\right),\ \ e_q=\frac{\partial\\mathbf{mathbit}
{\mathbf{x}}}{\partial q}=\left(\begin{matrix}0\\1\\\end{matrix}\right)

　この文字列を「\```math」と「\```」の間に記載すると以下の表示になります。
$$
e_p=\frac{\partial\mathbit{x}}{\partial p}=\left(\begin{matrix}1\\0\\\end{matrix}\right),\ \ e_q=\frac{\partial\mathbit{x}}{\partial q}=\left(\begin{matrix}0\\1\\\end{matrix}\right)
$$
　 太字の斜体の部分が反映されず「\\mathbit」と表示されています。「mathbit」の部分を「symbfit」に置き換えることで、太字の斜体を表現することができます。
$$
e_p=\frac{\partial\symbfit{x}}{\partial p}=\left(\begin{matrix}1\\0\\\end{matrix}\right),  \ \ e_q=\frac{\partial\symbfit{x}}{\partial q}=\left(\begin{matrix}0\\1\\\end{matrix}\right)
$$
 ## おわりに
 　数式を含むWordファイルから、TeX形式の数式を含むWordファイルへの変換について説明しました。
　実際に使用する場合は、「変換」の際に「すべて-行形式」を選択すると、すべての数式の変換が行われます。その後、太字の斜体の部分を一括置換で修正します。Qiitaでエラーの出ないTeX形式の数式の含まれた原稿が作成できるかと思います。

  

---
title: 「脳のクラス図」（４つの意識、時の流れ、左右の扁桃体と大脳皮質）
tags: 意識 扁桃体 大脳皮質 時の流れ
author: tshimizu8
slide: false
---
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/78212/fbc1372c-358b-1d9b-931a-af357baf95da.png)

脳全体（ホール・ブレイン）を活かして思考のクセを変える――『WHOLE BRAIN 心が軽くなる「脳」の動かし方』より 
https://nhkbook-hiraku.com/n/nf3412275e530 

# はじめに
こんにちは清水です。
脳科学者のジル・ボルト・テイラーは脳出血で、自分の左脳がシャットダウンするプロセスを体験した。その報告であるTEDと本は大きな影響を与えた。

* TED日本語 パワフルな洞察の発作 https://digitalcast.jp/v/18436/
* 奇跡の脳―脳科学者の脳が壊れたとき 2012

本記事は彼女の2冊目の著書「WHOLE BRAIN(ホール・ブレイン) 心が軽くなる「脳」の動かし方 2022」をもとに、脳のクラスなどを作成したものである。この本は少しスピリチュアルに傾斜しすぎと感じられるところもある。

一般に左脳と右脳の特徴は、つぎのように考えられている。

|項目| 左脳| 右脳 |備考 |
|:-----------|:------------|:------------|:------------|
| 時間    | 過去、現在、未来 | 現在 |計画と実行。都市、文明|
| 視点     | 部分（木） | 全体（森） ||
| 機能      | 差異、秩序化（分類、関係） | 同一性、抽象化 ||
| 思考     | 言語 | イメージ、視覚 |視覚思考者：アインシュタイン、イーロン・マスク|
| 分野      | 言語、計算、理論など論理的、概念的な思考       | 音楽、幾何学、発想など芸術的な分野に関連 ||

# 要点
## 複数の意識、人格
1. 分離脳では左脳と右脳にそれぞれ意識が宿る。（てんかん患者の脳梁離断手術）
1. 解離性同一性障害では１人に複数の意識が宿る。（1人のなかに13人の意識の報告あり、年齢や性別や運動スキルが異なる）

## 時間と自己概念と欲望
1. 時の流れ（過去、現在、未来）の内、単細胞生物には現在のみ、過去と未来は認識していない。現在のパターンに反応しているのみ。
1. 現在を記憶し、過去情報を生存に役立てるようになった。。
1. 右脳は現在のみ、左脳は時の流れ（過去、現在、未来）を認識する
1. 自己境界はあいまい。ラバーバンド実験。自己境界は記憶から生成される。
1. 記憶から自己概念が創造される。自他が創造される。不安がうまれ欲望が生まれる。

## 右脳は悟りの境地
1. 今、ここに集中する
1. ワンネス（全ては一つ、自他の区別がない）
1. 自己概念の消失。欲望がない。

## 左脳のシャットダウンプロセス
1. 体の境界という感覚が消える （自分が宇宙の広大さと一体になった気がした）
1. 記憶の喪失による、安堵と歓び
1. 知覚できる全てのものは、今、ここにあるもの。未来や過去は想像できない。何事も急いでする必要なないと感じた。
1. 満ち足りた幸福感
1. 左脳の「やる」意識から右脳の「いる」意識へ変化
1. 図と地がわからなくなる。文字が認識できなくなる。
1. 臨死体験と重複する部分あり(https://ja.wikipedia.org/wiki/臨死体験)

## 言語と左脳
1. 多くの人は左脳で言語を処理する
1. 右利きの人の90％が左脳で言語を処理し、2％が右脳処理で、8％は両方の脳で処理する
1. 左利きの人の約３分の２も左脳で言語を処理する
1. ブローカ野（左前頭葉、運動性言語中枢）、ウェルニッケ野（左側頭葉、知覚性言語中枢）
1. 左脳 混沌とした世を整理し、分類し、数え、一覧表にし、最終的に、他者と意思疎通するための構造的な言語を生み、すべての物に名前をつける


## 物理的世界と空
1. すべてのものは空間のなかで振動する原子と分子や素粒子からできている。すべては流動している存在。動的なパターンがあるだけ。動的な関係があるだけ。永遠不変な実体はない。
色即是空。諸行無常。空。諸法無我。
1. 物理的世界から五感センサーにより情報を取得して、世界像（仮想世界）を創造する

# 脳のクラス図
「脳のクラス図」をつぎに示す。　このクラス図には、4つの意識、時の流れ、左右の扁桃体、左右の大脳皮質などの要素が含まれる。

<!-- ![alt](https://yuml.me/diagram/scruffy/class/draw
// -[note: キャラ１ー４]  
[世界{bg:yellow}]->[五感{bg:cyan}]->[脳{bg:cyan}]
[時の流れ{bg:red}],[今、ここ{bg:green}],[過去{bg:red}],[未来{bg:yellow}]
[左扁桃体{bg:red}],[右扁桃体{bg:green}]
[キャラ２{bg:red}],[キャラ３{bg:green}]
[キャラ１{bg:red}],[キャラ４{bg:green}]
[左大脳皮質{bg:red}],[右大脳皮質{bg:green}]
[記憶、経験{bg:red}],[言語{bg:red}],[自他{bg:red}],[自我{bg:red}] 
[扁桃体{bg:cyan}]-[note: 緊急事態発令]
[脳]^-[大脳皮質{bg:cyan}]
[脳]^-[大脳辺縁系{bg:cyan}]
[大脳皮質]^-[左大脳皮質],[大脳皮質]^-[右大脳皮質],
[左大脳皮質]^-[キャラ１],[右大脳皮質]^-[キャラ４],
[左大脳皮質]拡張-[左扁桃体],[右大脳皮質]拡張-[右扁桃体],
[大脳辺縁系]^-[扁桃体]
[扁桃体]^-[左扁桃体],[扁桃体]^-[右扁桃体]

[時の流れ]^-[過去],[時の流れ]^-[未来]
[時の流れ]^-[今、ここ]->[右扁桃体]->[キャラ３]
[時の流れ]->[左扁桃体]->[キャラ２]
[過去]->[記憶、経験],[記憶、経験]->[言語],[記憶、経験]->[自他],[記憶、経験]->[自我]
[キャラ２]-[note: 不安（未来）、怒り、幸せ（一過性）]
[キャラ３]-[note: 恐怖（例ヘビ）、好奇心、喜び（永続）]
[世界]-[note: 一見無秩序\n物理的には分子、原子、素粒子]
[キャラ１]-[note: 時間：過去、現在、未来\n自己：自他、貪欲、競争\n視点：部分、差異、秩序化\n思考：言語（意味）、学問\n価値：外面的な富や名声]
[キャラ４]-[note: 時間：現在\n自己：ワンネス、無欲、協調\n視点：全体、同一性、抽象化\n思考：形（イメージ）、祈り瞑想\n価値：尊い生命体として自分自身]
[大脳皮質]-[note: 新しい脳 \n 思考組織]
[大脳辺縁系]-[note: 古い脳 \n 感情組織]
[意識、価値観{bg:yellow}]^-[キャラ１],[意識、価値観]^-[キャラ２],[意識、価値観]^-[キャラ３],[意識、価値観]^-[キャラ４]
[脳の作戦会議{bg:yellow}]<>-[意識、価値観]
-->
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/78212/857d23b5-5137-47f4-58d0-f1f25dd6e95d.png)


## 進化の物語

1. 最初は古い脳（感情組織）として左右の扁桃体があった。人間は感じる動物。脳には「現在」のみがあり過去や未来という概念はなかった。
1. つぎに左の扁桃体が「時の流れ」を認識した。過去情報は生存に役立った。
1. 新しい脳（思考組織）として大脳皮質が発達した。考えることもできるようなった。
1. 左脳は過去情報を記憶として蓄積した。記憶情報より自己と自他の概念が創造された。
1. 左脳は「未来」概念を発明した、計画を立て未来を創造した。道具や建物を作り始めた。文明の構築が始まった。
1. 左脳は未来への不安を感じるようになった（飢餓など）。不安から貪欲になった。
1. 言語が誕生し左脳は言語で考えるようになった。
1. 右脳はイメージで考える。右脳は今ココ、で無欲。

# ４つの意識
個別の脳組織脳に個別の意識がやどり、それぞれ特徴（キャラクター）を持つ。
４つのキャラに「脳の作戦会議」を開かせ、賢明な選択を行う。

|意識名称|脳組織|特徴
|:-----------:|:------------|:------------|
キャラ１|左大脳皮質|現在と過去と未来、自己創造、自他、記憶
キャラ２|左扁桃体|不安、怒り、幸せ（一過性）、記憶
キャラ３|右扁桃体|好奇心、喜び
キャラ４|右大脳皮質|今ココ、ワンネス、主体と客体はひとつ、悟り

# ４つのキャラの例

|意識名称|ビジネスのやり方|体の捉え方|
|:-----------:|:------------|:------------|
キャラ１|利益を上げたい|体を乗り物と考えている|
キャラ２|アイデアや細部をもてあそびたい|体に責任を感じている|
キャラ３|とにかく楽しいことをしたい|体をおもちゃだと感じている|
キャラ４|より善きことをしたい|体を魂の神殿ととらえている|

# おわりに
左脳をオフにできる人がいるらしい。左脳をオフにした右脳だけの世界を体験してみたい。満ち足りた幸福感を感じてみたい。

ロボットと意識と時間に関して謎は多い
* ロボットに自己意識が必要か？、ロボットに不安が発生し、欲望が発生するのか。ロボットに生存本能を持たせるべきなのか？
* 時間の流れの認識がすべてのはじまりなのか？
   時間の流れ→記憶→自己→自他→欲望→闘争
* 悟りロボット（右脳ロボット）を実装してみたい  （キャラ３、キャラ４）
* ロボットに感情は必要か？ 恐怖、不安、喜び。 （キャラ２、キャラ３）
* 未来概念は人が発明したのか？未来概念をロボットに予測として実装する？

今後は数式による意識の定式化を考えて行きたい。

# 参考URL
selected just for you
TED日本語 - ジル・ボルト・テイラー: パワフルな洞察の発作
https://digitalcast.jp/v/18436/

世界は脳の幻想？生き残った右脳が見た世界がヤバすぎた話。『私の中の私たち』とは・・・？【脳科学 ジル・ボルト・テイラー 左脳と右脳 都市伝説】
https://www.youtube.com/watch?v=1VhZlZLymZ0

左脳の機能失った脳科学者が発見､凄い脳の使い方
4つのキャラを知れば､なりたい自分になれる
https://toyokeizai.net/articles/-/614620?display=b

# 参考文献

* WHOLE BRAIN(ホール・ブレイン) 心が軽くなる「脳」の動かし方 2022 ジル・ボルト・テイラー
* 奇跡の脳―脳科学者の脳が壊れたとき 2012 ジル・ボルト テイラー
* 決定版　脳の右側で描け 2013 ベティ・エドワーズ 
* ぼくが13人の人生を生きるには身体がたりない。: 解離性同一性障害の非日常な日常 2020 haru
* 左脳さん、右脳さん。　―あなたにも体感できる意識変容の５ステップ 2023 ネドじゅん
* 自閉症だったわたしへ 2000 ドナ ウィリアムズ 
* ドナの結婚: 自閉症だったわたしへ 2002 ドナ ウィリアムズ
* 自閉症の僕が跳びはねる理由 2016 東田直樹
* 日経サイエンス　2024年12月号 瞑想の神経科学　「無の境地」をもたらす脳の変化 M. D. サチェット他

# 参考 ウィキペディア
https://ja.wikipedia.org/wiki/脳機能局在論#右脳・左脳論
https://ja.wikipedia.org/wiki/分離脳
https://ja.wikipedia.org/wiki/解離性同一性障害
https://ja.wikipedia.org/wiki/大脳辺縁系
https://ja.wikipedia.org/wiki/脳機能局在論#言語野
https://ja.wikipedia.org/wiki/ブローカ野
https://ja.wikipedia.org/wiki/ウェルニッケ野
https://ja.wikipedia.org/wiki/ゲシュタルト崩壊
https://en.wikipedia.org/wiki/Jill_Bolte_Taylor

https://ja.wikipedia.org/wiki/臨死体験
https://ja.wikipedia.org/wiki/臨死体験#科学的な仮説・解釈
https://ja.wikipedia.org/wiki/臨死体験#側頭葉てんかん説
https://ja.wikipedia.org/wiki/臨死体験#側頭葉てんかん説への批判

# 付録
【あなたは４人いる！？】WHOLE BRAIN　心が軽くなる「脳」の動かし方｜ジル・ボルト・テイラー より
https://masudabooks.com/2024-05-10/

# 左右の考えるキャラ１と４   （第３章「脳を支えるチーム」）
機能を知覚して処理する方法がほぼ正反対
|  |左脳の〈考えるキャラ１〉| 右脳の〈考えるキャラ４〉 |
|:-----------:|:------------|:------------|
|1|  （直列プロセッサ）|（並列プロセッサ）|
|2|  言葉による|言葉によらない|
|3| 言語で考える|絵で考える|
|4|順序だてて考える|経験にもとづいて考える|
|5|過去／未来にもとづく|現在の瞬間にもとづいて考える|
|6|分析的|運動感覚的／身体的|
|7|細部に注目|総合的に対局を見る|
|8|違いを探す|類似点を探す|
|9|手厳しい|思いやりがある|
|10|時間を守る|時間の流れに没入する|
|11|個別に|集団で|
|12|簡潔／正確|柔軟性／弾力性|
|13|固定した|さまざまな可能性に柔軟|
|14|「私」を重視|「私たち」を重視|
|15|忙しい（手がふさがっている）|手が空いている|
|16|意識的|無意識|
|17|構造物／整列|流動的／流れ|

# 左右の感じるキャラ２と３
感じ方がほぼ正反対
|  |左脳の〈感じるキャラ２〉| 右脳の〈感じるキャラ３〉 |
|:-----------:|:------------|:------------|
|1|抑圧された|おおらか|
|2|融通がきかない|オープン|
|3|用心深い|危険を厭わない|
|4|恐怖心にもとづく|怖いもの知らず|
|5|厳格|フレンドリー|
|6|条件付きで愛す|無条件で愛す|
|7|猜疑|信頼|
|8|いじめる|支える|
|9|正義を求める|感謝する|
|10|あやつる|流れに任せる|
|11|定石|創造的／革新的|
|12|個別で|集団で|
|13|利己的|分かち合う|
|14|批判的|優しい|
|15|優れた／劣った|平等|
|16|正しい／まちがっている|文脈によりけり|

<!--

-->

---
title: 『FreeCADの作図方法によるファイルサイズの違いの調査』で作成したデータをFEMにかけてみました〜その4〜
tags: FEM FreeCAD
author: toshita172
slide: false
---
# ご挨拶
こんにちは。たいちゃんです。
今年もあと僅かですね。
今回は前回の『『FreeCADの作図方法によるファイルサイズの違いの調査』で作成したデータをFEMにかけてみました〜その3〜』で予告しましたように、『FreeCADの作図方法によるファイルサイズの違いの調査』シリーズで作成した他の図形について変位と材質を変化させたときのことを投稿したいと思います。

前回迄の投稿はこちら
[『FreeCADの作図方法によるファイルサイズの違いの調査』で作成したデータをFEMにかけてみました〜その3〜](https://qiita.com/toshita172/items/1b3932c219bac586cc43)[^1]

[『FreeCADの作図方法によるファイルサイズの違いの調査』で作成したデータをFEMにかけてみました〜その2〜](https://qiita.com/toshita172/items/647a0e3764cf6b7c8b0c)[^2]

[『FreeCADの作図方法によるファイルサイズの違いの調査』で作成したデータをFEMにかけてみました〜その1〜](https://qiita.com/toshita172/items/be11f627467fb38ebafb)[^3]

更に参考となる過去の投稿はこちら
[FreeCADの作図方法によるファイルサイズの違いの調査～その1](https://qiita.com/toshita172/items/05fdde3cbe7464f3c52a)[^4]

[FreeCADの作図方法によるファイルサイズの違いの調査～その2](https://qiita.com/toshita172/items/e0cb67e51046209e5f3a)[^5]

[FreeCADの作図方法によるファイルサイズの違いの調査～その3](https://qiita.com/toshita172/items/2528d7d4836612692ce6)[^6]

# 前回迄の注意事項
前回迄の注意事項として、3DCADデータを作成したときと今回のFEM(有限要素法)をかけたときではPC自体には変更はありません。しかし、OS等はバージョンアップされています。その為、動作環境を記載しておきます。

## 動作環境
PC本体
- m-Book X400-HS　(CPU : Core i7-8565U メモリ : 16GB)
で変更なし

### 3DCADデータを作成したとき
- Debian GNU/Linux10(buster)
- FreeCAD 0.18

### FEMを3DCADデータにかけたとき
- Debian GNU/Linux12(bookworm)
- FreeCAD 0.20.2

また、FEM(有限要素法)ですが、[Wikipediaの有限要素法の項目](https://ja.wikipedia.org/wiki/%E6%9C%89%E9%99%90%E8%A6%81%E7%B4%A0%E6%B3%95)を見てみましたが、流石によく分かりません。どうも小さな領域に分けて微分方程式の近似解を得るものらしいのですが、そもそも微分方程式をよく理解してません。〜その1〜[^3]のまとめでも書きましたように材料力学の教育もほぼ受けてないというのもあるのでしょうか。

# 今回使用する図形について
今回は[FreeCADの作図方法によるファイルサイズの違いの調査～その2](https://qiita.com/toshita172/items/e0cb67e51046209e5f3a)[^5]で作成した『図形C』と『図形D』を使用します。(※『図形A』、『図形B』は『〜その1』[^4]、『図形E』は『〜その3』[^6]で出てきます。)
作り方はどちらも『Sketcher+Partの押し出し』で作成したものです。形状の詳細はリンクをご参照下さい。

## 『図形C』について
この図形は簡単に説明すると、底面がφ10mm、高さが10mmの円筒形です。
![Screenshot from 2024-12-14 19-23-07_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/1ae7d084-b185-19de-693a-a575f677a7e2.png)
具体的には上図のような図形です。

### 『図形C』の変位を変化させてみよう!

![Screenshot from 2024-12-14 19-23-07_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/799c15a6-d103-60a8-5b8c-19d088c293b5.png)

まず、前回迄同様材質はPLAから解析していきます。

![Screenshot from 2024-12-14 19-25-34_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/70ef9829-193b-0f2c-5bf5-eb5dad2c16c1.png)
今回は前回迄と同様に側面の1面を固定しようと思ったのですが、円筒形なので側面全体の固定になってしまいました。

![Screenshot from 2024-12-14 19-29-00_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/1ce427e6-f0ab-56ba-1015-e9755db0ff35.png)
前回迄のように上方向から力をこの条件で加えると、今回は真ん中が凹みました。

![Screenshot from 2024-12-14 19-29-00_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/a06b6a0c-c47b-fc2a-77ab-1ff6a96231c5.png)

こちらについても前回迄の操作を踏まえ、『CCX_Results』で解析結果が見られる状態にしておきます。また、図形の『透明度』は90に予め設定しておきます。更に、『結果タイプ』については今回も『Displacement Magnitude』を選択しておきます。『変位』のところの『表示』にチェックを入れ、『スライダー最大値』をデフォルトの1000倍の100000.0にしておきます。その後、『係数』のスライダーを上限一杯、『スライダー最大値』になる迄右に動かします。
この解析結果で『Displacement Magnitude』の場合、最小:0.00mm、最大:13.86nmでした。
(※今回も最小は0.00ということもあり、mmオーダー、最大はnmオーダーです。)

### 『図形C』の材質を変化させてみよう!!
![Screenshot from 2024-12-14 19-29-23_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/13bdb116-bf24-f7b3-5c43-ca3c0e63670f.png)

今度は材質を変化させてみましょう。同条件で材質をPLAからABSに変更します。

![Screenshot from 2024-12-14 19-30-35_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/066acf27-de04-4b72-cd09-eb9dff47953d.png)
![Screenshot from 2024-12-14 19-30-35_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/b425d8a3-ac29-7ad3-9149-132605d0073b.png)


再解析後、『Displacement Magnitude』のとき、最小:0.00mm、最大21.52nmとなりました。PLAのときは最大:13.86nmですので、『図形C』のときもABS/PLAの最大同士ではおよそ1.5〜1.6倍となっていました。
メッシュの画像の変位は前回迄とは状況が異なり、図形の形状の為か変化が分かり難いように見受けられます。
『ヤング係数』はPLAが3640.00MPa、ABSが2300.00MPaです。『ヤング係数』は大きいと変化(ひずみ)が少なくなる数値とのことです。こちらもPLA/ABSの『ヤング係数』で計算すると1.5〜1.6倍になっています。

## 『図形D』について
この図形は簡単に説明すると、『図形C』をZ方向から肉厚2mmになるように中抜きをした図形です。具体的にはこの3DCADデータはφ10mm、高さ10mmの円筒形をφ6mm、高さ10mmの円筒形で中心から抜いたものです。
![Screenshot from 2024-12-14 19-44-09_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/64dfebb5-b54f-f734-9d28-875b5cd63bcc.png)
上図のような図形です。

### 『図形D』の変位を変化させてみよう!
![Screenshot from 2024-12-14 19-44-09_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/5ab224dd-f839-4da2-6473-5f04dfd69ed4.png)

こちらも材質はPLAから解析していきます。

![Screenshot from 2024-12-14 19-44-47_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/f206d416-8a1d-54e2-286c-5f8a85932beb.png)
『図形C』同様に側面の1面を固定しようと思ったのですが、こちらも円筒形なので側面全体の固定になってしまいました。

![Screenshot from 2024-12-14 19-46-18_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/e597c402-e430-67ff-cd15-92560be93bb6.png)
『図形C』同様に上方向から力をこの条件で加えると真ん中が凹みました。

![Screenshot from 2024-12-14 19-46-18_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/d402bcbf-c60c-0275-0399-01393db19cd1.png)

例によって『CCX_Results』で解析結果が見られる状態にしておきます。また、図形の『透明度』は90に予め設定しておきます。更に、『結果タイプ』については今回も『Displacement Magnitude』を選択しておきます。『変位』のところの『表示』にチェックを入れ、『スライダー最大値』をデフォルトの1000倍の100000.0にしておきます。その後、『係数』のスライダーを上限一杯、『スライダー最大値』になる迄右に動かします。
この解析結果で『Displacement Magnitude』の場合、最小:0.00mm、最大:16.39nmでした。

### 『図形D』の材質を変化させてみよう!!
![Screenshot from 2024-12-14 19-47-51_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/3d2bc60e-7687-5a92-70a8-867ddab6472b.png)

続いて材質を変化させてみましょう。同条件で材質をPLAからABSに変更します。

![Screenshot from 2024-12-14 19-48-04_Cust_a_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/46f50086-ad3e-293a-f80b-ef3bd988c87c.png)
![Screenshot from 2024-12-14 19-48-04_Cust2_b_600px.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/319826/ce301b07-8063-e759-a141-e94fabfb6d52.png)

再解析後、『Displacement Magnitude』のとき、最小:0.00mm、最大25.84nmとなりました。PLAのときは最大:16.39nmですので、『図形D』のときもABS/PLAの最大同士ではおよそ1.5〜1.6倍となっていました。
メッシュの画像の変位はこちらについては、PLAのときより大きくなったように見受けられます。

# その4のまとめ
今回はここ迄にしたいと思います。今回用いた図形は円筒形をもとにしていました。その為、前回迄の直方体とは違った変化の仕方があって面白かったです。また、前回迄の結果同様、中抜きの有無では『図形D』(中抜き有り)>『図形C』(中抜き無し)と変化に差が出ました。
今回は中抜きについては円筒形でしたが、これを例えば直方体で中抜きをしたらまた変わった値になるかもしれません。色々調べてみるのも面白いと思います。
材質を変えた場合も変えた後と変える前の比は今回も概ね一致していると思います。
最後迄お付き合い下さり有難うございました。

# 参考資料
- Debian　https://www.debian.org/
- Gmsh　https://gmsh.info/
- FREECAD A MANUAL　https://www.freecad.org/manual/
- FEM CaluculiX Cantilever 3D　https://wiki.freecad.org/FEM_CalculiX_Cantilever_3D
- FEM Workbench　https://wiki.freecad.org/FEM_Workbench
- Manual:Ceating FEM analysis　https://wiki.freecad.org/Manual:Creating_FEM_analyses
- Wikipedia 有限要素法　https://ja.wikipedia.org/wiki/%E6%9C%89%E9%99%90%E8%A6%81%E7%B4%A0%E6%B3%95
- 【改定新版】　これならわかる　[図解でやさしい]　入門　材料力学　有光　隆　2020/2/19　株式会社技術評論社


[^1]:https://qiita.com/toshita172/items/1b3932c219bac586cc43
[^2]:https://qiita.com/toshita172/items/647a0e3764cf6b7c8b0c
[^3]:https://qiita.com/toshita172/items/be11f627467fb38ebafb
[^4]:https://qiita.com/toshita172/items/05fdde3cbe7464f3c52a
[^5]:https://qiita.com/toshita172/items/e0cb67e51046209e5f3a
[^6]:https://qiita.com/toshita172/items/2528d7d4836612692ce6

---
title: 圏論（けんろん）、圏論（けんろん）、圏論（けんろん）、そして米田の補題（よねだのほだい）
tags: 圏論 米田の補題
author: zanjibar
slide: false
---
# 数学が本格的に日常に大きな影響を与える時代がきます

![秋葉原 adventcalendar .png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/48387/f1f0b690-cb55-d220-c685-2856c3f9e2d5.png)

現時点で、数学の基礎理論である圏論は知られておらず、さらに圏論の最重要定理の米田の補題を知っている人はほとんどいません。
でも、圏論はいままで、[万物の理論](https://amzn.to/3ZLmCJH)といわれていましたが、[数理科学 11月号](https://amzn.to/4iz6NgM)では、なんと　<font color="Red">万物・万事・万人</font>のための数学理論とまでいわれるようになりました

私は、以前から、圏論をしっていましたが、本格的に学んだのは、2023年1月から5月末までの入院中の約半年のことです。いまだに数学的にはよくわかっていませんですが、それでも日常に応用できるのですごいと思っています。数学は抽象的なので、通常の普段の日常とは縁がないでしょう。それが圏論は、すごく影響があります。特に圏論の最重要定理の米田の補題がすごいです。よいものの普及活動が好きな私としては、米田の補題を普及させることに使命をかんじています。

# 米田の補題の理解の前提は、圏、関手、自然変換です。どれも数学的に正面から理解しようとすると絶望的です。
東大理学部情報学科の4年生の学力が必要です。他の大学の情報学科でも、圏論は必須でないので言葉そのものを知らない人が多いです。壊滅的に難しい理論ですが、一瞬で覚えてもらう手法を模索しています。そこで考え出したのが、川柳です

# 米田の補題　関係は内容よりも重要だ

例です。

（内容）A国、B国はかくかくしかじかの国です
（関係）A国は、友好国、B国は敵対国
**関係のほうが重要でしょう**

# ポアンカレ 違うもの同じとみなすすごいこと
圏論のご先祖様 ポアンカレは、**数学は違うものを同じとみなす技術である**といいました。

なにがすごいかの例です。

おなじなら値段がやすい方がよい。普段からそうおもっていませんか？

# 圏論は矢印　矢印で考えるのはよくあるな

普段から、矢印をつかっていませんか？　
例えば、テレビでインタビューしていると、
きっかけ　→　現在
で質問をしているパターンがありませんか？
矢印を意識すると、日常生活には矢印があふれかえっています。
そして、きっかけ　→　現在は、誰かについて知りたいと思ったら、即、質問として使えます。きっかけはなんですか？　そして現在はどうしていますか？
少し数学的な話をするときっかけ、現在は、対象といいます。矢印は射といいます。

# グロタンディーク なんでもと思えるならばすごいこと
圏論で数学を書き換えた天才 グロタンディークは**対象、射(やじるし)なんでも良い**といっています。
圏論を万物の理論に方向づけたのは、グロタンディークです。
**会議でこんな会話していませんか？**
課題が解決できればなんでもよいのだから、〇〇は違う方法だけどで同じように解決できるのでは
ポアンカレやグロタンディークの言葉を意識して、会議に臨むと生産性が桁違いにあがります。私は、いま、別世界に生きている感じがしています。

# どうですか？　圏論って面白いと思いましたか？

※この文章は、米田の補題 AdventCalendar2024(https://qiita.com/advent-calendar/2024/yonedalemma) 米田の補題からの抜粋です





---
title: 大学入試問題をswiftで解く ~前編~
tags: Swift SwiftUI
author: reodon
slide: false
---
# はじめに
大学入試問題シリーズ第2弾です。

第1弾は以下を参照してください。
[大学入試問題をoctaveで解く #Octave - Qiita](https://qiita.com/reodon/items/fd0f0bd381ce92f1b886) [^1]

今回は、[Swift](https://developer.apple.com/jp/swift/) [^2] を使って解いてみたいと思います。macOS の iPhone エミュレータで動作を確認します。
本来は一つの記事にまとめたかったのですが、下記のビルドエラーに悩まされて執筆が捗らなかったため、前後編に分けました。

> the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions

本記事は前編として、作図までを実装しました。
後日公開予定の後編では、残りの面積を求める部分の実装を行い、ソースコードを公開する予定です。

# 動作環境
- macOS
  - System Version: macOS 15.2
  - Chip: Apple M1 Pro
  - Memory: 16 GB
- Xcode
  - Version: 16.2

# 入試問題
解答の対象となる入試問題です。第1弾と同じ問題です。

```math
\begin{align}
|x| + |y| - 2 & \leq 0 \tag{1} \\
x^2 + 2x - 2y - 1 & \geq 0 \tag{2} \\
\end{align}
```

```math
\begin{array}{c}
(1), (2) を同時に満たす点(x, y)の全体からなる領域を D とする。 \\
D を図示し、その面積を求めよ。 \\
\end{array}
```

## アプリでの表示
せっかくなので、アプリでも問題を確認できるようにしてみました。

![「問題」のスクリーンショット](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/501772/9fdc820f-69d2-e1ea-34b8-a7efb4f1f936.png)

WebView 内で、[MathJax](https://www.mathjax.org/) [^3] を使っています。
本来は改行しないのですが、スクリーンからはみ出さないように CSS などを駆使して無理やり改行させています。紙面の都合で、Landscape Mode のスクリーンショットを掲載していますが、Portrait Mode にすると改行されます。

# 解答
## 利用するフレームワーク・ライブラリ
- [Swift Charts](https://developer.apple.com/documentation/charts) [^4]
  - グラフを図示するために使います
  - 最新機能を利用する場合、ビルドのターゲットを iOS v18.0 以上にしないとビルドエラーになります
- [Accelerate](https://developer.apple.com/documentation/accelerate) [^5]
  - 面積を求めるための行列演算や積分で利用する予定です

## 作図
![「作図」のスクリーンショット](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/501772/043dc67e-9c55-d634-6283-99588c14c369.png)

縦横スクロール、ピンチでの拡縮に対応しています。がんばりました。

## （面積）
後編で答えを求める予定です。

# おわりに
普段は TypeScript を書くことが多いのですが、Swift は構文が特徴的だと感じました。その構文は、Ruby の[ブロック付きメソッド呼び出し](https://docs.ruby-lang.org/ja/latest/doc/spec=2fcall.html#block) [^6] に由来しているのかもしれません。
Swift Charts は比較的あたらしい SwiftUI のフレームワークのようで、サンプルコードも少なく実装に苦労しました。
できるだけ早くソースコードを公開できるようがんばります。

# おまけ
本記事を執筆する際に役立った情報を残しておきます。

## macOS
macOS のハードウェア情報とソフトウェア情報を確認するのは、下記コマンドが便利です。

```ShellSession
$ system_profiler -detailLevel mini SPHardwareDataType SPSoftwareDataType
```

## Swift
- Swift さくっと確認したい基礎文法 [Struct(構造体)] #iOS - Qiita
  - https://qiita.com/yuinchirn/items/98b568d595650eca3334
- SwiftでRangeからArrayを取得する #Swift - Qiita
  - https://qiita.com/shoma2da/items/efe1cb6e96d95959fcdd
- Swiftの範囲型を理解する #iOS - Qiita
  - https://qiita.com/roba4coding/items/a981c7faf43555753314
- Swift で上付き文字・下付き文字を表示させる - 酢ろぐ！
  - https://blog.ch3cooh.jp/entry/ios/display_superscript_and_subscript_characters

## SwiftUI
- SwiftUIで「式が複雑すぎる」「式を分解しろ」と言われたら #Swift - Qiita
  - https://qiita.com/Hyperbolic_____/items/cf808879ef8ff04a1afb
- 【SwiftUI】フォントサイズの種類とサイズのカスタム方法 | Seeds
  - https://seeds-digital.com/swiftui-fontsize/
- 【SwiftUI】onAppearの使い方と活用方法を徹底解説！ - iPhoneアプリ開発講座｜CodeCandyオンラインプログラミングスクール
  - https://blog.code-candy.com/swiftui_onappear/
- [SwiftUI] 複数ジェスチャーのサポート (Pinch と Drag の両方をサポートする) | SmallDeskSoftware
  - https://software.small-desk.com/development/2021/06/28/swiftui-pinch-and-drag/

### 公式チュートリアル
SwiftUI を触ったことがなかったので、勉強のために下記のチュートリアルを実施しました。

#### SwiftUI essentials
- Creating and combining views
  - https://developer.apple.com/tutorials/swiftui/creating-and-combining-views
- Building lists and navigation
  - https://developer.apple.com/tutorials/swiftui/building-lists-and-navigation
- Handling user input
  - https://developer.apple.com/tutorials/swiftui/handling-user-input

#### Drawing and animation
- Drawing paths and shapes
  - https://developer.apple.com/tutorials/swiftui/drawing-paths-and-shapes
- Animating views and transitions
  - https://developer.apple.com/tutorials/swiftui/animating-views-and-transitions

#### App design and layout
- Composing complex interfaces
  - https://developer.apple.com/tutorials/swiftui/composing-complex-interfaces
- Working with UI controls
  - https://developer.apple.com/tutorials/swiftui/working-with-ui-controls

#### Framework integration
- Interfacing with UIKit
  - https://developer.apple.com/tutorials/swiftui/interfacing-with-uikit

## Xcode
コーディングが捗る設定やショートカットです。

### Vim Mode
Editor > Vim Mode

### インデント、コード整形
Ctrl + I

### コメントアウト
Command + /

### 選択行の上下移動
Command + Option + [
Command + Option + ]

## エミュレータ
### ビルド
- Xcode: A build only device cannot be used to run this target. #iOS - Qiita
  - https://qiita.com/ishitan/items/5720949783b89d0af9d9

### スクリーンショット・レコード
- 【ffmpeg】動画の解像度を指定してリサイズ、アスペクト比を維持したまま解像度を変更する、回転する #ffmpeg - Qiita
  - https://qiita.com/riversun/items/d09d8e596a20ec1798f3
- 【iOS Simulator】 iPhoneシミュレータのスクリーンショットを撮る方法 | アマチュア無線局JS2IIU
  - https://js2iiu.com/2024/06/15/xcode-iphone-screenshot/

[^1]: https://qiita.com/reodon/items/fd0f0bd381ce92f1b886
[^2]: https://developer.apple.com/jp/swift/
[^3]: https://www.mathjax.org/
[^4]: https://developer.apple.com/documentation/charts
[^5]: https://developer.apple.com/documentation/accelerat
[^6]: https://docs.ruby-lang.org/ja/latest/doc/spec=2fcall.html#block

---
title: 剰余類
tags: ＃剰余類 # ガロア理論
author: katoTeru
slide: false
---
　ガロア理論の本を読むと、余りの数で分類したグループを
 「剰余類」と呼んでいる。たとえば１００を５で割ると、余りが
 １，２，３，４，０（５で割り切れる）の５つのグループに分かれる。
 今回は、この「剰余類」を取りあげ、「群論」の話に触れる。

●１．素数は貴重！素数２，３，５だけ取り上げる話をする。
６を因数分解すると、
　　1, 2, 3, 4, 6
が因子になる。この中で、６と最小公倍数が同じもの、つまり
２と３と６を除くと、１と５だけが残る。この１と５を「既約剰余類」と呼ぶ。
つまり、「素数」と１だけ残る。（１は約数が１つなので、素数ではない。）

それに対して、５を因数分解すると、
　　1, 5
になる。「素数」と１だけになる。なぜかというと、５が「素数」だからだ！

素数のすごさが分かる。

●２．既約剰余類
この商の６や５をｎと置く。
ｎと互いに素であるものを選び、群にする
（Ｚ／ｎＺ）＊
この＊は、因数が入ってないことを意味する。
ｎに６を入れると、１と６だけ（「既約剰余類」だけ）選んでくれる。
（２，３，４は＊マークが、省いてくれる。）

剰余類には、割り切れる、つまり余り０のグループがある。しかし、０のグループは
省きたいので、以下の表現をする。
　　Ｚ/5Z-{0}

「演算表」に、＋に関して、または×に関してを左上に表記する。
「演算表」で、行（縦）と列（横）の交差するところに、１で割り切れるグループを探す。この行と列のお互いを、「逆行列」の関係という。例えば、５で割った余りが２のグループは、余りが４のグループの逆元である。

●３　互いに素
　kx+ny=1
の例題を説く。高校の数学Ｂの問題。
この問題は、「剰余類」の「逆元」と関連する良問である。解き方は割愛する。

●４　（Ｚ／ｎＺ）＊　は巡回群である。

巡回群は、ｎが素数だとありがたい。

(Z/pz)*は、位数p-1の巡回群に同型である。
(Z/pZ)* と Z/(p-1)Z　は同型である。

この同型を探す数学が、「群論」である。
たとえば、カレンダーは７日すると、また日曜日になります。
この「同型」は、３６５を７で割った余りのグループ（これが曜日になっている）
ですね。一見違うものをじっくりみて、同じ性質を探すのが、群論です。
その手掛かりが、ｎで割った余りのグループに着目して、そのｎが素数だといろいろありがたいことが起きるのです！

参考文献）
「ガロア理論の頂を踏む」
石井敏全　著　ベレ出版
Ｐ．３３からＰ．８６

---
title: 原始根を求めるCプログラム
tags: 原始根 ガロア理論 C
author: embittt
slide: false
---
2024年の10月から秋葉原ロボット部の「ガロア理論の頂を踏む」読書会に参加していますが、1章9節に原始根という言葉が出てきました。

定義は、既約剰余類群(Z/pZ)*[^1]の元であってそのべき乗を計算すると全ての(Z/pZ)*の元を表せるもの[^2]、です。

また1章10節によるとpが素数ならば原始根は必ず存在します。原始根を探すアルゴリズムも載っているのですが少々複雑なので、単純に定義に基づいてpに対する原始根を全て求めるプログラムをC言語で作ってみました。

```C
#include <stdio.h>

// nがpの原始根であるか判定
int isPrimitiveRoot(int p, int n)
{
	int count = 0;
	long long m = 1; // intだと溢れた
	char already[110000] = {0}; // 10000個目の素数は104729

	while (1) {
		m *= n; // mにnのべき乗が入る
		m %= p; // 溢れないよう即mod p
		count++;

		//if (m != 1) // pが素数なら原始根でなくても必ず1に到達する前提のコード←NG
		if (already[m] == 0) { // pが素数でなくても無限ループにならないようにするため
			already[m] = 1;
			continue;
		}

		if (m != n) // pが素数なら起きないみたいだが、素数でないと起きる場合があった
			printf("%d %d\n", m, n);
		//if (count == p - 1) // pが素数なら原始根でなくても必ず1に到達する前提のコード←NG
		if (count == p)
			return 1;
		else
			return 0;
	}
}

int main(void)
{
	int p;

	printf("prime number: ");
	scanf("%d", &p);

	int count = 0;
	for (int i = 2; i < p; i++)
		if (isPrimitiveRoot(p, i)) {
			printf("%d ", i);
			count++;
			count %= 10;
			if (count == 0)
				printf("\n");
		}
	printf("\n");

	return 0;
}
```

本に載っていた41の原始根を求めてみた例です。
```
prime number: 41
6 7 11 12 13 15 17 19 22 24
26 28 29 30 34 35
```
グロタンディーク素数には原始根はありませんでした。:-)
```
prime number: 57

```

このプログラムは、入力されたpに対し2からp-1の数が原始根であるかをisPrimitiveRoot関数で判定し、原始根であれば表示しています。

pが素数でない場合にも原始根がありうるのか(いくつか調べた感じではなさそうですが)、あったとして数学的に使い道があるのかは分かりませんが、一応素数でないpを入力されても無限ループに陥らないためにnのべき乗を計算していて既に出現した値が再び出現したかをチェックするようにしました。

ネットで原始根をある程度まで求めた情報が載っていましたが、それとは一致していました。またネットで素数表を探したところ10000個目の素数は104729ですが無限ループに陥ることなく終了できました。

抽象的な議論だけだとどこかもやもやするので具体的に原始根の値を計算してみたお話でした。

[^1]:整数をpで割った余りは0、1、、p-1のp通りなので、整数を余りによってp個に分類でき($0$、$1$、$2$、、$p-1$と表し数のように扱う)、これらの集合をZ/pZと表します。Z/pZは足し算に関して群を成します。
Z/pZの元からpと互いに素であるものだけを選ぶと掛け算に関して群を成し既約剰余類群と呼び(Z/pZ)*と表します。

[^2]:具体例として(Z/5Z)*の元は$1$、$2$、$3$、$4$の4個ですがどれが原始根か定義に従って確認してみます。各元をべき乗して5で割った余りを求めると、
$1$は何乗しても$1$以外の元が出てこないので$1$は原始根ではありません。
$2^1=2$、$2^2=4$、$2^3=8=3$、$2^4=16=1$ と全ての元が出てきたので$2$は原始根です。
$3^1=3$、$3^2=9=4$、$3^3=27=2$、$3^4=81=1$ と全ての元が出てきたので$3$は原始根です。
$4^1=4$、$4^2=16=1$、$4^3=64=4$、$4^4=256=1$ となり$4$と$1$しか出てこないので$4$は原始根ではありません。


---
title: ディフィー・ヘルマン鍵共有 (Diffie-Hellman Key Exchange) の群論による説明
tags: #math #暗号 #internet
author: kau
slide: false
---
## 群論的基礎

ディフィー・ヘルマン鍵共有は群論の枠組みで説明すると、以下の要素を利用します。

### 1. 有限巡回群 \( G \)
- 群 \( G \) は有限集合であり、乗法演算に関して閉じています。
- 特に、群 \( G \) は素数 \( p \) を法とする既約剰余類群 
$$
(\mathbb{Z}/p\mathbb{Z})^*
$$

で構成されます。
- \( G \) の元に対する群演算は「乗法」とし、元の逆元も存在します。

### 2. 生成元 \( g \)
- \( g \in G \) は \( G \) の生成元（巡回群の構造をもつ）で、以下の性質を満たします：
  $$
  [
  G = \{ g^0, g^1, g^2, \dots, g^{|G|-1} \} \mod p
  ]
  $$
 $$ ここで ( |G| = p-1 ) は群の位数です。$$

### 3. 離散対数問題
- $( g^x \mod p )$ を計算することは効率的に可能ですが、逆に $( g^x \mod p )$ が与えられたときに $( x )$ を見つけるのは計算量的に困難です。これがアルゴリズムの安全性を支える鍵となります。

---

## アルゴリズムの詳細

### 1. 公開された群と生成元の設定
大きな素数pとGの生成元gを準備します。

### 2. 秘密値の選択
- **アリス**はランダムな整数aを選びます。
- **ボブ**はランダムな整数bを選びます。

### 3. 公開値の計算
- アリスは $( A = g^a \mod p )$ を計算し、ボブに送信します。
- ボブは $( B = g^b \mod p )$ を計算し、アリスに送信します。

### 4. 共通鍵の計算
- アリスはボブから受け取ったBを用いて次を計算します：
  $$[
  K_{\text{Alice}} = B^a \mod p = (g^b)^a \mod p
  ] $$
- ボブはアリスから受け取った \( A \) を用いて次を計算します：
  $$[
  K_{\text{Bob}} = A^b \mod p = (g^a)^b \mod p
  ]$$

群論におけるべき乗の結合法則により、次が成立します：
$$[
K_{\text{Alice}} = K_{\text{Bob}} = g^{ab} \mod p
]$$

---

## 具体例: 実際の計算

以下の値を使用します：
- $$( p = 23 ): 群の法（素数）$$
- $$( g = 5 ): 群の生成元$$
- $$アリスの秘密値 ( a = 6 )、ボブの秘密値 ( b = 15 )$$

### 手順

1. **アリスの公開値**:
  $$ [
   A = g^a \mod p = 5^6 \mod 23 = 15625 \mod 23 = 8
   ] $$

2. **ボブの公開値**:
  $$ [
   B = g^b \mod p = 5^{15} \mod 23 = 30517578125 \mod 23 = 19
   ]$$

3. **共通鍵の計算**:
   - アリス側：
    $$ [
     K_{\text{Alice}} = B^a \mod p = 19^6 \mod 23 = 47045881 \mod 23 = 2
     ]$$
   - ボブ側：
     $$[
     K_{\text{Bob}} = A^b \mod p = 8^{15} \mod 23 = 35184372088832 \mod 23 = 2
     ]$$

$したがって、アリスとボブは共通鍵 ( K = 2 ) を共有します。$

---

## 安全性の理論

- **離散対数問題の難しさ**:
  $( g^a \mod p ) と ( g^b \mod p ) を観測しても、$
  $秘密値 ( a ) または ( b ) を特定するのは現実的に難しいです。$

- **Diffie-Hellman問題の困難性**:
  $( g^a \mod p ) と ( g^b \mod p ) を知っていても、$
  $直接 ( g^{ab} \mod p ) を計算するのは困難です。$

---

---
title: 妖怪クリストッフェルと仲良くなれないかな・・
tags: 相対性理論 多様体 微分幾何
author: osawat
slide: false
---
# はじめに

『秋葉原ロボット部 理論グループ Advent Calendar 2024』の投稿です
線形代数が大好きからはじまり、『一般相対性理論を一歩一歩数式で理解する』読書会で何とか理解したいと、日々楽しく追い詰められています

<img src="https://m.media-amazon.com/images/I/61QAwiBMpbL._SL1068_.jpg" width=10%>

自分にとって一番ショックが大きかった接続係数 クリストッフェル記号について記事にしました、直感的に理解できればと思い自分のための復習的に書いています、敷居の高さで恨みを込めて"妖怪"と書いてしまいましたが、理解とともに友達になれてきた気がします、実はとてもよいやつだと思います（多分）

**ここからの話は、$\mathbb{R}^2$つまり、２次元平面での話です、$\mathbb{R}^3$ではありません**
直線座標としていますが、ここからの話は、**標準基底**としています

# 直線座標と曲線座標

## 座標について

通常、座標を表現するために、基底の線形結合を用います、座標 $(2,3)$というときには、$2 \vec{e_1} + 3 \vec{e_2}$、つまり、$x$方向に大きさ1のベクトルの２倍と$y$方向に大きさ1のベクトルの３倍を足したものと考えます、この標準基底をみんなで共有しているので、誰でも$(2,3)$の位置情報を共有できるわけです、つまり、基底が決まらなければみんなと同じ議論ができないことになります
それで、ここでの話は、この基底が曲線の場合にどうすんのって話です

- 直線座標 : $\vec{x}=(x_1, x_2)$
- 曲線座標 : $\vec{x}=(x_1(u_1, u_2), x_2(u_1, u_2))$

この座標の基底について議論を進めます

<img src=https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/71601/e7a044df-5367-d8d3-2494-4ffc676fbb07.png width=70%>

## 直線座標の基底
- 直線座標の基底は、馴染みのある標準基底 ${ \vec{e_1}, \vec{e_2} }$です（としています）
- 曲線座標と同様に、接ベクトルを考えれば、偏微分したものは、位置$(x_1, x_2)$に依存しない定ベクトルとなります（曲線座標と比べてみてください）
$$
\begin{array}{l}
\cdot \ \  \frac{\partial \vec{x}}{\partial x_1} = \frac{\partial}{\partial x_1} \left( x_1 \vec{e_1} + x_2 \vec{e_2} \right) = \vec{e_1} \\\\
\cdot \ \  \frac{\partial \vec{x}}{\partial x_2} = \frac{\partial}{\partial x_2} \left( x_1 \vec{e_1} + x_2 \vec{e_2} \right) = \vec{e_2}
\end{array}
$$

- 直線座標をまとめると
    - 直線基底は２次元平面上のどこにあっても同じ定ベクトル
    - 直線基底は、$\vec{x}$ の位置に依存しない、位置の関数とならない
    - 直線基底は、グローバルは基底と言えます

<hr>

## 曲線座標の基底
- 曲線座標の基底は、空間全体で定ベクトルとなるような具合のよい基底はありません
- 全体ではなく、各点においての接ベクトルを基底とすることで対応します（$(u_1, u_2)$の関数とはなりますが、基底がなければ始まりません）
- 局所的に採用される基底です

$$
\begin{aligned}
\cdot \ \ \frac{\partial \vec{x}}{\partial u_1} \\\\
\cdot \ \ \frac{\partial \vec{x}}{\partial u_2}
\end{aligned}
$$

- 曲線座標をまとめると
    - 曲線座標の基底は２次元平面全体ではなく、**各点においての基底**です
    - 曲線座標の基底は、$\vec{x}$ の位置に依存し、位置$(u_1, u_2)$の関数となります
    - 曲線座標の基底は、ローカルな基底と言えます（局所的）

# 曲線座標を議論するための仕掛け

曲線座標を議論するための仕掛けは、**媒介変数**です、媒介変数表示することで、合成関数の微分が利用できるようになります

- $x_1 = x_1(u_1, u_2)$
- $x_2 = x_2(u_1, u_2)$

この辺は、$(u_1, u_2)$から $(x_1, x_2)$の写像があり、しかも微分可能とか・・・深い話があるようですが

$$
\begin{array}{ccc}
\mathbb{R}^2 & \longrightarrow & \mathbb{R}^2 \\\\
(u_1, u_2) & \longmapsto & (x_1(u_1, u_2), x_2(u_1, u_2))
\end{array}
$$

- 直線座標 : $\vec{x}=(x_1, x_2)$
- 曲線座標 : $\vec{x}=(x_1(u_1, u_2), x_2(u_1, u_2))$


## 曲線の基底の変化率

曲線の基底は、各点ごとの値なので場所がずれるとどのようになっているのかを考える必要がありそうです
こう考えると、空間の曲がり具合を考えるために、基底の微分考えればよいように思えます
ということで、基底の変化率、つまり$u_1$,$u_2$での偏微分を考えると以下のようになります

$$
$$

$$
\begin{aligned}
\cdot \ \ \frac{\partial \vec{x}}{\partial u_1} &\overset{u_1で微分}\longrightarrow \frac{\partial}{\partial u_1} \left( \frac{\partial \vec{x}}{\partial u_1} \right) = \frac{\partial^2 \vec{x}}{\partial u_1 \partial u_1} \\\\
&\overset{u_2で微分}\longrightarrow \frac{\partial}{\partial u_2} \left( \frac{\partial \vec{x}}{\partial u_1} \right) = \frac{\partial^2 \vec{x}}{\partial u_2 \partial u_1} \\\\
\cdot \ \ \frac{\partial \vec{x}}{\partial u_2} &\overset{u_1で微分}\longrightarrow \frac{\partial}{\partial u_1} \left( \frac{\partial \vec{x}}{\partial u_2} \right) = \frac{\partial^2 \vec{x}}{\partial u_1 \partial u_2} \\\\
&\overset{u_2で微分}\longrightarrow \frac{\partial}{\partial u_2} \left( \frac{\partial \vec{x}}{\partial u_2} \right) = \frac{\partial^2 \vec{x}}{\partial u_2 \partial u_2} \\\\
\end{aligned}
$$

曲線の基底の変化率は:
- ベクトルの2階微分の形をしています
    - 接ベクトルを基底としているので、その微分といことで、当然ですが
    - 見た目ば、一挙におどろおどろしくなり、逃げたくなりますね
- これらも同じ$\mathbb{R}^2$の平面上のベクトルでなので、基底$\\{ \frac{\partial \vec{x}}{\partial u_1} , \frac{\partial \vec{x}}{\partial u_2} \\}$の線形結合の形で表すことができます
    - 例えば、$\vec{x}=a_1 \vec{e}_1 + a_2 \vec{e}_2$のように
    - 曲線座標の基底は$\frac{\partial \vec{x}}{\partial u_1},\frac{\partial \vec{x}}{\partial u_2}$なので、
    - こんな感じ$a_1\frac{\partial \vec{x}}{\partial u_1} + a_2\frac{\partial \vec{x}}{\partial u_2}$ですね
    - 基底が一式あれば、空間全体を表現できます（雑な表現ですが）

## 基底の変化率の係数

曲線の基底の変化率は4種類ありました
それぞれを曲線の基底の線形結合であわらすと以下です

出ました！、**妖怪クリストッフェル**、この子は、線形結合での基底の**係数**だった！？
おどろおどろしい風貌ですが、簡単なルールで添え字が振られています
- 左辺の2階偏微分の$u$の添え字が、右辺の$\Gamma$の下付き添え字と一致します
- 右辺の曲線の基底で$u$の添え字が、$\Gamma$の上付き添え字と一致します

$$
\begin{aligned}
\frac{\partial^2 \vec{x}}{\partial u^{1} \partial u^{1}} = 
\Gamma^1_{{11}} \frac{\partial \vec{x}}{\partial u^1}+\Gamma^2_{{11}} \frac{\partial \vec{x}}{\partial u^2} \ (1) \\\\
\frac{\partial^2 \vec{x}}{\partial u^{1} \partial u^{2}} = 
\Gamma^1_{{12}} \frac{\partial \vec{x}}{\partial u^1}+\Gamma^2_{{12}} \frac{\partial \vec{x}}{\partial u^2} \ (2) \\\\
\frac{\partial^2 \vec{x}}{\partial u^{2} \partial u^{1}} = 
\Gamma^1_{{21}} \frac{\partial \vec{x}}{\partial u^1}+\Gamma^2_{{21}} \frac{\partial \vec{x}}{\partial u^2} \ (3) \\\\
\frac{\partial^2 \vec{x}}{\partial u^{2} \partial u^{2}} = 
\Gamma^1_{{22}} \frac{\partial \vec{x}}{\partial u^1}+\Gamma^2_{{22}} \frac{\partial \vec{x}}{\partial u^2} \ (4) \\\\
\end{aligned}
$$

これらの右辺は、以下のように解釈できます

- 基底$\frac{\partial \vec{x}}{\partial u^1}$の
    - $u^1$方向の変化率 (1)式
    - $u^2$方向の変化率 (2)式
- 基底$\frac{\partial \vec{x}}{\partial u^2}$の
    - $u^1$方向の変化率 (3)式
    - $u^2$方向の変化率 (4)式

## 接続係数

$\Gamma$は、"接続係数"の名前がありますが、
- "接続"の部分の詳細は不明ですが、
- "係数"の部分はまさに、係数そのもの

右辺を見ると、単に２階の偏微分なので以下の性質があります
$$
\frac{\partial^2 \vec{x}}{\partial u^{1} \partial u^{2}} = \frac{\partial^2 \vec{x}}{\partial u^{2} \partial u^{1}} 
$$

$$
\Gamma^1_{{12}} =\Gamma^1_{{21}} \ (接続係数の対称性)
$$

また、接続係数は定数ではなく、曲線の基底がそうであったように、やはり関数です
$$
\Gamma^i_{jk}(u_1, u_2)
$$

行列で表すと以下

$$
\begin{aligned}
\begin{bmatrix} 
\frac{\partial^2 \vec{x}}{\partial u^1 \partial u^1} \\\\
\frac{\partial^2 \vec{x}}{\partial u^1 \partial u^2} \\\\
\frac{\partial^2 \vec{x}}{\partial u^2 \partial u^1} \\\\
\frac{\partial^2 \vec{x}}{\partial u^2 \partial u^2} 
\end{bmatrix}=
\begin{bmatrix} 
\Gamma^1_{11} & \Gamma^2_{11} \\\\
\Gamma^1_{12} & \Gamma^2_{12} \\\\
\Gamma^1_{21} & \Gamma^2_{21} \\\\
\Gamma^1_{22} & \Gamma^2_{22} \\\\
\end{bmatrix}\begin{bmatrix} 
\frac{\partial \vec{x}}{\partial u^1} \\\\
\frac{\partial \vec{x}}{\partial u^2} \\\\
\end{bmatrix}
\end{aligned}
$$


アインシュタインの縮約記法を使うと以下
書籍(p431)では「この係数$\Gamma^i_{jk}$を$(x^1, x^2)$でみた$(u^1, u^2)$の接続係数といいます」とされています

$$
\begin{aligned}
\frac{\partial^2 \vec{x}}{\partial x^j \partial x^k}
&= \Gamma^i_{jk} \frac{\partial \vec{x}}{\partial x^i} \\\\
\end{aligned}
$$

ベクトル表示から成分表記にすると

$$
\begin{aligned}
\vec{x}
&=\begin{bmatrix} x^1 \\\\ x^2 \end{bmatrix}   \\\\
\frac{\partial^2 x^1}{\partial x^j \partial x^k} 
&= \Gamma^i_{jk} \frac{\partial x^1}{\partial x^i} \\\\
\frac{\partial^2 x^2}{\partial x^j \partial x^k} 
&= \Gamma^i_{jk} \frac{\partial x^2}{\partial x^i} \\\\
\end{aligned}
$$

妖怪クリストフェルが、ちょっと可愛く思えてきませんか

# 後記

コメントや誤りの指摘などありましたら、大歓迎です、大らかな気持ちで、お願いいたします


---
title: 一次元人の世界を理解するための接続係数の使い方を妄想してみた 
tags: 相対性理論
author: kazueda
slide: false
---
## はじめに 

勉強会で採用しているテキストの「一般相対性理論を一歩一歩数式で理解」の第5章「曲線座標のテンソル場」§4「曲線座標の接続係数」では、接続係数という考え方が導入されます。接続係数の概念をつかむのに苦労しましたので、一次元座標での座標変換を例に、接続係数の役割を妄想してみました。一次元の座標では、ベクトルが移動する際はすべて平行移動になります。 
## 直線座標の一次元人のベクトル移動 
　まずは、直線座標の一次元人の世界（以降、直線世界）の例です。 
　直線座標の一次元人は、我々の世界の$xy$平面と原点を共有し、$x$軸に平行な直線上で生活をしているとします。全ての*xy*平面の座標を一次元人の座標で表すことはできませんので、$xy$平面内の$y$ = 0上の座標に限定して、座標変換を行います。 
　我々の世界の基底ベクトルを$e_x$と$e_y$とし、一次元世界の基底ベクトルを$e_p$とします。さらに、我々が理解しやすいように、ある座標での基底ベクトルに対する法線ベクトルを$e_q$とします。ただし、$e_q$は一次元人には認識できません。直線世界を我々が理解するために導入したものです。 
　あるベクトル$x$ = ($x$, $y$) = ($p$, $q$)（ただし、$q$ = 0に限定）とおくと、 
$$ 
e_p=\frac{\partial\symbfit{x}}{\partial p}=\left(\begin{matrix}1\\0\\\end{matrix}\right),\ \ e_q=\frac{\partial\symbfit{x}}{\partial q}=\left(\begin{matrix}0\\1\\\end{matrix}\right)
$$

が成り立ちます。さらに微分を行い、それを1階微分と接続係数で表すと、 
$$
\frac{\partial^2\symbfit{x}}{\partial p\partial p}=\left(\begin{matrix}0\\0\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial p}+0\frac{\partial\symbfit{x}}{\partial q}=0e_p+0e_q,\ \ \Gamma_{\ \ \ pp}^p=0,\ \ \Gamma_{\ \ \ \ pp}^q=0
$$
$$
\frac{\partial^2\symbfit{x}}{\partial p\partial q}=\left(\begin{matrix}0\\0\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial p}+0\frac{\partial\symbfit{x}}{\partial q}=0e_p+0e_q,\ \ \Gamma_{\ \ \ pq}^p=0,\ \Gamma_{\ \ \ \ pq}^q=0
$$
$$
\frac{\partial^2\symbfit{x}}{\partial q\partial q}=\left(\begin{matrix}0\\0\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial p}+0\frac{\partial\symbfit{x}}{\partial q}=0e_p+0e_q,\ \ \Gamma_{\ \ \ qq}^p=0,\ \Gamma_{\ \ \ \ qq}^q=0
$$
が成り立ちます。$q$ = 0の限定条件があっても、同様の式です。変数$p$のみが変化する一元ですので、以下の式のことのみを考えます。 
$$
\frac{\partial^2\symbfit{x}}{\partial p\partial p}=\left(\begin{matrix}0\\0\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial p}+0\frac{\partial\symbfit{x}}{\partial q}=0e_p+0e_q,\ \ \Gamma_{\ \ \ pp}^p=0,\ \ \Gamma_{\ \ \ \ pp}^q=0
$$
我々が直線世界を理解するために導入した法線ベクトルを使わなくても、$y$ = 0上での移動の際の基底ベクトルの変化を表すことができます。この場合、直線世界の任意の座標($p$, 0)への基底$e_p$の平行移動は$xy$座標でのベクトルの平行移動と一致することを意味します。 
## 曲線座標の一次元人のベクトル移動 

次に、曲線座標に住む一次元人の世界（以降、曲線世界）の例をみてみます。 

先ほどと同様、$xy$平面のすべての座標を一次元の曲線世界に表すことができません。ここでは、直交座標の$x^2 + y^2 = 1$上の座標を極座標に変換する世界を曲線世界とします。これは、極座標での$r = 1$に限定した座標を意味します。 

$x_r = (x, y) = (rcosθ, rsinθ)$　（ただし、$r = 1$）とおくと、 
$$
\frac{\partial\symbfit{x}}{\partial\theta}=\left(\begin{matrix}-rsin\theta\\rcos\vartheta\\\end{matrix}\right),\ \ \frac{\partial\symbfit{x}}{\partial r}=\left(\begin{matrix}cos\theta\\sin\vartheta\\\end{matrix}\right)
$$
となります。$∂x/∂θ$は曲線世界の基底ベクトル、$∂x/∂r$は我々が曲線世界を理解するために導入した法線ベクトルです。$θ$と$r$でさらに微分すると 
$$
\frac{\partial^2\symbfit{x}}{\partial\theta\partial\theta}=\left(\begin{matrix}-rcos\theta\\-rsin\theta\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial\theta}-r\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ \theta\theta}^\theta=0,\ \ \Gamma_{\ \ \ \theta\theta}^r=-r
$$
$$
\frac{\partial^2\symbfit{x}}{\partial\theta\partial r}=\left(\begin{matrix}-sin\theta\\cos\theta\\\end{matrix}\right)=\frac{1}{r}\frac{\partial\symbfit{x}}{\partial\theta}+0\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ \theta r}^\theta=\frac{1}{r},\ \ \Gamma_{\ \ \ \ \theta r}^r=0
$$
$$
\frac{\partial^2\symbfit{x}}{\partial r\partial r}=\left(\begin{matrix}0\\0\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial\theta}+0\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ rr}^\theta=0,\ \ \Gamma_{\ \ \ rr}^r=0
$$
となり、$r = 1$で固定なので、 
$$
\frac{\partial^2\symbfit{x}}{\partial\theta\partial\theta}=\left(\begin{matrix}-cos\theta\\-sin\theta\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial\theta}-\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ \theta\theta}^\theta=0,\ \ \Gamma_{\ \ \ \theta\theta}^r=-1
$$

$$
\frac{\partial^2\symbfit{x}}{\partial\theta\partial r}=\left(\begin{matrix}-sin\theta\\cos\theta\\\end{matrix}\right)=\frac{\partial\symbfit{x}}{\partial\theta}+0\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ \theta r}^\theta=1,\ \ \Gamma_{\ \ \ \ \theta r}^r=0
$$

$$
\frac{\partial^2\symbfit{x}}{\partial r\partial r}=\left(\begin{matrix}0\\0\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial\theta}+0\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ rr}^\theta=0,\ \ \Gamma_{\ \ \ rr}^r=0
$$

さらに、$θ$のみが変化しますので、以下の式のことのみを考えます。 

$$
\frac{\partial^2\symbfit{x}}{\partial\theta\partial\theta}=\left(\begin{matrix}-cos\theta\\-sin\theta\\\end{matrix}\right)=0\frac{\partial\symbfit{x}}{\partial\theta}-\frac{\partial\symbfit{x}}{\partial r},\ \ \Gamma_{\ \ \ \theta\theta}^\theta=0,\ \ \Gamma_{\ \ \ \theta\theta}^r=-1
$$

$r = 1$で制限した極座標上での移動の際の基底ベクトルの変化を表す
$∂^2x/∂θ∂θ$を見ると、基底ベクトルの軸上の移動を考える場合、我々が、曲線世界を理解するために導入した法線ベクトル$∂x/∂r$を考慮しなければいけないことがわかります。さらに、次の節で示すように、曲線世界の任意の座標$(sinθ, cosθ)$への基底$∂x/∂θ$の移動は$xy$座標でのベクトルの平行移動と一致しないことがわかります。$xy$座標での平行移動を優先すると終点でベクトルの向きの変化を必要とします。 
## 曲線世界での最短距離の考え方 

我々が観測すると、曲線世界をベクトルが移動する際、我々が導入した法線ベクトルの向きが変化します。曲線世界のベクトルは平行移動しかないので、我々の観測事実と一致しません。例えば、以下のルートでベクトルの平行移動を行う場合、始点Aと終点Bでの基底ベクトルは曲線世界のものが使えますが、その途中は、我々の$xy$平面での基底ベクトルで表現される平行移動となります。 
![平行移動_400.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/693019/85a1d868-9f51-926e-d680-10518584c7a1.png)
従って、終点でベクトルの向きを一致する必要があり、回転操作をすることで、一次元人の世界のベクトルと一致します。 
![回転_400.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/693019/022d1ac8-eb16-ce16-7253-a3ca0c62dbcd.png)
一次元人には、点A上のベクトルが消えたと思ったら、突然、点Bに表れたように感じるのかもしれません。 

回転操作を伴うベクトルの変化が曲線世界に及ぼす影響は予測できませんが、仮に曲線世界の宇宙が存在していると仮定したら、ベクトルの向きの変化は概念として存在しないので、回転操作によって、宇宙が崩壊するのでしょうか。 

宇宙の崩壊を避けるためには、移動の際に曲線世界とxy座標でベクトルの向きが変化しない経路を使って必要があります。 

一次元世界の観察者からみて、曲線世界のベクトルの向きや法線ベクトルの向きが変化せずに移動するためには、曲線上の無限に小さい距離の移動を積み重ねる必要があります。つまり、円弧上での経路積分です。 

こう考えると、曲線世界でのベクトルの最短距離での移動の理解の助けになるかもしれません。 

## おわりに 

1次元世界の接続係数を妄想してみました。接続係数の有無で、$xy$座標の概念と曲線世界の概念の一致の有無を判定しました。 

接続係数は係数なので、その数値の意味が重要になりますが、まだ、数値の意味を理解していません。共変微分の意味を理解する必要があるのでしょう。 

それから、本稿を記述する際に、頭の片隅には、ハル・クレメント著「重力への挑戦」の設定がありました。また、曲線世界で最短距離を考える際の宇宙の崩壊を記述の際は、エドモンド・ハミルトン著「フェッセンデンの宇宙」を思い出しました。本稿はSFですので、物理学的に正しい場合がありますが、物語として楽しんでいただけたらと思います。 

 

## 参考文献 
ハル・クレメント著「重力への挑戦」 
エドモンド・ハミルトン著「フェッセンデンの宇宙」 
