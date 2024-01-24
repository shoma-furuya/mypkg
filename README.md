# ros2 
![test](https://github.com/shoma-furuya/robosys2023/actions/workflows/test.yml/badge.svg)


## mypkg
このレポジトリは、ロボットシステム学の講義を元に作成したレポジトリである


## インストール方法
ROS2をインストール、その後以下のコマンドでインストール可能
```
$ git clone https://github.com/shoma-furuya/mypkg.git
```
インストール後、以下のコマンドでディレクトリを移動すると、コマンドが使用可能
```
$ cd mypkg
$ source ~/.bashrc
```


## ノードの説明
#### talker.py
* トピックにメッセージを出すパブリッシャを持つ
#### listener.py
* トピックからメッセージを受け取るサブスクライバーを持つ
#### talk_listen.launch.py
* talker.pyとlistener.pyの二つのノードを一度に立ち上げるlaunchファイル

## 使用方法
### talkerとlistenerの実行
* 以下のコマンドで実行
```
$ ros2 run mypkg talker
(何も表示されない)
```
* 別の端末を開いて以下のコマンドで実行し、サブスクライブする
```
$ ros2 run mypkg listener
[INFO] [1703967181.715403497] [listener]: Listen: 354
[INFO] [1703967182.209274960] [listener]: Listen: 355
[INFO] [1703967182.709573117] [listener]: Listen: 356
[INFO] [1703967183.209397837] [listener]: Listen: 357
[INFO] [1703967183.709303066] [listener]: Listen: 358
[INFO] [1703967184.209870238] [listener]: Listen: 359
[INFO] [1703967184.709663779] [listener]: Listen: 360
[INFO] [1703967185.210034754] [listener]: Listen: 361
[INFO] [1703967185.709541268] [listener]: Listen: 362
[INFO] [1703967186.209616140] [listener]: Listen: 363
[INFO] [1703967186.709539119] [listener]: Listen: 364
[INFO] [1703967187.209197676] [listener]: Listen: 365
[INFO] [1703967187.710033194] [listener]: Listen: 366
[INFO] [1703967188.209642135] [listener]: Listen: 367
[INFO] [1703967188.709502362] [listener]: Listen: 368
[INFO] [1703967189.209557251] [listener]: Listen: 369
(Ctrl + C 押すまで続く)
```

### talker_listen.launch.pyの実行
* 以下のコマンドでローンチファイルを実行する
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/tom1513/.ros/log/2023-12-31-05-21-01-190379-shoumapc-29998
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [30000]
[INFO] [listener-2]: process started with pid [30002]
[listener-2] [INFO] [1703967662.085697702] [listener]: Listen: 0
[listener-2] [INFO] [1703967662.564067077] [listener]: Listen: 1
[listener-2] [INFO] [1703967663.064108130] [listener]: Listen: 2
[listener-2] [INFO] [1703967663.563971807] [listener]: Listen: 3
[listener-2] [INFO] [1703967664.064288186] [listener]: Listen: 4
[listener-2] [INFO] [1703967664.564109171] [listener]: Listen: 5
[listener-2] [INFO] [1703967665.064237431] [listener]: Listen: 6
[listener-2] [INFO] [1703967665.564372943] [listener]: Listen: 7
[listener-2] [INFO] [1703967666.063850570] [listener]: Listen: 8
[listener-2] [INFO] [1703967666.564056938] [listener]: Listen: 9
[listener-2] [INFO] [1703967667.064387176] [listener]: Listen: 10
(Ctrl + C 押すまで続く)

```

## 必要なソフトウェア
* ROS2 foxy


## テスト環境
* Ubuntu 20.04


## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2024 Shoma Furuya
