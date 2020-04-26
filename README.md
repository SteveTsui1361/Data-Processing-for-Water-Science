# Data Processing for Water Science
 Daily Streamflow Forcasting by First Order Exponential Smoothing Method

## Introduction
Long_term prediction of streamflow is useful for the planning and operation of water resources. Similarly, short-term prediction of 
streamflow is important for managing extreme events and reservoirs. Several approaches exit to predict streamflow time series, such as 
exponential smoothing method, Auto Regressive Integrated Moving Average (ARIMA) model and machine learning tools. This code is to use an 
exponential smoothing model for streamflow forcasting using past streamflow timeseries.

## Processes of the program
* Download USGS streamflow data
  * Imported hydrofunctions are used to build the NWIS url to download the dataset. Here instantaneous data for USGS 03335500 WABASH RIVER
 AT LAFAYETTE, IN for a period of 5 months from 01/01/2019 to 05/31/2019 is downloaded.
  * Then the dataframe is resampled into a timeseries of daily mean streamflow.
* Plot streamflow data
  * Plotting streamflow timeseries for preliminary visualization and checking if there is any missing value.
* Building a first order exponential smoothing model
  * The formula used in this model: <img src="https://render.githubusercontent.com/render/math?math=y_{t}=\alpha y_{t-1}+(1-\alpha)y_{t-1}">
* Plotting ouput from first order model
* Making predictions from first order model
* Defining function to return the error of predictions
