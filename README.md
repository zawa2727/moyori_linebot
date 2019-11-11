# moyori_linebot  
現在大学の研究室でPythonを学習中のため、Pythonでも何か作ってみようと思い、最寄り駅を教えてくれるLINEボットを作成しました。  
MessagingAPIを介してやり取りを行い、内部処理の部分をPythonでFlaskをインポートして書いています。  
最寄り駅の受け取りにはSimpleAPIを、距離や時間の計算やマップの出力にはGoogleAPIを利用しました。  
大まかな流れは以下の通りです。  
１．「最寄り駅」と話しかけてもらい位置情報を受け取る  
２．送られた位置情報をもとに最寄り駅を探し、距離や時間を計算する。  
３．MessagingAPIを通してLINEに結果を送信する。  
※実際に動かすにはenvファイルに各種環境変数の設定をする必要があります。  
