請用 Google Earth Engine 完成以下分析：

* **地表溫度** ：`MODIS/061/MOD11A2`，Band `LST_Day_1km`，時間範圍 2022-06-01 至 2022-08-31，取平均值，換算公式：`LST_celsius = LST * 0.02 - 273.15`
* **土地利用** ：`MODIS/061/MCD12Q1`，Band `LC_Type1`，年份 2022，都市像素 = class 13，農村像素 = class 12（耕地）
* **縣市邊界** ：`FAO/GAUL/2015/level2`，篩選 `ADM0_NAME == 'Taiwan'`
* 對每個縣市計算：都市像素平均溫度 − 農村像素平均溫度 = 熱島強度
* 輸出：各縣市名稱與對應熱島強度（°C），以 `print()` 顯示並匯出為 CSV
