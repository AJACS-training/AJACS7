# 「自然言語処理技術の活用実例」 [#def3411a]

# 一応、自己紹介 [#j43e7643]
- 前置き
- 副題：東工大生のキャリアパス
## 略歴 [#zaf1a2c8]
### 東工大 生命理工の卒業生です。（wet時代） [#w6dda962]
- 生体機構学科（現：生命科学科）
- → 生体システム専攻
### 広瀬研究室でした [#g4268d8c]
- 卒研のテーマ：恐山ウグイにおける酸性適応機構の解明
- 修論のテーマ：ウナギにおける硫酸トランスポーターの解析と海水適応に果たす役割
- ようするに「浸透圧調節、血圧調節、イオン濃度調節の分子生物学的なアプローチ」って感じです。
### その後 [#h543d418]
- IT系大企業のバイオインフォマティクス部門に就職（dry時代）
    -なぜ、そんなところに
        -まわりが製薬や食品に就職する中、挫折感と実験もうやりたくない、という思いから
        -でも、バイオの分野からは離れたくなかった
    -やっていたこと
        -ソフト開発：文献データから情報を抽出して、遺伝子の特徴を表示する。関連遺伝子のネットワーク表示
        -テクニカルマーケティング：上記ソフトの営業支援、今後の開発についての戦略策定
        -市場調査・情報収集：今、何が「来ている」か。今後、何が「来る」か。
- 部署のおとりつぶしに遭う（冬の時代）
    -別の部署に飛ばされる
    -バイオとはほとんど関係ないヘルスケア分野について、毎日 PowerPoint で企画書を書く日々
    -半年間 耐える
- 再び、現場へ。というか最前線（再び dry時代）
    -会社時代から、草の根コミュニティに顔を出していたので、飛ばされたところを拾ってもらう。
    -...
- そういえば学位は
    -会社時代に国内留学の形で阪大で（情報科学）
    -wet系だと、研究室にはりついて、ですが、情報系なので、パソコンがあればどこでもよく、メールベースでやりとりでOKだったので。
    -ただ、学位を取る前に会社を辞めたので、資金的な補助は打ち切り、すべて会社に返納

# 本題 [#bab330ce]
## そもそも「自然言語」とは何か? [#z7e41005]
- 英語だと "natural language" （直訳だ）
- ようするに「テキスト情報」
- きっちり目に言うと、「日常生活に用いられる言語」
    -日常生活、とは言え、今回は、研究生活ですが
