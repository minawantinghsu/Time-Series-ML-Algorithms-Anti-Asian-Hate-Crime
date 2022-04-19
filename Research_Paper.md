The Outbreak of Covid-19 to Anti-Asian Crime Rate

Executive Summary

As Covid-19 proliferated across the United States, we have constantly heard on the news that Asians are becoming the new target for criminal attacks. The Federal Bureau of Investigation even warned that a surge in anti-Asian crime was expected at the start of the Covid outbreak in the US (BBC, 2021). Multiple sources indicate that recent violent attacks on Asian Americans are related to Asians being blamed for the spread of Covid-19. However, the act of “Covid Crime” has pointed out a notion that “anti-Asian hate isn't’ new”, but something being exacerbated (Laura, 2021). Pandemic-related health crises have always been stigmatized by the othering of people; individual and institutional-level racism and xenophobia have operated throughout history. For example, since the late 1700s, Asian Americans have experienced a certain level of racial bias and verbal or physical attacks (Angela, Shannon & Lynn, 2020). To know whether the Covid outbreak in the US has changed the state of the crime scene, we focus on crime data in New York and set days before March 2020 as pre-pandemic crime data and days after as post-pandemic crime data. 
This research aims to clarify if the Covid-19 event changed the anti-Asian crime rate in New York throughout the period. To achieve this, we categorize the NYPD reported crime dataset into Asian and non-Asian subtypes and conduct exploratory data analysis, correlation analysis, time series, and Bayesian Structural Time Series (BSTS) to forecast the anti-Asian crime rate. Victims of the Asian / Pacific Asian race are all grouped into the anti-Asian crime dataset. From the scatter plot and correlation analysis, we see a positive relationship between the Asian and Non-Asian crime groups. The number of anti-Asian crimes shares a linear relationship with the number of crimes of all as well. We use BSTS to forecast a predictive 22 months anti-Asian crime rate based on pre-pandemic anti-Asian crime data. Based on the two-sample t-test, it's statistical significance to state a difference between the predicted anti-Asian crime rate and the actual anti-Asian crime rate. That is, Covid-19 did impact the state of crime scenes. 


Statement of the Problem & Research Questions 

The main research question of this paper is, in terms of proportion, whether the outbreak of Covid-19 has led to a change in the number of anti-Asian crimes than anti-other races crimes. Since the epidemic is likely to increase the number of all types of crime, looking at the change in the number of anti-Asian crimes is not convincing enough to justify the unprecedented increase in anti-Asian crimes. Therefore, we use the percentage of anti-Asian crime, calculated by the ratio of the number of anti-Asian crime cases to the total number of crimes, as the parameter to indicate the change.
Using data points from the past 10 years, we trained our BSTS model to predict the ratios for the 22 months after the outbreak of covid in March 2020. By comparing the predicted crime ratios and the actual crime ratios, we hope to examine the significance of differences between the two and conclude the effect of covid on anti-Asian crimes.
The null hypothesis is that the predicted ratio is equal to the actual ratio, while the alternative hypothesis is that the predicted ratio is not equal to the actual ratio. The ratio is calculated by dividing anti-Asian crimes by the total number of crimes. Here Y1 hat represents the monthly ratio during the Covid-19 period predicted based on the data of the pre-Covid-19 period, and Y1 represents the real ratio calculated by the real data. 
H0: E(Y1) - E(Y1^) = 0
HA: E(Y1) - E(Y1^) ≠ 0
If the null hypothesis is rejected, which means that there is a true difference between the mean of Y1 hat and the mean of Y1, we should say that Covid-19 influenced the ratio of Asian crimes within New York City. Then, we could conclude that the covid-19 causes the anti-Asian crimes to grow at a faster rate.


Literature review

