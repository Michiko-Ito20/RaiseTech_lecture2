# lecture3 アプリケーションの構築
- トークンを設定した記憶が無かった
- Windowsならではの事象が起こったりして慌てたが、エラーコードは落ち着いて読めるようになってきたのでちょっと進歩しました  
![画像1](lecuture03image/lecuture3_app.png)

## アプリケーションサーバーについて調べる

- `puma -v`  
Puma version: 5.6.7 (ruby 3.1.2-p20) ("Birdie's Version")  
![画像2](lecuture03image/lecuture3_puma-v.png)

### puma stop時にどうなるか  
- Railsアプリケーションの表示ができました
![画像3](lecuture03image/lecuture3_pumaStop2.png)

## DBサーバーについて調べる  
 - SHOW DATABASES;  
![画像4](lecuture03image/lecuture3_SHOWDATABASES.png)

 - `mysql -V`  
sql Ver 8.0.35  
![画像5](lecuture03image/lecuture3_mysql-V.png)  

 - `bundle -v`  
Bundler version 2.3.14  
![画像6](lecuture03image/lecuture3_BundlerVersion.png)  

### mysqld stop時にどうなるか  
- Railsの画面は表示されなくなり、エラーとなりました
![画像7](lecuture03image/lecuture3_mysqlStop.png)  

## アプリの表示が当初うまくいかなかった  
-  課題には無かったが、アプリを表示した時に貼り付けた画像が上手く表示され無かったので解消させてみた
-  ログがどこにあるか調べる　　アプリケーションの中？
-  ログがどこにあるか仮説を立てる　アプリケーション
-  本当にあるのか調べる　　アプリケーションのファイルバーの中から探せた  
![画像8](lecuture03image/lecuture3_appError.png)  

### 結果、ImageMagickが無いというエラーがログに出ていたので解消できた
![画像9](lecuture03image/lecuture3_appErrorWord.png)
-  `sudo yum install -y ImageMagick`  
![画像1](lecuture03image/lecuture3_app.png)
