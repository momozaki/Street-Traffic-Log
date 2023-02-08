# yolov7-image-segmentation
This project is demonstrating simple traffic counting on toll road or highway using image segmentation technique with low light environment

This app is based on YOLOV7 object detection library engine from WongKinYiu repository on https://github.com/WongKinYiu/yolov7

And based on image segmentation and tracking github project from RizwanMunawar on https://github.com/RizwanMunawar/yolov7-segmentation.git

Run this command to run the app : python segment/predict_counting.py --weights yolov7-seg.pt --source 120.mp4 --view-img --nosave --trk

Notes: You can download yolov7-seg from https://github.com/RizwanMunawar/yolov7-segmentation/releases/download/yolov7-segmentation/yolov7-seg.pt

App Demo: https://www.youtube.com/watch?v=o3imTspjnn8

Sample Video: https://drive.google.com/file/d/1irx1XrYUmA34QNKfuX8KSRPPAOB5SYtc/view?usp=sharing


# 使い方
anacondaの導入  
公式サイトから導入  
参照:https://www.javadrive.jp/python/install/index5.html

環境設定はanacondaを導入してきたときに付いてきたanaconda promptを用いる

仮想環境の作成  
anaconda　promptでyolov7-STLフォルダの中に入り、yolov7-STLフォルダの中にあるyolov7STL.ymlを使って仮想環境を構築  
yolov7-STLフォルダの中に入った状態で  
conda env create -n [お好みの環境名] -f yolov7STL.yml  
で仮想環境の構築が出来る  
参照:https://tarovlog.com/2021/01/10/create-env-anaconda/  


仮想環境の起動  
conda activate 作った環境名  
で起動  
仮想環境を終了する場合はconda deactivateで終了出来る  

https://github.com/RizwanMunawar/yolov7-segmentation/releases/download/yolov7-segmentation/yolov7-seg.pt  
からyolov7-seg.ptをダウンロードしyolov5s-seg.ptと同じ階層に配置  

メインプログラムはyolov7-STLフォルダの中のsegmentフォルダの中にあるpredict_counting.py  
そのためyolov7-STLフォルダの中に入った状態で
python segment/predict_counting.py --weights yolov7-seg.pt --source [動画名、またはストリーミングのURL] --view-img --trk --device 0 --nosave  
で実行できる。  
ストリーミングのプロトコルはHTTP、RTSP、RTMPに対応  

実行時のオプションについて  
参照:https://zenn.dev/gotty/articles/6bd35b25cf3bd9  