In December 2019, a new variant of the Sars-Coronavirus was detected in Wuhan, China. Two months after the initial outbreak of the virus, Covid-19 was found in 136 countries around the globe. The United States had its first Covid-19 case on January 20, 2020, and in a short span of two months, on March 27th, 2020, it overtook China and became the country with the most infected cases in the world. As the virus continues to rampage in the states, social problems arise as reports of hate crimes targeting Asians have increased. Reports of Asians suffering from racial slurs, workplace termination, wrongful evictions, physical violence, harassment, and homicide can be seen across the country. 
In our study, we first examine whether the “Asian targeted” rate increases with the rise of Covid-19 cases in America. Though it is widely acknowledged that anti-Asian crimes are more frequently reported on the news, some might argue that it would be the result of biased reporting by the media. This perspective suggests that all crime rates increase due to the disturbed economy and various levels of lockdowns and that anti-Asian hate crimes increase only to the same ratio as other ethnic groups. Our goal is to test this argument and study the relationship between anti-Asian hate crimes in New York City and the respective Covid-19 cases.
What’s more, this study dives into the relationship between Asian animus and social media usage. The increase in anti-Asian violence is not the product of Covid-19 alone. Online sentiment towards Asians (especially Chinese) exasperated dramatically on social media like Twitter, Instagram, and Facebook. A finding from a research paper done by Massey University suggests that “the more a social media user believes their most-used daily social media is fair, accurate, present the facts, and is concerned about the public (social media believe), the more likely that user is to believe Chinese pose a realistic and symbolic threat to America.” (Croucher) Political representatives also played a big part in shaping the consensus when Trump repeatedly took the anti-China stance, as research done by Runjing Lu and Yanying Sheng indicates that “this racial animus is stronger on days when the connection is more salient, as proxied by President Trump's tweets mention China and Covid-19 at the same time.” (Lu)
From 2019 to 2020, the bias motivation from race/ ethnicity/ ancestry of hate crime has almost risen by 32%. (Department of Justice, 2020) To investigate if Covid-19 caused the overall national insecurity, general xenophobia toward people of different races, and dissimilar language, we examine the standardized mean difference between anti-Asian and anti-non-Asian crime rates. 


Data Descriptions 

The dataset used in this study is a criminal record from NYC Open Data. It included the dates, crime types, and the number of crimes in New York City in the 12 years following March 2010, spanning before and after the pandemic. 
Specifically, the dataset includes two time-related variables, record-created date and arrest date. These two-time records are usually not consistent, which means compared to the record-created date, the arrest date often has a lag. In general, criminals don’t usually get arrested on the same day; it takes the police a period to solve. And for some cases, there may only be a record creation date, and no error date since not all cases will be resolved so that the record creation date is more comprehensive and complete. Therefore, we use the record creation date as the time reference in this study.
Besides, the variable County records the area where each crime occurred, such as KINGS and BLOOMS. The regional data can help understand the geographic distribution of crimes. In addition to time-and region-related data, another major data category in the second data set is the description of the criminal process and the type of case, including compact precinct, patrol borough, bias motive description, and offer category.
This original data set was divided into two parts, the before-Covid-19 period from March 2010 to March 2020 and the Covid-19 period from March 2020 to March 2022. The data from the before-Covid-19 period are used as a historical data set to determine the relationship between the number of anti-Asian crimes and the number of all kinds of crimes. We then use the found relationship to predict the percentage of anti-Asian crimes during the after-Covid-19 period.


Analytical Techniques

Using the data from the pre-Covid-19 period (from March 2010 to March 2020), we first built up a simple linear regression model (lm1) to calculate the correlations between the cases count of anti-Asian crimes and the cases count of the crimes towards all other races. The regression summary indicates that the number of anti-Asian crimes is significantly correlated to the number of crimes targeting all other races.

lm1: Linear Regression Model between the cases count of anti-Asian crime to cases count of all other races crime, March 2010 - March 2021

Another linear regression model (lm2) was built to prove further the significant correlation between the number of anti-Asian crimes and the sum of all other crimes to find out the specific value of the correlation. The statistical results prove that the cases count of anti-Asian crimes (the independent variable) is significantly and positively correlated with the cases count of all crimes (the dependent variable) under the 99% confidence level (with a p-value of 0.00237). Based on this proven correlation, we intend to use this correlation to predict the percentage of anti-Asian crime in the after-Covid-19 period (from March 2020 to March 2022).
 
lm2:. Linear Regression Model between the cases count of anti-Asian crime to sum of all crime, March 2010 - March 2021

After confirming the linear correlation between anti-Asian crimes and anti-other races crimes, we decided to use the percentage of anti-Asian crimes as the parameter. A BSTS model was then built using the past 10 years of crime data to predict the estimated anti-Asian crime percentage for the months after Covid-19 had occurred. Since our dataset covers crime data all the way to December 2021, we can calculate the actual percentages of anti-Asian crime for each month.
Graph 1 presents the predicted range for the percentages of anti-Asian crimes using confidence bound of 95%. This graph includes the actual anti-Asian percentages along with a 22-months prediction.
 
Graph1. Predicted range for the percentages of anti-Asian crimes, 2015 - 2022

A closer illustration of the predictions is then taken out and shown in Graph 2.  

Graph2. Predicted range for the percentages of anti-Asian crimes, 2020 - 2022

Plotting the actual percentage of anti-Asian crimes in Graph 3.

Graph3. Actual percentage of anti-Asian crimes, March 2020 - December 2021

Finally, we overlap the prediction and the actual percentages in Graph 4.

Graph 4. Predicted and actual percentages of anti-Asian crimes, March 2021 - December 2021

