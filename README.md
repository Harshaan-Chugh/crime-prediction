# crime-prediction
Predicting occurrence of Crime in cities and neighborhoods using City crime data 

**Motivation**
- Why is crime a big problem?
- Negatively impacts one’s life and other health outcomes
- Affects innocent people
- Several factors, can increase the rate of crime

**Project Goal**
Predicting crime useful to adjust policing policies, allocate funding for Policies, and in general for city planning.
Our model serves to try to accurately predict crime in the United States

**Data Collection**
* Data From About 200 Cities from publicly available data sources
* Data Collection Features:
- Crime Rate (H: >=40, M, L: <23.80)	
- Race
- Median Household Income
- % Democrats, % Republicans
- Population Density (per mi²)
- Employment Rate
- Education Rate (College)
- Disabilities
- Homelessness Rate (%)
- Police Count Per 10k People
- Average Age
- Stress Score

From sources such as the US Census and other websites. See References below.

**Model Building**


<img width="659" alt="image" src="https://user-images.githubusercontent.com/39035528/188327294-49fc2657-8d51-4901-89e7-9a83f14c75ca.png">


![image](https://user-images.githubusercontent.com/39035528/188327330-f4f0ff23-5858-4ebe-8238-e7fcbce07b1f.png)

**Results**

Accuracy score: 59%
Improvements in progress:
Collecting more data (200-300 more cities)
Feature selection
Different algorithms (XGBoost, neural networks)

After using our model to predict the crime rates for the rest of our data, our model achieved an accuracy of 59%, and we are currently in the process of increasing that value. Due to limited time, our model has lots of factors that have yet to be fine tuned in order to raise our accuracy. First, we can collect more data as we currently only have data for 200 cities and we’re are looking to increase our dataset by at least 200-300 more cities. Also, we can improve our dataset by adjusting our feature selection, which means experimenting with adding different features like high school education, the distribution of different job types, or whether a city’s population has increased or decreased in recent years, to name a few. Finally, we will test our data on different algorithms including XGBoost and neural networks to see if our model can achieve a higher accuracy score. When all this is complete, our model will have a stronger dataset and will be used to predict crime rate for different cities in the US with even greater accuracy.

Here is our current model’s feature importances. These scores are generated based on the importance of each feature in our current model’s prediction process. In the future, after we collect more data, we can use the importance score to give insight on which features we should consider removing or keeping in order to refine our dataset. Currently, our top five features are median household income, the police count per population, the percentage of black population, percentage of the population with disabilities, and the percentage of white population. It’s important to note that the more accurate our model is, the more trustworthy the feature importance scores are, so these scores and the order of importance may change upon future testing.

<img width="250" alt="image" src="https://user-images.githubusercontent.com/39035528/188327398-3c01f9ff-2edb-4849-b066-4a839b0ce146.png">



**Interpretation**

- Meaning of feature importances
- Correlation does not imply causation
- Bias in data
- Historical data → predictions

Here are some other elements to consider while interpreting our model. When interpreting the model’s feature importances, it is important to note that the generated feature importance only scores the correlation or statistical association between features and classification. This correlation does NOT imply that any feature will cause our predicted classification. Also, the general cautioning for machine learning models applies here in that any unintentional bias in the data collected for our model will be reflected in the model and may produce biased results. 

Furthermore, in real world application of our model, there are limitations to our predictions since the historical data we use for prediction are from past years and may not reflect any current changes in society that may affect future crime rate.



**References**


https://wallethub.com/edu/most-least-stressed-cities/22759
https://ballotpedia.org/Largest_cities_in_the_United_States_by_population
https://worldpopulationreview.com/us-cities
https://www.census.gov
https://www.governing.com/archive/police-officers-per-capita-rates-employment-for-city-departments.html
https://www.homelessshelterdirectory.org/
Thoughts on Homelessness in Birmingham – UAB Institute for Human Rights Blog
City leaders, law enforcement working to help with homelessness | rocketcitynow.com
Juneau’s homeless population dips slightly | Juneau Empire
2021 Point in Time Count and Quality By Name List Announcement - Anchorage Coalition to End Homelessness (aceh.org)
Scottsdale's response to homelessness is falling short, some say (azcentral.com)
https://www.eastvalleytribune.com/news/mesa-police-take-new-approach-to-homeless-people-downtown/article_9d02205c-02e2-11e9-b039-873b38005d64.html
https://www.kgun9.com/twoamericas/the-state-of-homelessness-in-arizona-and-pima-county#:~:text=According%20to%20the%20city%20of,3%2C193%20homeless%20people%20in%202020.
https://www.usich.gov/homelessness-statistics/ar/
https://spectrumlocalnews.com/nc/triangle-sandhills/news/2019/10/08/fayetteville-city-council-look-into-housing-for-the-homeless
https://riverviewhopecampus.org/homelessness-in-fort-smith/
https://www.latimes.com/homeless-housing/story/2021-12-01/la-voters-are-frustrated-impatient-over-persistent-homelessness-crisis
https://www.koaa.com/news/covering-colorado/updated-homeless-population-estimate-released#:~:text=In%202020%2C%20that%20population%20was,population%20was%20based%20on%20safety.
https://kdvr.com/news/problem-solvers/homeless-population-growing-in-aurora-mayor-plans-to-reintroduce-camping-ban/#:~:text=A%20city%20survey%20found%20Aurora%20has%20nearly%20600%20homeless%20people.
https://fortcollinsrescuemission.org/what-we-do/homelessness-in-our-city/

https://www.presstelegram.com/2022/01/13/long-beach-announces-new-date-for-homeless-count/
https://harivco.org/ContinuumofCareDivision/HomelessPointInTime(PIT)Count/tabid/268/Default.aspx#:~:text=During%20the%202020%20count%2C%202%2C884,unsheltered%20and%20729%20were%20sheltered.
https://en.wikipedia.org/wiki/Chula_Vista,_California#:~:text=In%202016%2C%20it%20was%20estimated,homeless%20individuals%20in%20Chula%20Vista.
https://www.fremont.gov/DocumentCenter/View/41835/Homeless-Newsletter
https://sanjosespotlight.com/why-cant-san-jose-solve-its-homelessness-crisis/#:~:text=The%20number%20of%20unhoused%20residents,hit%20close%20to%207%2C000%20people.
https://californiaglobe.com/articles/sacramentos-solutions-and-pending-are-growing-homeless-population/
https://www.sfchronicle.com/sf/article/How-many-homeless-people-are-in-S-F-A-night-16944970.php
https://www.turnto23.com/news/local-news/kern-county-unveils-plan-to-reduce-homelessness#:~:text=BAKERSFIELD%2C%20Calif.,experiencing%20homelessness%20in%20Kern%20County.
https://newsantaana.com/the-santa-ana-city-managers-latest-homelessness-update-noted-that-there-were-81-arrests-citations-in-nov/#:~:text=In%202019%20the%20Point%2Din,in%20November%20of%20this%20year.
https://www.pe.com/2020/05/06/riverside-countys-homeless-population-climbs-5/
http://www.laalmanac.com/social/so14b.php
https://www.modbee.com/news/local/article254787527.html
https://www.sbsun.com/2022/02/24/volunteers-survey-count-san-bernardino-countys-homeless-population/#:~:text=In%202020%2C%20San%20Bernardino%20County,sleeping%20accommodation%2C%20and%20735%20sheltered.
https://calmatters.org/california-divide/2022/01/fresno-homelessness/
https://voiceofoc.org/2020/02/anaheim-poised-to-expand-salvation-army-homeless-shelter/
https://www.sfchronicle.com/projects/2021/homeless-project-oakland/#:~:text=The%20last%20biennial%20homeless%20count,jump%20in%20the%20Bay%20Area.
https://www.city-data.com
https://www.bestplaces.net/
https://www.denverpost.com/2022/01/21/denver-homeless-population-count-2021/#:~:text=There%20were%202%2C530%20people%20in,Denver%20area%2C%20service%20providers%20say.
