# covid_19
Covid-19 predictions (March 25th 2020)
(Jupyter notebook, further analyses and discussion will follow soon.)


![Covid-19 predictions](/covid_19_predictions_25_03_2020.png)

Predictions of the number of **confirmed** Covid-19 cases from the
Johns Hopkins CSSE repository (https://github.com/CSSEGISandData/COVID-19) are shown.

The  logistic function in the upper left corner was fit to the Hubei China dataset by minimizing squared deviations. <br/>
It is assumed that the lockdown in China on January 23rd of 2020 was the cause of the logistic evolution of case numbers.

Therefore, the two remaining parameters (L and b) were determined for each country from **hypothetical** counter measure reference dates onwards while fixing k and x0 from the Hubei fit.<br/>

Differences in testing efficiency / testing amount between countries result in different
percentages of missed cases. Therefore, the true number of cases differ from country to country 
and case fatality rates have to be estimated for each country separately:

![Covid-19 case fatality rates](/case_fatality_estimates_for_each_country.png)

Deaths were divided by case numbers a week before since the median time from onset of symptoms to intensive care unit (ICU) admission is around 10 days and the time between symptom onset and death ranged from about 2 weeks to 8 weeks<sup>[1](#source1)</sup>. 

According to these estimates, fatalities could be as high as 50,000 in Spain, 40,000
in New York state, 20,000 in the UK and 6,000 in Germany by the end of April.


Considering the data for **Germany:**

**An adjusted case fatality rate of 1.5% (non-adjusted 6.2% in the Italy dataset<sup>[2](#source2)</sup>) would amount to about 6,000 deaths until the end of April.**

**If 3% (12% in the Italy dataset, 5% in China<sup>[3](#source3)</sup>) of these cases were admitted to the intensive care unit that would amount to 12000 ICU cases.**

<a name="source1">1</a>: https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(20)30195-X/fulltext \
<a name="source2">2</a>: https://www.epicentro.iss.it/coronavirus/bollettino/covid-19-infografica_eng.pdf \
<a name="source3">3</a>: https://jamanetwork.com/journals/jama/fullarticle/2763188
