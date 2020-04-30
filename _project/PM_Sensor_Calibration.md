---
title: "Evaluation and calibration of a low-cost particle sensor"
excerpt: "Evaluation and calibration of a low-cost particle sensor in ambient conditions using machine-learning methods"
classes: wide
tags: 
  - Air quality monitoring
  - PM2.5 monitoting
  - Machine Learning
  - Neural Network
  - XGBoost
---

Particle sensing technology has shown great potential for monitoring particulate matter (PM) with very few temporal and spatial restrictions because of its low cost, compact size, and easy operation. However, the performance of low-cost sensors for PM monitoring in ambient conditions has not been thoroughly evaluated. Monitoring results by low-cost sensors are often questionable. In this study, a low-cost fine particle monitor (Plantower PMS 5003) was colocated with a reference instrument, the Synchronized Hybrid Ambient Real-time Particulate (SHARP) monitor, at the Calgary Varsity air monitoring station from December 2018 to April 2019. The study evaluated the performance of this low-cost PM sensor in ambient conditions and calibrated its readings using simple linear regression (SLR), multiple linear regression (MLR), and two more powerful machine-learning algorithms using random search techniques for the best model architectures. The two machine-learning algorithms are XGBoost and a feedforward neural network (NN). Field evaluation showed that the Pearson correlation (r) between the low-cost sensor and the SHARP instrument was 0.78. The Fligner and Killeen (F–K) test indicated a statistically significant difference between the variances of the PM2.5 values by the low-cost sensor and the SHARP instrument. Large overestimations by the low-cost sensor before calibration were observed in the field and were believed to be caused by the variation of ambient relative humidity. The root mean square error (RMSE) was 9.93 when comparing the low-cost sensor with the SHARP instrument. The calibration by the feedforward NN had the smallest RMSE of 3.91 in the test dataset compared to the calibrations by SLR (4.91), MLR (4.65), and XGBoost (4.19). After calibrations, the F–K test using the test dataset showed that the variances of the PM2.5 values by the NN, XGBoost, and the reference method were not statistically significantly different. From this study, we conclude that a feedforward NN is a promising method to address the poor performance of low-cost sensors for PM2.5 monitoring. In addition, the random search method for hyperparameters was demonstrated to be an efficient approach for selecting the best model structure.

Check out the full paper at [*Atmospheric Measurement Techniques*](https://www.atmos-meas-tech.net/13/1693/2020/) <https://www.atmos-meas-tech.net/13/1693/2020/>