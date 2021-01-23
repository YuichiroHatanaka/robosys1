# あ行のモールス信号の出力

## 実装内容

* LEDの点滅で”あいうえお”のモールス信号を出力する。

---

## 用意する物
* Raspberry Pi 4 
* ブレッドボード
* LED *1
* 抵抗　300Ω *2
* ジャンパー線 オス−メス *2

---
## 回路
以下のように回路を組みました。

<img src=https://github.com/YuichiroHatanaka/robosys1/blob/main/PXL_20210123_153820663.jpg width=500px/>
LEDはアノードがGPIO25に接続しています。GNDはどこでも構いません。
---

## ビルド
実行する場合、以下のように行ってください。

* $ git clone https://github.com/YuichiroHatanaka/robosys1.git  
* $ cd robosys1/myled  
* $ make  
* $ sudo insmod myled.ko  
* $ sudo chmod 666 /dev/myled0  

## 実行した場合
* 0を入力した場合

　$ echo 0 > /dev/myled0  
 
 LEDが消灯

* 1を入力した場合

　$ echo 0 > /dev/myled0
 
 LEDが点灯

* 2を入力した場合

　$ echo 0 > /dev/myled0 
 
 1秒後にLEDが点灯
 
* 3を入力した場合

　$ echo 0 > /dev/myled0 

LEDが点灯し、1秒後に消灯

* aを入力した場合

　$ echo 0 > /dev/myled0 
 
 "あ"のモールス信号が出力される

* iを入力した場合

　$ echo 0 > /dev/myled0 
 
  "い"のモールス信号が出力される

* uを入力した場合

　$ echo 0 > /dev/myled0 
 
  "う"のモールス信号が出力される

* eを入力した場合

　$ echo 0 > /dev/myled0 
 
  "え"のモールス信号が出力される

* oを入力した場合

　$ echo 0 > /dev/myled0 
 
  "お"のモールス信号が出力される
 
---
## 実行動画

動画URL:https://youtu.be/vAC13WaXVMQ

youtubeにあげた実行動画はこちらになります。

## ライセンス
[GNU General Public License v3.0](https://github.com/YuichiroHatanaka/robosys1/blob/main/README.md)
