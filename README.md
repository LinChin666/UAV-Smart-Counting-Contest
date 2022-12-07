# 無人機飛行載具之智慧計數競賽 - TEAM_2258
## 參賽者：國立勤益科技大學 電機工程系碩二 林晉儇 4b012123
## 競賽連結：https://tbrain.trendmicro.com.tw/Competitions/Details/25
## 競賽說明 
近年來科技高度發展所帶來之影響，已逐漸深入人類生活環境。無人飛行載具提供更寬廣的視野及更高度的移動性和靈活性，至今已被應用在許多不同產業領域，如地理資訊蒐集、交通監控、物品運送、通訊網路中繼站等不同類型。本次計畫著重於AI與影像辨識及無人飛行載具應用，期望參賽者以日常生活可能遭遇之問題為出發點，將深度學習原理作為基礎，運用相關人工智慧核心知識深入發展應用，進而將無人飛行載具相關技術應用於實際環境中，結合不同領域之人才並發揮創意，將平時所學專業知識確實落地，提升個人及團隊之實作能力與競爭力。 本次競賽主題為AI與影像辨識-無人機飛行載具之智慧計數（車輛與人群計數），無人機載具有高度移動性以及遠距遙控功能，能夠快速且輕易到達不容易接近的區域，搭配高解析度相機即如同鷹眼般，能從空中俯視地表，並將地表一切變化詳實記錄在影像中而不遺漏，目前國內尚無此空拍影像分析之比賽，此計畫將以無人機空拍影像為基礎，運用深度學習原理等相關訓練模組進行車輛與人群數量辨識。

## 最終成績
### Private Leaderboard：0.748631 (12名)
### Public Leaderboard：0.728647 (14名, 僅參考用)

## 環境與流程

### 1. 安裝配置環境
#### 硬體環境設置
- 筆電型號：MSI GP72 7REX
- 中央處理器：Intel(R) Core(TM) i7-7700HQ CPU @ 2.80GHz
- 圖像處理器：NVIDIA GeForce GTX 1050 Ti (GPU記憶體 12.0 GB：專屬GPU記憶體：4.0GB + 共用GPU記憶體：8.0GB)
- 記憶體：16384MB RAM
- 作業系統：Windows 10 家用版 64 位元
- 虛擬環境：Anaconda 虛擬環境 (UAV)
#### 軟體開發套件
- 程式語言：Python
- 開發平台：Anaconda - Spyder
- 深度學習套件：PyTorch
- 深度學習模型：YOLOv5
- 軟體套件：gitpython、ipython、matplotlib、numpy、opencv-python、Pillow、psutil、PyYAML、requests、scipy、thop、torch、torchvision、tqdm、tensorboard、pandas、seaborn

### 2. 資料處理、重要模塊輸出/輸入
#### 資料介紹與擴充
- 訓練資料：1000張訓練照片
- 測試資料：500張公開照片、500張私有照片
- 水平翻轉：1000張照片
- 垂直翻轉：1000張照片
- 照片亮度調整：2000張照片
- 擴充後訓練資料量：5000張照片
#### 資料分割
- 訓練資料分割方法：訓練資料集和驗證資料集比例為9:1
- 訓練資料：4500張照片
- 測試資料：500張照片
#### 深度學習模型模型輸入與輸出
- 深度學習模型輸入：增強後的訓練資料與驗證資料
- 深度學習模型輸出：偵測框的位置資訊和信心指數

### 3. 訓練流程
#### 訓練方法
```
python train.py
```
#### 參數設定 
- 信心度門檻值
- 過濾重疊框門檻值

### 4. 模型預測
#### 偵測方法
```
python detect.py
```
#### 參數設定
- 信心度門檻值
- 過濾重疊框門檻值

## 重新訓練與結果重現步驟
### 1. 前置作業
1. 下載這裡的程式碼並放到工作資料夾
2. 按照下方方式擺放好訓練資料與測試資料
UAV-Smart-Counting-Contest
>>>> datasets
>>>>>>> test (1000張照片)
>>>>>>> train (4500張照片)
>>>>>>> val (500張照片)
### 2. 重新訓練方法
```
python train.py
```
### 3. 結果重現方法
```
python detect.py
```
### 上傳的檔案

## 參考資料
- https://github.com/ultralytics/yolov5
- https://medium.com/@_Xing_Chen_/yolov5-%E8%A9%B3%E7%B4%B0%E8%A7%A3%E8%AE%80-724d55ec774
- https://officeguide.cc/pytorch-yolo-v5-object-egg-detection-models-tutorial-examples/
- https://yulongtsai.medium.com/object-detection-data-collection-16d551526a33

## 
