# Macroeconometrics-Money-Demand-estimation

Macroeconometrics-Money-Demand-Estimation
This project employs advanced macroeconometric techniques to estimate the Money Demand in Argentina using Vector Error Correction Models (VECM).

Table of Contents
Objectives

Estimation

Metrics

Results

Prediction

Objectives
The purpose of this project is to analyze the Money Demand for Argentina during the period 1997-2023, particularly to estimate the elasticity to GDP, the interest rate, and the effect of expectations about exchange rate devaluation on Money Demand. In order to advance the analysis, it will apply a Vector Error Correction Model (VECM) and a Markov-Switching model following the Gibbs Sampling strategy.

Estimation Strategy:
First step: We calculate a multivariate regression with OLS to estimate the real exchange rate as a response to fundamental economic variables such as Expenditures/GDP, Debt/GDP, Productivity, and foreign price indices.

![image](https://github.com/user-attachments/assets/4e4a14f8-0e0f-4280-be1a-ea3d6f871b07)

Next, we estimate the linear projection on trend values regarding fundamental variables. We take the trend values applying the Hodrick-Prescott filter.
![image](https://github.com/user-attachments/assets/10e699d9-85f1-4222-b6b2-35e7e537c9dc)

So, we can identify the observed real exchange rate and equilibrium exchange rate estimated upon the fundamental variables in their trend values, getting the Dev variable as the difference between the equilibrium exchange rate and the observable values.

![image](https://github.com/user-attachments/assets/13d1f34a-8c1e-45cd-83d8-bd41514118ca)

![image](https://github.com/user-attachments/assets/9cd79c8b-91c9-4795-8f20-8bcaaf3d20ce)

Second step: Estimating a VECM to predict the long-term relation among variables. Previously, we identify the integration order and the Johansen test supports the hypothesis of 1 cointegration relation.

![image](https://github.com/user-attachments/assets/5b1222c0-fc9d-4152-9403-e3a0ad723ba5)

![image](https://github.com/user-attachments/assets/deba6fad-a969-4c7a-9ec7-c1c65651b4ee)

Impulse Responses and Variance Decomposition:

![image](https://github.com/user-attachments/assets/b85a5e68-9e20-4bce-ba1c-d83ebbccb26f)


In order to make inferences about the contribution of different variables to money demand, we estimate the impulse-responses following different Cholesky orders.

![image](https://github.com/user-attachments/assets/7bee57b1-f1e1-4a73-b776-d27fdf7d47af)

Variance Decomposition

![image](https://github.com/user-attachments/assets/f04f1bf8-d7cc-40f7-882d-55bb7c59e4fc)

Conclusion

The impulse response analysis predicts a negative reaction between the expected exchange rate and Money Demand, aligning with economic theory. Additionally, the relationship between the interest rate and GDP follows the traditional pathway with respect to Money Demand. Finally, the variance decomposition reveals that the exchange rate expectation is the most significant predictor of Money Demand behavior.
