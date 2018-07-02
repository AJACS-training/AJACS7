[[AJACS7]]

本日のプレゼンテーションスライドは後日掲載いたします。
        --
目次

#contents
        --

# プレゼンで紹介したサイトへのリンク [#x454d6ca]
- 想-IMAGENE Book Search
>http://imagine.bookmap.info/index.jsp

- clustermed
>http://clustermed.info/

- iHOP
>http://www.ihop-net.org/UniPub/iHOP/

- SAGOOL
>http://sagool.jp/

- SPYSEE
>http://spysee.jp/


#  統合ホームページの紹介 [#ba6e4dc2]
> http://lifesciencedb.jp/

統合データベースプロジェクトのサービスは上記のURLで提供しています。簡単に全体像を紹介しましょう。ではまずみなさんの手元のPCに統合ホームページを表示しましょう。

++URLを入力するのはスペルミスなどめんどうくさいので、検索を利用しましょう。みなさんのPCの検索というアイコンを押すと左側にGoogle検索の窓が出ます。

++LSDBと入力（小文字でも可）してI'm Feeling Luckyのボタンを押します。

++統合ホームページが表示されました！

## ポータルサービス [#r7f53519]
世の中にはたくさんのデータベース、ジャーナル、学会、など知っていると便利なリソースがたくさんあります。自分の専門分野のことはよく知っていても、少し離れるとなかなか見つからないものです。そういうときにはポータルサービスを利用しましょう。
+++[[生命科学データベースカタログ:http://lifesciencedb.jp/lsdb.cgi?pg=1]]
+++[[生命科学学会協会カタログ:http://lifesciencedb.jp/lsdb.cgi?gg=tool_academy]]
+++[[ゲノム・ポストゲノム主要プロジェクト一覧:http://lifesciencedb.jp/lsdb.cgi?gg=project]]
## 検索サービス DB検索と文献検索 [#y20bc65f]
世の中には様々な検索サービスがあります。統合データベースプロジェクトでは、キーワードによる検索を数種類用意しています。たくさんのデータベースを一度に検索できる横断検索や、日本語文献の検索サービス、GenBankやGEOなど巨大で複雑なデータベース検索があります。GoogleやYahooのように簡単では無いですが、今日の実習で使い方を覚えましょう。
+++[[生命科学データベース横断検索:http://lifesciencedb.jp/dbsearch/]]
+++[[DNAデータベース総覧と検索(DDBJ/EMBL/GenBank):http://lifesciencedb.jp/ddbj/]]
+++[[遺伝子発現バンク(GEO)目次:http://lifesciencedb.jp/geo/]]
## 自然言語処理によるサービス [#vf75847e]
自然言語処理とはなんぞや？ということは、午前中の佐藤先生の講義や、後の演習で紹介されますが、それを使った高度なサービスを提供しています。
+++[[OReFiL:http://orefil.dbcls.jp/]] (オンラインリソースファインダー）
+++[[Allie:http://allie.dbcls.jp/]] (略語の正式名称を検索）
## ツールやリソース [#n230bb22]
+++[[アナトモグラフィー/BodyParts3D:http://lifesciencedb.jp/ag/]] (解剖整理棚)
+++[[Wired-Marker:https://addons.mozilla.org/ja/firefox/addon/6219]] (参照情報共有ツール)
+++[[生物アイコン:http://lifesciencedb.jp/lsdb.cgi?gg=resource_icon]]
## 教材 [#icc3ce0a]
+++[[統合TV:http://togotv.dbcls.jp/]]
+++[[MotDB:http://motdb.dbcls.jp/?MotDB]]
## 基盤技術開発 [#f8cd488c]
ウェブサービス、APIを使って自分でプログラムを動かす人は必見です。世の中のデータベースをぐりぐり使いましょう。
## 参画機関の成果 [#h07df42e]
+++[[かずさアノテーション:http://a.kazusa.or.jp/]]

#  生命科学データベース横断検索の利用法 [#xbd5b6cf]


横断検索サービスは国内外の有用なデータベースや文献を一括して検索するサービスです。各データベースの情報はオリジナルのサイトにおいたまま、検索に必要な情報をクロウリングやオリジナルデータを使って作製します。いわばGoogleのような検索です。検索エンジンはHyper Estraierを使っています。このエンジンは現在mixiの検索などに使われているオープンソースのプログラムです。統合DBセンターでは約20ノードで構成されるクラスターサーバーで計算をさせています。
## 1 横断検索に収録されているデータベース [#l28fd7fb]
現在横断検索に収録されているデータの一覧は[[横断検索収録DB一覧:http://lifesciencedb.jp/dbsearch/dblist.html]]で見ることができます。それぞれのデータベースの属性にあわせて画面の左側にグループごとにわけて検索結果が表示されるようになっています。
###  1-1 日本語文献 [#j0834d51]
::[[蛋白質核酸酵素:http://www.kyoritsu-pub.co.jp/pne/]]|共立出版の生命科学の総説誌。創刊約53年の歴史を持つ。基礎的な話題を幅広くとりあげる。日本語の総説はなかなか業績にはなりにくいかもしれないが、選ばれて書けるのは誇りだし、何より他の人にわかってもらうにはやはりまずは日本語。
::[[毎日新聞:http://www.nichigai.co.jp/sales/mainichi/mainichi-series.html]]|CDによって提供される毎日新聞のテキストデータを使った過去記事の検索。オンライン上のニュースは一定時間がたつと消滅してしまうので、過去のニュースを探す時に便利。
::[[文科省「ゲノム」研究報告書:https://www.genome-sci.jp/]]|文部科学省の特定領域研究のうち「ゲノム」と呼ばれる領域の報告書を集めて検索できる。科学研究費には種別が色々あるが、重点的な課題はこのように大きなグループで進められる。つまり重要な成果が報告書にはたくさん記載されていると思われるので、それらを集めて一括して検索できるようにするのが目標。
###  1-2 特許 [#td98c118]
::日本特許　公開特許広報,公表特許広報など | 特許権が認められた発明のデータ、申請されて一定期間後に公開された特許の申請データ
::米国特許（外部情報）|アメリカの特許。機械的な大量ダウンロードは禁止されているので検索は米国特許庁のシステムに質問を投げている。
::欧州特許 (外部情報）|ヨーロッパの特許。米国特許と同様。
###  1-3 用語解説 [#c31c587f]
::[[ウィキペディア:http://ja.wikipedia.org/wiki/]]|オンライン百科事典。英語版が中心だが全部で264言語ある。英語版には250万の記事、日本語版にも50万近い記事がある。誰もが自由に編集に参加できる。最初は記述の正確性に欠けるのではと言われていたが、ネイチャーにブリタニカ百科事典と比較しても劣らないという調査結果が報告されたりした。
###  1-3 基本のデータベース [#iafff6d5]
::[[KEGG:http://www.kegg.jp/ja/]]|Kyoto Encyclopedia of Genes and Genomesの略。生命システム情報統合データベース。京大化学研究所および東大医科研の金久研究室によって構築されている世界的に有名なデータベース。遺伝子配列を中心に論文から関連する記述を抽出しパスウェイやリンクとして再構築し知識として体系づける。統合データベースプロジェクトでは後述する医薬に関する薬や化合物の統合を担っている。
::[[PDBj:http://www.pdbj.org/index_j.html]]|Protein Data Bank Japan の略。生体高分子の立体構造データベースの日本アーカイブ。国内の登録を受け付けるとともに、日本語のドキュメントも整理されている。今年、登録された立体構造が５万を超えた。
::[[RefSeq:http://www.ncbi.nlm.nih.gov/RefSeq/]]|Reference Sequenceから命名された。GenＢankへの登録数が増えredundancyが問題になってきたため、重複の無い基準となる配列のコレクションを作った。現在リリース２９で５千以上の生物種にわたって５００万以上の蛋白質がコレクションされている。
::[[OMIM:http://www.ncbi.nlm.nih.gov/omim/]]|Online Mendelian Inheritance in Manの略。ヒトの遺伝子と遺伝病のカタログ。
###  1-4 生物種ごとのデータベース [#n10c4362]
+ヒト、動物
::[[H-Inv:http://www.jbirc.jbic.or.jp/hinv/ahg-db/index.jsp]]|ヒト遺伝子アノテーションデータベース。ヒトの遺伝子と転写産物を対象とした統合データベース。ヒトゲノム上の遺伝子に対してcDNAを基準にして様々な情報を注釈付けするプロジェクト。産業技術総合研究所。
::[[JSNP:http://snp.ims.u-tokyo.ac.jp/index_ja.html]]|日本の一塩基多型(SNPs)のデータベース。理化学研究所と東大医科研によりミレニアムプロジェクトやオーダーメイド医療実現化プロジェクトで測定されたデータが中心。最近はDNAチップにより解析されている。データそのものはA, G, C, T の塩基の情報だが、正しく理解するには遺伝学の知識も必要。
::[[DBTSS:http://dbtss.hgc.jp/]]|転写開始点及びプロモーター領域に関するデータベース。完全長cDNA配列の5'末端の情報が中心。現在では次世代シーケンサーも利用されている。東大医科研。
::[[HUGE:http://www.kazusa.or.jp/huge/index.html]]|ヒト長鎖 cDNA (KIAA cDNA) 解析情報データベース。かずさDNA研究所。
::[[NEDO:http://www.kazusa.or.jp/NEDO/index.html]]|ヒト長鎖 cDNA (FLJ cDNA) 解析情報データベース。かずさDNA研究所。
::BodyＭap|ヒトの臓器ごとの遺伝子発現を観測したデータベース。ESTという短い遺伝子配列の解読法を生み出した。現在実験データの追加はされていないが、発現データの統合データベースとして更新されいてる。
::[[FANTOM:http://fantom.gsc.riken.go.jp/index.html]]|Functional Annotation of the mouseの略。マウス遺伝子の機能情報に関するデータベースで現在のバージョンはFANTOM3。FANTOM1および2はcDNAの機能に関する注釈が中心であったが、現在ではCAGEのデータが公開されており、RNA mappingのデータとしても利用価値が高い。京大の山中教授が万能細胞を作るときに参考にしたデータベースとして話題になった。
+植物
::[[CLOVER:http://clovergarden.jp/]]|クローバーとマメ科植物を対象とした、ゲノム情報とゲノム研究用リソースのデータベース。かずさDNA研究所。
::[[RAPDB:http://rapdb.dna.affrc.go.jp/]]|Rice Annotation Project Databaseの略。イネゲノム上の全遺伝子の構造と機能の人手によるアノテーション。農業生物資源研究所。
::RPSD|イネ、トウモロコシ、小麦等の植物のタンパク質構造データベース
+微生物
::[[CYANOBASE:http://bacteria.kazusa.or.jp/cyanobase/]]|シアノバクテリア（藍藻）ゲノムデータベース。（午前中の講義で紹介がありました。）
::RHIZOBASE|根粒菌のゲノムデータベース。かずさDNA研究所。
::[[GTOP:http://spock.genes.nig.ac.jp/~genome/gtop-j.html]]|ゲノムにコードされる全タンパク質の配列データを解析した結果をまとめたデータベース。配列相同性解析を主な手段として、立体構造の情報を積極的に利用していることが特徴
::Mycoplasma penetrans genome|マイコプラズマのゲノムデータベース。マイコプラズマは細胞壁やアミノ酸合成経路を持たない細菌。真核生物の細胞に共生する。ゲノムサイズは小さい。
+医薬
::[[ゲノムネットJAPIC:http://www.genome.jp/kusuri/]]|日本医薬情報センター(JAPIC)の医薬品添付文書情報とKEGG DRUGを統合したデータベース。
::[[OMIM:http://www.ncbi.nlm.nih.gov/omim/]]|Online Mendelian Inheritance in Manの略。ヒトの遺伝子と遺伝病のカタログ。
+糖鎖、脂質関連
::[[GGDB:http://riodb.ibase.aist.go.jp/rcmg/ggdb/]]|糖鎖に関連する遺伝子（糖転移酵素遺伝子など）の各種情報についてのデータベース
::[[LipidBank:http://lipidbank.jp/]]|整理活性脂質データベース。脂質に関するデータを化合物ごとに整理しデータベース化。
+海外
::EntrezＧene|
::RefＳeq|
::PIR|
::OMIM|
###  1-5 これから追加するデータベース [#uf91bbe0]
- [[理研のデータベース群:http://www.riken.go.jp/index_j.html]]
- 医薬系データベース
- タンパク関連データベース
#br
国内だけでも500以上のデータベースがあると予想されます。今後はこれらの中から役に立つものを順に追加していきます。


# 実習　それではみなさんも実際にキーワードを入力して検索してみましょう [#k9aa1faf]
- [[実践編>/AJACS5/thecla]]へ。
