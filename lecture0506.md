# lecture05・06の学び

## CloudTrail のイベントについて直近の3イベント
- CreateTrail  CloudTrailを作る  
- PutEventSelectors  CloudTrailデータイベントをログ記録する 
- StartLogging   CloudTrailロギングの開始  
<イベント履歴画像>  
/lecture0506image/lecture0506(1).png  

## CloudWatch アラームについて
- Unicornを起動させて、アプリが表示できるようにしないとCloudWatchアラームが  
ずっとデータ不足のままで起動しない事がわかった。  
- メトリクスの選択の際、何日間か前に作ったALBがが残ってしまうので、要注意。  
ロードバランサーARNの末尾の部分を参考に該当ALBを探すのが良いと判明した。  
- アラーム状態とOKアクションは1つのCloudWatch アラームでできることがわかった。  

## AWS 利用料の見積について
- 当初、ネットの記事を参考に作成したところ、毎日一定量を使う計算となり、  
年額で200万円くらいかかる事になってしまったが、週にどれくらい使うかに変更したり、  
内容をもっと小さいものを設定したことを思い出して、現状に近い料金にできた。  
https://calculator.aws/#/estimate?id=26b40abe26c552ebc39fd9b6f70517e988bfdceb  

## マネジメントコンソールから、現在の利用料を確認して教えてください
- 現在、3月のAWSのオンラインイベントのアンケートに答えてでクレジットを50ドル  
もらったので、料金の支払いはここ2ヶ月発生していません。  
- なお、無料枠は既に終了しています。  
<現在の利用料画像>  
/RaiseTech_lecture2/lecture0506image/lecture0506(2).png  

## 質問  
- CloudWatch アラームで、RDSが起動したら通知という条件ができるんでしょうか？