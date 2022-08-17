# YOLOv4安裝流程
# 安裝python 3.7.7 
## 到 https://www.python.org/downloads/windows/
![image](https://user-images.githubusercontent.com/79627981/185031504-d3bc5a23-0f1c-4225-829a-9388a4990198.png)
## 將python加入path
![image](https://user-images.githubusercontent.com/79627981/185031680-0a73ab2e-aa7d-415b-83d2-b54fb9d4c85d.png)
## 到cmd去 pip -V 查看python版本是否為3.7
## 如果不是的話要去環境變數設定
![image](https://user-images.githubusercontent.com/79627981/185031840-70285723-a0fb-4ebe-9214-1b4d67ffce4f.png)
![image](https://user-images.githubusercontent.com/79627981/185032149-ada0d220-b9a7-4294-b694-95e5d40828a9.png)
## 確認python版本為3.7後 pip install numpy
![image](https://user-images.githubusercontent.com/79627981/185032478-c1611983-733b-41c8-a04e-9f9eade4868b.png)

# 去下載git跟CMake 
## https://git-scm.com/   https://cmake.org/download/
![image](https://user-images.githubusercontent.com/79627981/185032921-b98b268c-1c21-477f-9b76-574710b0659e.png)
![image](https://user-images.githubusercontent.com/79627981/185032860-91056ebb-d577-4989-9388-afe8863f11be.png)

# 安裝Visual Studio
### 影片是下載2019的版本但我是用2022所以到使用CMake那附近會出錯
## 安裝VS 、英文語言套件 https://visualstudio.microsoft.com/zh-hant/downloads/ 
![image](https://user-images.githubusercontent.com/79627981/185033269-83307fad-a65f-4857-80a5-a4501c718024.png)
![image](https://user-images.githubusercontent.com/79627981/176881867-6fbf4853-22f9-47f9-a632-8981a29c822e.png)
## 在安裝編譯軟體[VScode](https://code.visualstudio.com/download)
![image](https://user-images.githubusercontent.com/79627981/185033380-1a547c9e-c671-4aea-bc19-5a8f00453a04.png)

# 更新顯卡驅動
#先確認顯卡型號
![image](https://user-images.githubusercontent.com/79627981/185033750-1e33cecf-4068-4602-83a7-2edde2251c91.png) 
#到 https://www.nvidia.com/zh-tw/geforce/drivers/ 去更新驅動
![image](https://user-images.githubusercontent.com/79627981/185033927-07b869c7-f3af-4137-bfff-e6d4c3c60b7f.png)

# 安裝CUDA
## 先去wiki去看CUDA對應支援的顯卡型號  https://en.wikipedia.org/wiki/CUDA
## 有超過3.0就好
![image](https://user-images.githubusercontent.com/79627981/185034340-fae90d67-7e79-4aac-b716-1b332e2f3ec9.png)
## 到CUDA Toolkit下載CUDA，影片中的版本是10.2，而我是下載11.7，要記起來後面會用到
##  https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=11
![image](https://user-images.githubusercontent.com/79627981/185034472-a891a13f-367f-4aee-a80f-a40990588791.png)
## 安裝路徑可以放在C:或D:槽\CUDA裡面就好，不用中間再夾一堆路徑

# 安裝cuDNN 
## 到 https://developer.nvidia.com/rdp/cudnn-archive 下載，要先辦帳號才能下載(記得要載對應CUDA版本的版本)
![image](https://user-images.githubusercontent.com/79627981/185035398-ac878143-2526-48fc-b7b8-09be76499c85.png)
## 載完後解壓縮到C:\或D:\ 都可以
![image](https://user-images.githubusercontent.com/79627981/185035655-ef8d043c-aa99-4d3a-8ef9-1fcbc8ca6572.png)

# 將cdDNN的資料複製到CUDA內
## 把bin lib include三個資料夾 {裡面的} 檔案分別複製到CUDA的 bin lib include資料夾內
### 影片內的檔案才幾個而我有很多，但應該沒差
![image](https://user-images.githubusercontent.com/79627981/185035954-b09cd531-b34b-4afd-9899-132251936800.png)




## 安裝OpenCv (https://opencv.org/releases/)
### 安裝在C槽或D槽
![image](https://user-images.githubusercontent.com/79627981/176902332-476e8dfe-f65e-413b-987d-372bebb9e9a2.png)
![image](https://user-images.githubusercontent.com/79627981/176902672-04cb97ab-14af-4407-81a6-bd466de47ea5.png)
## 在C:\或D:\新增一個opencv資料夾
## 安裝完後將兩個檔案解壓縮然後放到剛剛建立的opcv資料夾內
![image](https://user-images.githubusercontent.com/79627981/185037049-b71e5bc8-5fef-4be5-9c3b-b3006b19f750.png)

# 使用CMake
## 在上一步的opencv資料夾中建一個build資料夾
## 進到D:\opencv\opencv-4.1.0\cmake
![image](https://user-images.githubusercontent.com/79627981/185037465-cfe79000-5f05-4fbc-96ae-6c913abd722a.png)
## 打開 OpenCVDetectPython 將裡面所有的python2改成python3 然後儲存就可以關掉了
![image](https://user-images.githubusercontent.com/79627981/185037636-e72a3bb8-71b8-4f13-bc5e-95123737c44d.png)
## 打開CMake 按下Configure
![image](https://user-images.githubusercontent.com/79627981/185037957-0c4bb381-bbca-4f72-963c-cc8626dbd663.png)
## 選完BUILD_opencv_world[勾]、OPENCV_GENERATE_SETUPVARS[不勾]這兩個後，再Configure一次沒問題的話Generate就可以了
![image](https://user-images.githubusercontent.com/79627981/185038276-d59c8f89-a429-4dde-8632-0cc5d4d5ddb5.png)
![image](https://user-images.githubusercontent.com/79627981/185038304-68382693-45d0-4876-8ee0-e0a0821291c6.png)
## 進到build資料夾內
![image](https://user-images.githubusercontent.com/79627981/185038664-42f63433-6d2d-471c-91e9-20466e919802.png)
## 進到VS內後把Debug改成Release 然後對 ALL BUILD 跟 INSTALL 進行建置，這邊應該會出現錯誤，如果都沒錯就可以關掉了
![image](https://user-images.githubusercontent.com/79627981/185038774-71e683d6-5038-47b5-99dc-352bb11334b8.png)

# 安裝darknet
# 新增一個Yolo_v4資料夾
![image](https://user-images.githubusercontent.com/79627981/185039471-ab501430-3522-4591-9ec4-7c6b8ca58f8a.png)
## Yolo_v4到資料夾內輸入cmd
![image](https://user-images.githubusercontent.com/79627981/185039633-0334b523-71fc-4431-a0ee-b524a844c965.png)
## 在cmd內輸入這串 git clone  https://github.com/AlexeyAB/darknet
![image](https://user-images.githubusercontent.com/79627981/185039528-10a5a877-cd3a-4cc8-8b8c-b727e64e1955.png)
## 把 D:\opencv\build\bin\Release 內的 opencv_ffmpeg410_64.dll跟opencv_world410.dll 複製到               D:\Yolo_v4\darknet\buil d\darknet\x64裡面
![image](https://user-images.githubusercontent.com/79627981/185040694-182b3b50-7644-43cd-8d79-bfb283472c48.png)
## 再把 C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.7\bin 內的 cudnn64_8.dill 放到 D:\Yolo_v4\darknet\build\darknet\x64裡面
![image](https://user-images.githubusercontent.com/79627981/185041200-3cdb0be3-4a01-41e3-a8fc-bd3430fc759b.png)
## 把darknet.vcxproj 用VScode打開，把程式碼裡面全部的CUDA的版本改成 11.7
![image](https://user-images.githubusercontent.com/79627981/185041310-821e4395-c828-4f7c-b00e-b6e5da702f42.png)
![image](https://user-images.githubusercontent.com/79627981/185041506-34bef650-0ca0-49c3-9b77-d90dc03b2112.png)
## 把跟上一步一樣 將yolo_cpp_dll.vcxproj用VScode打開並把改成 11.7

# 建置yolo_cpp.dill
## 將yolo_cpp_dll.vcxproj用VS打開並建置
## 這邊應該會出錯
![image](https://user-images.githubusercontent.com/79627981/185041971-50df3c52-42c4-47be-bae2-bbc998f14f02.png)

# 更改屬性
##  D:\Yolo_v4\darknet\build\darknet 用VS打開 darknet.sln
![image](https://user-images.githubusercontent.com/79627981/185042359-0ef8ed68-8501-47f1-af0d-ff7209958bb5.png)
## 打開darknet屬性
![image](https://user-images.githubusercontent.com/79627981/185042321-1fe148e1-398e-442f-a7aa-6a5f0e9f5d55.png)
## https://youtu.be/PVf16gIhnek?t=1735 這邊步驟比較多所以看影片照做比較快
### CUDA Device這邊時影片會把compute75_,sm_75刪掉，而我的不是75是85但沒差我還是照刪了只留第一個
![image](https://user-images.githubusercontent.com/79627981/185042449-f8dd812c-bac4-4b44-bff1-2d9e5a0deca4.png)

# 開始測試
## 到 D:\Yolo_v4\darknet\build\darknet\x64 輸入cmd
![image](https://user-images.githubusercontent.com/79627981/185043354-6b5e3be8-cd2e-4114-a526-bd111cba420c.png)
##　在小黑輸入　darknet.exe detector test cfg/coco.data cfg/yolov4.cfg yolov4.weights 
### 這邊會出錯
![image](https://user-images.githubusercontent.com/79627981/185043731-a474e939-0b7d-4fde-8395-2ba7a3da4a52.png)
## 這邊再輸入圖片的路徑就可以成功執行了
![image](https://user-images.githubusercontent.com/79627981/185043765-9234d29d-d4b7-4eb1-a94e-7019ab13bf51.png)
# YORO!
![image](https://user-images.githubusercontent.com/79627981/185044067-1e79cd42-76a1-4c2c-b474-cb76ef2b0674.png)
# 參考資料 https://www.youtube.com/watch?v=PVf16gIhnek&ab_channel=%E6%9F%AF%E6%9F%AF
