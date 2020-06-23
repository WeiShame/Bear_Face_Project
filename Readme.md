# Disease_Prevention_Project
於COVID-19(武漢肺炎)期間開發的防疫系統，透果臉部辨識紀錄教職員的活動紀錄，以確實記錄教職員的活動軌跡。
> 因為資料敏感，所以不提供資料

## 安裝步驟:
(因為電腦問題environment無法匯出，所以手動安裝package)
powershell=
conda install -c conda-forge opencv

到https://pypi.org/simple/dlib/ 下載dlib-19.8.1-cp36-cp36m-win_amd64.whl
pip install dlib-19.8.1-cp36-cp36m-win_amd64.whl

pip install face_recognition
conda install -c conda-forge psutil
conda install -c conda-forge dataclasses
pip install easygui

#### 或是試試看引入環境
powershell=
conda env create -f Face_Recognition_Project\Disease_Prevention_Project\V8\environment.yml

## 執行步驟：

### 創建.db擋
powershell=
python encode.py\
--image [PATH/TO/IMAGE_DIRECTORY]\
--excel [PATH/TO/EXCEL_FILE]\
--db [PATH/TO/DB_FILE]

#### 注意:
1. Excel .xls檔格式
![](https://i.imgur.com/Qi3KxGE.png)
2. **每個圖片的檔名需要與staff_cd一樣**



### 

### 開啟臉部辨識
1. 移動到目的資料夾
powershell=
cd Face_Recognition_Project\Disease_Prevention_Project\V8\

2. 執行主程式：

powershell=
python video_demo.py [PATH]
> PATH: video_demo.py的位置

EX.

powershell=
python .\video_demo.py D:\大三\專題\防疫專案\Others\Bear_Face_Project\Disease_Prevention_Project\V7

#### 注意：
V8前一個資料夾需要有Start_temp.bat(為了與學長的程式合併)
V8需要有Release資料夾

## demo流程：
1. 先選擇要當作人臉辨識的相機，選完後會執行FLIR的Start_temp.bat(只先將他們的.bat設為pause)
![](https://i.imgur.com/WsrYBnd.jpg)

2. 在框內才會偵測人臉
![](https://i.imgur.com/DxWL81d.jpg)

3. 按s儲存照片
![](https://i.imgur.com/MA0nKSC.jpg)

7. 按q退出
