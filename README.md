# Street-Traffic-Log
道路を走っている車両をAIでカウントする交通量調査アプリです。

# システムの全体像
![Street Traffic Log](https://user-images.githubusercontent.com/103170011/218346227-096fb450-419c-42a8-b925-56882ad592b4.png)

# 使い方

## 動作環境の設定
### ダウンロード
1.Street-Traffic-Logリポジトリをダウンロード

2.以下のURLからyolov7-seg.ptをダウンロードしyolov7-STL1の直下に置く。
https://github.com/RizwanMunawar/yolov7-segmentation/releases/download/yolov7-segmentation/yolov7-seg.pt  

### 動作環境
- anacondaの導入  
  以下のURLの公式サイトから導入  
  参照:https://www.javadrive.jp/python/install/index5.html

- anaconda promptを使って、以下の準備作業を行う。

### 仮想環境の作成
1.yolov7-STL1フォルダの中に入る。

2.以下のコマンド実行して仮想環境を構築する
```bash
conda env create -n yolov7STL -f yolov7STL.yml
```

※参照(anacondaでの仮想環境構築を知りたい人向け):https://tarovlog.com/2021/01/10/create-env-anaconda/  


### 仮想環境の起動
以下のコマンドで仮想環境を起動する。
```bash
conda activate yolov7STL
```

また、仮想環境を終了する場合は以下のコマンドで終了出来る。  
```bash
conda deactivate
```

## 実行
1.yolov7-STL1フォルダ内のsegmentフォルダの中に入る

2.以下のコマンドでメインプログラムを実行する。
```bash
python segment/predict_counting.py --weights yolov7-seg.pt --source Traffic.mp4 --view-img --trk --device 0 --nosave  
```

- ストリーミングのプロトコルはHTTP、RTSP、RTMPに対応。  

- 実行時のオプションについて  
  参照:https://zenn.dev/gotty/articles/6bd35b25cf3bd9  


# yolov7-image-segmentation(元のファイルのREADme.mdです)
This project is demonstrating simple traffic counting on toll road or highway using image segmentation technique with low light environment

This app is based on YOLOV7 object detection library engine from WongKinYiu repository on https://github.com/WongKinYiu/yolov7

And based on image segmentation and tracking github project from RizwanMunawar on https://github.com/RizwanMunawar/yolov7-segmentation.git

Run this command to run the app : python segment/predict_counting.py --weights yolov7-seg.pt --source 120.mp4 --view-img --nosave --trk

Notes: You can download yolov7-seg from https://github.com/RizwanMunawar/yolov7-segmentation/releases/download/yolov7-segmentation/yolov7-seg.pt

App Demo: https://www.youtube.com/watch?v=o3imTspjnn8

Sample Video: https://drive.google.com/file/d/1irx1XrYUmA34QNKfuX8KSRPPAOB5SYtc/view?usp=sharing

## Androidアプリ
Android-RTSP-App.zipを解凍し、AndroidStudioで実行

## 車両の判定に使うAI
yolov7-STL1


# ブログ
https://scrapbox.io/Street-Traffic-Log/
