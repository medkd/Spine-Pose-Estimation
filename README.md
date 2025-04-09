# Spine-Pose-Estimation
Cobb angle and LTV detection

Using Stacked Hourglass Network for Vetebra boundary points detection, and then calculate Cobb angle based on derivatives


1. 利用matlab定出vertebra的四個角座標，分別從T1-L5以及S1中點
2. 將四個角座標取平均，訂出每個vertebra的重心
3. 訓練Stacked hourglas model以偵測:
   (1)各vertebra重心 --> 請參閱 vertebra_centrioid_model.ipynb
   (2)各vetebra上下左右四個點座標 --> 請參閱vertebra_4_point_model.ipynb
4. 訓練後使用Demo.ipynb即可自動判斷該Whole spine X ray的
   (1) Last touched vetebra
   (2) 各個curve的apex, upper endplate, lower endplate 以及對應的Cobb angle
