# 最寄り駅検索　LINEBot  
就活をしていく中で、今まで一度も訪れたことのない場所に行くことが増え、近くの駅がどこか分からないという状況が頻発したため、位置情報を送るだけで簡単に最寄り駅を教えてくれるLINEボットを作成しました。就活以外に、終電間際ですぐに最寄り駅を知りたいという場合にも役立つかと思います。  

現在大学の研究室（ゼミ）でPythonを学習中ということもあり、内部処理にはPythonを採用しました。
LINEへのメッセージの送受信はMessagingAPIを介して行っています。  
また、内部処理の部分はPythonでFlaskをインポートして書いており、LINEからアクションがあった場合にHeroku上で動作します。  
最寄り駅の検索にはSimpleAPIを、距離や時間の計算やマップの出力にはGoogleAPIを利用しました。  

大まかな流れは以下の通りです。  
１．LINEで「最寄り駅」と話しかけてもらい位置情報を受け取る  
２．送られた位置情報をもとにSimpleAPIを用いて最寄り駅を探し、GoogleMapsAPIで距離や時間を計算する。  
３．MessagingAPIを通してLINEに結果を送信する。  
※実際に動かすにはenvファイルに各種環境変数の設定をする必要があります。  

さらに徒歩時間を考慮して、目的地を送信すると次の電車の時刻を教えてくれる機能など実装するとより使い勝手が良くなるのではないかと思います。  


制作にあたり、以下のサイトを参考にさせていただきました。  
http://rautaku.hatenablog.com/entry/2018/01/07/153000  
  
