# ML_final_project
PUBG final rank prediction  
  
資料集與模型檔較大放在以下雲端:  
https://drive.google.com/drive/folders/1FC6uMjBmogZKreGTsW3zTAMQMjRDWYee?usp=sharing  

可下載PDF觀看完整報告

### 內容敘述
Kaggle上的資料集，內容包含知名大逃殺遊戲PUBG的玩家遊玩資料，紀錄該玩家在一場遊戲中的移動距離、獲取裝備數、擊殺數等數十項資訊，以及該玩家的最終名次百分比。  
![image](https://github.com/mengbei0116/ML_final_project/blob/main/PUBG%E7%89%B9%E5%BE%B5.png)

我設計了兩個目標，分別是利用遊玩資訊預測出他的最終名次(回歸)，以及利用遊玩資訊與名次判斷該玩家遊玩的模式(分類)，透過實作了解不同機器學習的資料清洗、前處理、建模等等。並且實作一簡單介面可以輸入單場玩家資訊，預測出他該場的實際名次。  

#### 實作步驟簡述  
1.人工去除與名次無關之資料(如玩家編號等資訊)  
2.資料觀察
3.找出關聯性過高之feature刪除以減少feature數   
    
以下為名次預測回歸任務    
4.根據遊玩模式分群     
5.拆分訓練集與測試集    
6.剔除訓練集中過於誇張之數值    
7.利用隨機森林與Gradient boost進行訓練    
    
以下為模式判斷分類任務    
8.拆分訓練集與測試集    
9.使用SMOTE平衡各模式樣本數    
10.利用決策樹、隨機森林、Adaboost進行訓練

#### 效果評估
名次預測:R2 score 0.92  
模式判斷:accuracy 0.82  

### 名次預測UI使用方法
將模型檔與"輸出.py"載下來放入相同資料夾，即可執行。  
接著將單場單玩家資訊依照csv檔的格式輸入後，將csv檔路徑輸入進介面即可進行預測名次。
![image](https://github.com/mengbei0116/ML_final_project/blob/main/%E9%A0%90%E6%B8%AC%E5%99%A8.png)
