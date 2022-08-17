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
# 先確認顯卡型號
![image](https://user-images.githubusercontent.com/79627981/185033750-1e33cecf-4068-4602-83a7-2edde2251c91.png) 
# 到 https://www.nvidia.com/zh-tw/geforce/drivers/ 去更新驅動
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

# 安裝OpenCv 
## 安裝opencv 4.1.0  https://github.com/opencv/opencv/archive/4.1.0.zip
## 安裝opencv_contrib https://github.com/opencv/opencv_contrib/archive/refs/heads/4.x.zip
![image](https://user-images.githubusercontent.com/79627981/176902332-476e8dfe-f65e-413b-987d-372bebb9e9a2.png)
![image](https://user-images.githubusercontent.com/79627981/176902672-04cb97ab-14af-4407-81a6-bd466de47ea5.png)
## 至 https://github.com/AlexeyAB/darknet 去下載
# YORO!
![image](https://user-images.githubusercontent.com/79627981/185030348-3ec17bcf-2f72-4c1d-bc1f-9cd0bbaa14d8.png)
# 參考資料 https://www.youtube.com/watch?v=PVf16gIhnek&ab_channel=%E6%9F%AF%E6%9F%AF