- もっと平たく言うと「日本語とか英語とかの文章」
- 自然言語リソースの例
    -NCBIの
        -[[PubMed:http://www.pubmed.org]]（文献データベース・あとで触れる）
        -[[OMIM:http://www.ncbi.nlm.nih.gov/omim]]（疾患と疾患関連遺伝子のデータベース）
    -統合ホームページの
        -[[蛋白質核酸酵素 全文検索:http://lifesciencedb.jp/pne/]]
        -[[文科省「ゲノム」研究報告書 全文検索:http://lifesciencedb.jp/houkoku/]]
        -[[学会要旨統合検索:http://lifesciencedb.jp/lsdb.cgi?gg=tool_tproc]]
        -[[新聞記事検索:http://lifesciencedb.jp/mainichi/]]
    -一般的に
        -[[Wikipedia:http://en.wikipedia.org/wiki/SLC26A4]] … '''SLC26A4''' という遺伝子のエントリを例に
        -[[ブログ:http://blog.dbcls.jp/portal/]] … 統合DBプロジェクトのスタッフブログ「統合ぐらし」を例に
## なんで「自然言語」リソースに注目するのか? [#s6ab196b]
- 量：どのくらいの自然言語リソースがあるか
    -代表はMEDLINE（ようするにPubMed）
    -問：[[PubMed:http://www.pubmed.gov/]]には何件の文献がおさめられているでしょうか?
        -PubMedを "All[filter]" で検索してみる [[【参考動画】:http://togotv.dbcls.jp/20071213.html#p01]]
→ 件数は?
    -問：PubMedにはどのくらい前からの文献がおさめられているでしょうか?
        -検索した状態で "Sort by"を "Pub Date"にして、最後のページにアクセスしてみる
        -今、かなり前の文献まで収載しようとしていて、実際のは、[[PubMed Overview:http://www.ncbi.nlm.nih.gov/entrez/query/static/overview.html]]に書いてあったりします。
    -''50年以上にわたって集められた膨大な資産が自然言語という形で存在する (まさにknowledge base)''
- 質：バイオなデータにはどんなのがあるのか。他のデータベースと比較してみる
|''一般的なバイオ系DB''||''自然言語リソース''|
|Entrez gene|''DB例''|PubMed|
|配列、発現、SNP、...|''データの中身の例''|文献|
|豊富|''他のDBへのリンク''|貧弱|
|整っている|''構造''|肝心の内容は構造化されていない|
    -''文献データは、遺伝子などのデータベースと別の世界を作っている''
- 自然言語リソースを活用しよう!

## 自然言語処理とは [#wfe92190]
- 英語だと、natural language processing (NLP) と言います
- 情報処理の話なので、バイオなにおいはあまりないですが。。。
- テキストマイニング (text mining)
    -mine: 地雷、鉱山、採掘する （mine sweeper っちゅうゲームのmine）
    -テキストの山からお宝（=有用な情報）を掘り当てること
- どんなtaskが?
    -どの文字からどの文字までが遺伝子、疾患、化合物などをさしているか言い当てる（named entity recognition: NER）
    -書いてある要素（遺伝子、…）どうしの関連の抽出：up-regulate, bind, inhibit, phosphorylation, …
- 困難なところ（遺伝子を例に）
    -1つの遺伝子は、複数の名前をもっている
 SLC26A4: pendrin, PDS, pendred syndrome gene, DFNB4, solute carrier family 26 member 4
    -複数の遺伝子などで、同じ名前を共有している
 PDS: pendred syndrome gene
 PDS: prostaglandin D2 synthase
 PDS: ...
        -問：略語と長い名前のペアを検索するサービス [[Allie:http://allie.dbcls.jp/]] を使ってどんな長い名前があるか見てみよう
    -長い名前には、書き方のバリエーション（揺らぎ）がある
 例：NHE3 (PubMed を検索して最新20件についての記述の例)
 Na(+)/H(+) exchanger 3
 Na+/H+ exchanger 3
 Na(+)-H(+) exchanger NHE3
 Na/H exchanger isoform 3
 type 3 Na(+)/H(+) exchanger
 type 3 sodium hydrogen exchanger
 sodium/proton exchanger NHE3
- 結局、「自分の興味のある論文を（ノイズを減らしつつ）探しあてる」「論文に書いてある中身を理解する」という人間のやっている仕事と根源は同じ
    -ただ、大量なので、コンピューターで処理しましょう、ということ
    -いくつかの遺伝子を掘り下げる → ゲノムワイドにがっさり

## 自然言語処理の活用事例 [#u3908b3d]
- マイクロアレイなどのゲノムワイドな解析で得た遺伝子群についての生物学的な解釈
    -普通は、Gene Ontologyという語を使ったりするが、疾患、薬剤、生命現象はイマイチ
- Ingenuity Pathway Analysis
    -製品です。（学生に身分では買えないくらいの額）
    -知識のある人（学位のある人）が論文を読んで知識抽出。遺伝子のネットワークなどで表現
- [[Gendoo:http://gendoo.dbcls.jp/]] (gene, disease features ontology-based overview system)
    -遺伝子や疾患の特徴をキーワードで表す、というもの
    -データのつくりかた
        -各遺伝子（Entrez Gene）や疾患（OMIM）について、記載のある文献を取得する
        -各文献に付与されたキーワード（MeSH term）を抽出
        -スコアリング
    -例：'''APP''' (amyloid precursor protein)
        -[[Gene Ontology:http://www.ncbi.nlm.nih.gov/sites/entrez?Db=gene&Cmd=DetailsSearch&Term=351]]
|''Category''|''term''|
|Molecular Function|acetylcholine receptor binding|
||identical protein binding|
||serine-type endopeptidase inhibitor activity|
|Biological Process|cellular copper ion homeostasis|
||neuromuscular process|
|Cellular Component|Golgi apparatus|
||cell surface|
||cytoplasm|
||extracellular region|
||integral to plasma membrane|
||plasma membrane|
||platelet alpha granule lumen|
        -[[Gendoo:http://gendoo.dbcls.jp/cgi-bin/gendoo.cgi?geneid=351&taxonomy=human]] (MeSH)
|''Cateogory''|''term''|
|Disease|Alzheimer Disease|
||Cerebral Amyloid Angiopathy|
||Amyloidosis|
|Drugs|Amyloid beta-Protein Precursor|
||Amyloid beta-Protein|
||Peptide Fragments|
|Biological phenomena|Protein Binding|
||Protein Structure, Tertiary|
||Protein Structure, Secondary|
|Anatomy|Brain|
||Neurons|
||Senile Plaques|
||...|
||Chromosomes, Human, Pair 21|
    -例：[[1型糖尿病と2型糖尿病の特徴の違い:http://gendoo.dbcls.jp/cgi-bin/gendoo.cgi?taxonomy=human&omimid=222100&omimid=125853]]
#ref(nar.fig1.png)

# まとめ [#m03f76f9]
