---
title: "PEMS for a Steam Generator"
excerpt: "Development of a predictive emissions model using a gradient boosting machine learning method"
classes: wide
tags: 
  - PEMS
  - NOx monitoting
  - XGBoost
  - Gradient Boosting
---

Predictive emissions monitoring systems (PEMSs) are alternatives to continuous emissions monitoring systems (CEMSs) for monitoring air pollutants, such as NOx. Existing PEMSs and related research have focused on applying artificial neural network (ANN) algorithms. However, ANN-based models are treated as “black boxes”. Regulators and decision makers without a statistical background often have difficulty understanding these models, which poses a significant challenge for a broader application of PEMSs. In this study, we proposed a tree-based ensemble method with gradient boosting techniques for PEMS development. Compared to ANNs, tree-based methods are easier to understand and require less effort to preprocess data, fewer hyperparameters for model tuning, and less time for model training. We developed a predictive model using a gradient boosting machine learning library called XGBoost to monitor NOx emissions from a boiler located in Alberta, Canada. The model uses five process parameters as inputs and the predicted NOx emissions as output. We trained the model with 202,047 samples using random search methods to determine the best model and tested the model with 50,512 samples. We evaluated the test results against US EPA PEMS standards. The model passed all the statistical tests for precision outlined by US EPA Performance Specification 16. The Pearson correlation r value was 0.98 between the XGBoost-predicted NOx values and the CEMS-measured NOx values. The RMSE was 0.14, and the MAE was 0.09. We conclude that XGBoost is a good option for developing PEMSs. Facility operators can use the method provided in this study to develop PEMSs by themselves using the open-source library XGBoost at no cost.

Check out the full paper at [*Environmental Technology & Innovation*](https://www.sciencedirect.com/science/article/abs/pii/S2352186420313286) <https://www.sciencedirect.com/science/article/abs/pii/S2352186420313286> [Download Preprint](./assets/files/PEMS_XGBoost_ETI.pdf)