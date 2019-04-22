# Modeling & Forecasting Canadian National Bankruptcy Rates

> Crystal Sun, Liying Li, Zhi Li, Joy Qi
>
> Report: https://docs.google.com/document/d/15hPVEMnU04mBg2uyZOfCO0Y98mXdxdXSkxpKCCl2k1o/edit?usp=sharing

## Table of Content

- Project Goal
- [Modeling](#Modeling)
- [Froecasting](#Forecasting)

## Project Goal

The goal of this report is to precisely and accurately forecast monthly bankruptcy rates for Canada.

## Modeling




|                            Models                            |    RMSE    | Log-Likelihood |    AIC    |
| :----------------------------------------------------------: | :--------: | :------------: | :-------: |
|                   SARIMA(2,1,1)⨉(2,1,4)12                    |   0.2680   |    368.1910    | -716.3811 |
|               Holt-Winters (ɑ=0.6,β=0.2,γ=0.2)               |   0.2817   |                |           |
| SARIMAX (1,1,2)⨉(3,1,3)12<br />**Exogenous:**<br />Housing Price Index<br />Population<br />Unemployment Rate | **0.1896** |    376.2786    | -726.5573 |
| VAR(p=2)<br />**Endogenous:**<br />Housing Price Index<br />Population<br />Unemployment Rate |   0.2657   |                |           |
| VARX(p=2)<br />**Endogenous:**<br />Housing Price Index<br />UNemployment Rate<br />**Exogenous:**<br />Population |   0.2573   |  

## Forecasting

The predictions of bankruptcy rate are calculated by using the observed housing price index, population, and unemployment rate from January 2015 to December 2017. 

 ![forecasting plot](https://github.com/crystalxs/bankruptcy-rate-prediction/blob/master/Forecasting.jpg)

Our forecasting plot shows that, despite some seasonal fluctuations, there will be a general decreasing trend of the bankruptcy rate for the year 2015 to 2017. 