We can see from Graph 4 that the actual anti-Asain crime percentage was higher than the predicted percentages during the summer of 2020 and continues to be higher after November 2020. In order to test this observation, we conducted a two-sample t-test to analyze whether there is a significant difference between the mean of real percentage and the mean of predicted percentage. The t-test indicates that there is a significant difference between the two means with 95% confidence bounds. Hence, we conclude that Covid-19 has led to an increase in the number of crimes against Asians faster than that of other races.

Graph5.  Results of two-sample t-test for difference between the mean of actual and predicted percentage


Conclusion & Recommendations 

BSTS approach can better handle uncertainty and incorporate outside information into relationships. The predictive crime rate falls within the confidence interval, indicating a valid forecast. Statistical testing is used to validate if there's a statistical difference between predictive anti-Asian crime and actual anti-Asian crime. Since the p-value is less than the significance level, we can conclude that the spread of Covid-19 does cause the change in anti-Asian crime. But there are a few limitations to such results:  First of all, the amount of information (time period) given for predictive crime may be limited. Additionally, the rise of anti-Asian crime may be caused by other omitted variables like Trump winning the election and the stir-up of nationalism and xenophobia from the majority race. That is, the period used for predictions may be irrelevant to forecasting the future. 
The research supports the statement that the outburst of Covid-19 has caused the rise in the anti-Asian crime rate. The phrase like 'Chinese virus' only exacerbated socially entrenched racism and xenophobia, making Asian Americans more vulnerable to racial aggression. Studies also show that failure to fully investigate and adjudicate hate crime might cause the continually rampant hate crime (The City, 2022). There’s an apparent gap between punishing hate crimes in political or legal rhetoric and juridical conviction. The traditional way of over heavily relying on law enforcement cannot address the potential prosecution of hate crimes (Stanford Law School, Brennan Center for Justice, 2020). To fundamentally eradicate the harm and fear grappling across communities caused by bias-motivated violence (Alexandra & Daniel, 2021), the government should work on social, economic, and educational interventions such as restorative justice programs and social services support. Restorative justice programs can help identify and mend individual and community harms caused by hate crimes. At the same time, social support services can provide compensation and professional or mental health support to the harmed. 





















References
AAPI Equity Alliance. (n.d.). Stop AAPI Hate. Retrieved March 2, 2022, from https://stopaapihate.org/stop-aapi-hate-national-report-2/ 
BBC. (2021, May 21). Covid 'hate crimes' against Asian Americans on rise. Retrieved March 2, 2022, from https://www.bbc.com/news/world-us-canada-56218684 
Coronavirus disease 2019 (covid-19) - who. (n.d.). Retrieved March 4, 2022, from https://www.who.int/docs/default-source/coronaviruse/situation-reports/20200327-sitrep-67-covid-19.pdf  
Croucher, S. M., Nguyen, T., & Rahmani, D. (1AD, January 1). Prejudice toward Asian Americans in the COVID-19 pandemic: The effects of social media use in the United States. Frontiers. Retrieved March 3, 2022, from https://www.frontiersin.org/articles/10.3389/fcomm.2020.00039/full 
Gonen, Y., Aponte C. I., & Bhat S. (2022, March 6). Most Hate Crime Charges in NYC Get Dropped Before Conviction, Stats Show. The City. Retrieved April 14, 2022, from https://www.thecity.nyc/2022/3/6/22964719/hate-crime-nyc-dropped-before-conviction
Gover, A. R., Harper, S. B., & Langton, L.. (2020, July 7). Anti-Asian Hate Crime During the COVID-19 Pandemic: Exploring the Reproduction of Inequality. National Library of Medicine. Retrieved April 15, 2022, from https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7364747/ 
Larsen L., (2016, April 21). Sorry ARIMA, but I’m Going Bayesian. MultiThreaded. Retrieved April 14, 2022, from https://multithreaded.stitchfix.com/blog/2016/04/21/forget-arima/
Lu, R., & Sheng, Y. (2020, July 3). From fear to hate: How the covid-19 pandemic sparks racial animus in the United States. arXiv.org. Retrieved March 3, 2022, from https://arxiv.org/abs/2007.01448

Petri, A. E., & Slotnik, D. E. (2021, October 15). Attacks on Asian-Americans in New York Stoke Fear, Anxiety and Anger. New York Times. Retrieved April 15, 2022, from  https://www.nytimes.com/2021/02/26/nyregion/asian-hate-crimes-attacks-ny.html 
Stanford Law School & Brennan Center for Justice. (June, 2021). Exploring Alternative Approaches to Hate Crime.
U.S. Department of Justice. (n.d.). FBI Releases 2020 Hate Crime Statistics.  https://www.justice.gov/hatecrimes/hate-crime-statistics
Zornosa, L. (2021, October, 26). A Playwright Has a Message: Anti-Asian Hate Isn' t New. The New York Times. Retrieved March 2, 2022, from https://www.nytimes.com/2021/10/26/theater/covid-crime-stop-asian-hate.html 
