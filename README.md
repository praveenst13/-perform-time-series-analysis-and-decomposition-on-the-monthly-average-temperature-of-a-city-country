# Time series analysis and decomposition on the monthly average temperature of a city/country 

## AIM:
To Write a Program to time series analysis and decomposition on the monthly average temperature of a city/country 

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Procedure:


## Program:
```
/*
To Write a Program to time series analysis and decomposition on the monthly average temperature of a city/country 
Developed by: Praveen s
RegisterNumber:  212222240077
*/
import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose
data =pd.read_csv("/content/temperatures.csv",parse_dates=["YEAR"])
data.head()

data.set_index("YEAR",inplace=True)
data.index=pd.to_datetime(data.index)

data.dropna(inplace=True)
data.plot()

result=seasonal_decompose(data["ANNUAL"],model="multiplicable",period=12)

result.seasonal.plot()

result.trend.plot()

result.plot()
```
## Output:
### data.head()
![s1](https://github.com/praveenst13/-perform-time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/118787793/9611d5be-5ea5-4ddd-be74-dbcd7a4a7dbc)


### data.plot()

![s2](https://github.com/praveenst13/-perform-time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/118787793/5bcf5dc7-53d1-4cb6-b010-22e9940c62d3)
### result.seasonal.plot()
![s3](https://github.com/praveenst13/-perform-time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/118787793/a15d8391-c63f-4d81-a84b-78de8fa21f39)

### result.trend.plot()

![s4](https://github.com/praveenst13/-perform-time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/118787793/7cd52086-4702-425e-95a9-5fe48a01f57b)
### result.plot()
![s5](https://github.com/praveenst13/-perform-time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/118787793/855e6de5-a200-4b67-ab72-c1bff2bda08a)



## Result:
Thus the program to  time series analysis and decomposition on the monthly average temperature of a city/country  is written and verified using python programming.
