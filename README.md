# task_1
ロボットシステム学の課題１

授業動画を参考にLEDの追加とバッシュファイルで少しの遊びを入れた

# 使用したもの
ラズパイ３　B+   
ブレッドボード  
LED ジャンパー線  
抵抗　240Ω  
  
# 使い方
$ make   
$ sudo rmmod myled    
$ sudo insmod myled.ko  
$ sudo chmod 666 /dev/myled0  
  
 ・LEDを片方だけつける場合
 
$ echo 1 > /dev/myled0  もしくは　$ echo 3 > /dev/myled0  
消すときは１で点いたほうは代わりに0  
3で点いたほうは2で消える  
消すのは  
0 2  
つけるのは  
1 3  


 ・2つのLEDを使ったつく回数と切り替わる時間をコントロールするプログラム  
  
$ bash tempo.bash  
回数と切り替わりの時間を聞かれるので入力すると  
回数を表示しながらチカチカ光る  
