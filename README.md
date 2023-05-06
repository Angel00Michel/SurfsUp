# SurfsUp
Python / Pandas / SQLAlchemy

# Overview

In this analysis, the temperature data that accrued for the months of June and December were retrieved from Oahu, Hawaii. This data was pulled for the purpose of a surf and an ice cream shop, in hopes to see if their business models were sustainable year round. 

# Results

The June temparature statistics are as followed:

- A mean temperature of 75 degrees, with a minimum temperature of 64 degrees; with a maximum temperature of 85 degrees.
- The temperature is above 73 degrees 75% of the time.
- The standard deviation is only 3.25 degrees from the mean. 

![image](https://user-images.githubusercontent.com/106771574/236650781-e6fb1960-7331-4521-8b89-fad8194f38ad.png)

The December temparatures statistics are as followed based on our data:

- A mean temperature of 71 degrees, with a minimum temperature of 56 degrees; with a maximum temperature of 83 degrees.
- The temperature is above 69 degrees 75% of the time.
- The standard deviation is only 3.75 degrees from the mean. 

![image](https://user-images.githubusercontent.com/106771574/236650810-14c34f1c-1708-43a6-becf-728056a7f32c.png)

# Summary

Based on this model, the temperatures represented in June and December are usually above 70 degrees. They are very similar with a much hotter month in June. In conclusion, the ice cream shop business would be more sustainable year round.

Extension for seperate analysis to determine more of an accurate depiction... 2 queries related to precipitation would gather more weather data for June and December. The query for the June dataset for precipitation, is down below.

*from sqlalchemy import extract June_Month_Prec = session.query(Measurement.date,Measurement.prcp).filter(extract('month', Measurement.date)==6).all() June_Month_Prec prec_df = pd.DataFrame(June_Month_Prec, columns=['date','June Prec']) prec_df.set_index(prec_df['date'], inplace=True) prec_df = prec_df.sort_index() prec_df.head(5) prec_df.describe()*

This is similar for the December query for precipitation, which is down below. 

![image](https://user-images.githubusercontent.com/106771574/236650970-a0ff1fad-1606-43c1-b3cc-3c1beddb3bde.png)

![image](https://user-images.githubusercontent.com/106771574/236650971-8496e82a-b0f6-4d5e-9b2c-8cf6a5cbda70.png)

We are now able to conclude there will be more rainfall in December than June.



