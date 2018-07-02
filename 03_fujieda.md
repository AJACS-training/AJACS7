[[AJACS7]]
        --
目次

#contents
        --

#  アナトモグラフィーの場所 [#t45b2282]
- [[統合データベースプロジェクト:http://lifesciencedb.jp]]の「統合ツール」もしくは、「ボディパーツ３D緑のバナー」から。
- [[トップページURL (http://lifesciencedb.jp/ag):http://lifesciencedb.jp/ag]]
- [[「アナトモグラフィー」でgoogle検索:http://www.google.co.jp/search?q=%E3%82%A2%E3%83%8A%E3%83%88%E3%83%A2%E3%82%B0%E3%83%A9%E3%83%95%E3%82%A3%E3%83%BC&lr=lang_ja&ie=utf-8&oe=utf-8&aq=t]]

#  アナトモグラフィーとは [#t45b2282]
解剖学用語を選択して自由に人体のモデル図(アナトモグラム)を描くツールです。

#  方法２：表形式(CSVフォーマット）で一括入力してマップを作成する手順 [#p2d331fb]

目的：AQP3遺伝子の臓器別発現量を人体ヒートマップで表示します。

- 手順１．アナトモグラフィー(Anatomography)エディタ(CSVデータ入力)画面を表示します。
    -[[アナトモエディタ:http://lifesciencedb.jp/ag/]]上部の~
”臓器名と数値（例：発現量など）を表形式...こちらから”の[[”こちら”:http://lifesciencedb.jp/ag/form/indexCSV.jsp]]からをクリック。~
もしくは、
    -[[URL(http://lifesciencedb.jp/ag/form/indexCSV.jsp):http://lifesciencedb.jp/ag/form/indexCSV.jsp]]を入力してアクセス。

- 手順２．以下の表形式データをテキストエリア（臓器）に貼り付けます。~
各列（カンマ区切り）の意味は以下の通りです。

 臓器名, s(表示) or z(拡大表示), 色情報（数値 or RGB(例:255,0,0)), 不透明度(0.0-1.0 省略時:1.0(不透明))

 腎臓,s,300
 気管,s,1500
 唾液腺,s,1000
 膵臓,s,1200
 前立腺,s,1250
 肺,s,1500
 肝臓,s,250
 骨,s,-1,-1,-1,0.5

- 手順３．画面下の「Submit」ボタンをクリックします。~
カラーバーを表示したい場合は、「カラーバーの表示」をOnにします。

#ref(anatomography2570.png,left)

- おまけ：特定の臓器を拡大表示したい場合は、s→zに変えます。以下のように皮膚以外の臓器をzにすると、皮膚以外の臓器全てがちょうど収まるようにズームされます。

 腎臓,z,300
 気管,z,1500
 唾液腺,z,1000
 膵臓,z,1200
 前立腺,z,1250
 肺,z,1500
 肝臓,z,250
 骨,s,-1,-1,-1,0.5

#ref(Image22.jpg,left)

#  講習会資料(pdf)ダウンロード [#lc3c4d8d]

#ref(ajacs7（長津田）アナトモグラフィー.pdf,left)

#  統合TVアナトモグラフィー [#h88014f6]
- http://togotv.dbcls.jp/movie/080926ag3_f.html
- http://togotv.dbcls.jp/movie/080606AgService2_f.html
