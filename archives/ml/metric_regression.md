---
title: "Useful metrics for Regression problems"
date: 2022-11-15T15:15:16+07:00
tags:
  - "tech"
  - "learn"
draft: false
cover:
    #image: "https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png"
    # can also paste direct link from external site
    # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
    alt: "<alt text>"
    caption: "<text>"
    relative: false # To use relative path for cover image, used in hugo Page-bundles
---

# Metrics trong Machine Learning - Regression (P1)

Trong phần này ta sẽ tìm hiểu về các metrics sau:
1. [MSE - Mean Square Error](#first)
2. [RMSE - Root Mean Square Error](#second)
3. [R-Squared](#third)
4. [MAE - Mean Absolute Error](#forth)

và `constant model` của chúng 

> `constant model`: if we have to predict the same value for every object, what value is optimal to predict according to the chosen metric 

có thể hiểu `constant model` là base model của chúng ta, nếu model của chúng ta predict có score dưới score của base model => model chúng ta tệ hơn một model không học gì cả. 

## Notation
![Notation](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/397x234/0544c4c2d5259ca01ddcdc5803253704/notation.png)

## <a id="first"></a> 1. MSE - Mean Square Error 
> MSE calculate square different between the predictions and the target and then average those values over the examples. ![MSE](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/232x72/2931edd551f47c15b9cb67b29b6829d5/mse.png)

Với biểu đồ bên dưới, trục X gồm các predictions (5, 6, 8, 9, 27) và trục Y đại diện cho MSE score. Có thể thấy nếu chỉ được dự đoán một giá trị thì 11 `(Best contant : mean value)` sẽ cho MSE score tốt nhất. [proof](#proof)
![msebestmodel](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/983x392/bc1eb604e8a38de13b2e83ff9aba6976/msebestmodel.png)


## <a id="second"></a> 2. RMSE - Root Mean Square Error
> RMSE is very similar metric to MSE, first, we calculate MSE then we take a squared root of MSE
![RMSE](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/437x106/a6c671958bc456430801fc9b9f99492b/rmse.png)

### MSE vs RMSE
+ Khác biệt: phương trình đạo hàm của hai metric. Có thể thấy đạo hàm của RMSE bằng chính đạo hàm của MSE nhân thêm 1 hằng số 1/2sqrt(MSE). Đối với việc sử một số gradient based method chúng ta cần phải điều chỉnh một số hyperparameter khi thay đổi giữa MSE và RMSE (learning rate là một ví dụ).
![compare](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/577x154/9abff829c85a512ca603fb3572bfbdeb/daohamcompare.png)


## <a id="third"></a> 3. R-Squared 
Giả sử nếu ta nói MSE score của model là 32, RMSE của model là 0.4 liệu chúng ta có biết được model này tốt hay không?

> R2 measure how much our model is better than constant baseline, R2 will give us 0 if we are no better than baseline and 1 if the predictions are perfect.
![R2](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/502x188/6d07a2ffd5acbf5a75f12c3aa85923a2/r2.png)

## <a id="forth"></a> 4. MAE - Mean Absolute Error
> MAE calculate an everage of absolute differences between the target values and the predictions
![mae](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/229x71/05971003e0d1b099b5afbd8f711c5d02/mae.png)

Điều quan trọng ở MAE này là nó không penalize huge error như MSE (`not sensitive to outliers as MSE`)

Với biểu đồ bên dưới, trục X gồm các predictions (5, 6, 8, 9, 27) và trục Y đại diện cho MAE score. Có thể thấy nếu chỉ được dự đoán một giá trị thì 8 `(Best contant : median value)` sẽ cho MAE score tốt nhất. [proof](#proof)
![maebest](https://trello-attachments.s3.amazonaws.com/608a81f5c3b0161441d300ab/965x370/7a0d7e009925af0cb319f2b71c59f311/maebest.png)

### MAE vs MSE
+ Có outliers trong data? -> MAE 
+ Chúng có thật sự là outliers? -> MAE
+ Hoặc chúng là unexpected values mà chúng ta cần để ý? -> MSE 


# Take away
- MSE, RMSE, R-Squared 
    + Giống nhau hoàn toàn về khía cạnh "optimization"
- MAE
    + `Robust` hơn đối với outliers 


# References
+ [1] How to win Data Science Competition: Learn from Top Kaggler - Week 3 - Metric optimization - Regression metrics review I 
+ <a id="proof"></a>[[2] Proof of MSE and MAE constant model](https://github.com/HieuNgoUIT/HieuNgoUIT.github.io/blob/gh-pages/resources/regression/Metrics_video2_constants_for_MSE_and_MAE-Copy2.ipynb)