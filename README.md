# Predicting-COVID19-Active-Cases-
I developed this model along with Khusbhu Jayesh kumar Mewada under the guidance Dr. K.P. Singh (Professor Of Machine Learning IIITA) for forecasting the number of active cases in India and different states of India.

#### Abstract
The current research proposes a model to predict the number of people that may be affected, the peak
period and the halt time for the coronavirus pandemic outbreak worldwide. Here, we apply Machine
learning models to predict aforementioned predictions. We use the statistical data generated from
countries, namely India, Spain and South Korea and we also use the statistical data from some of
the Indian states for prediction purposes in order to get some meaningful insights from our analysis.

#### Introduction
Coronaviruses are a large family of viruses which may cause illness in animals or humans. In
humans, several coronaviruses are known to cause respiratory infections ranging from the common
cold to more severe diseases such as Middle East Respiratory Syndrome (MERS) and Severe Acute
Respiratory Syndrome (SARS). The most recently discovered coronavirus causes coronavirus disease
COVID-19.
![COVID19 Virus Image](https://github.com/shivamkasat/Predicting-COVID19-Active-Cases-/blob/master/ProjectDetails/corona_0.jpeg?raw=true)

COVID-19 is the infectious disease caused by the most recently discovered coronavirus. This newvirus and disease were unknown before the outbreak began in Wuhan, China, in December 2019.<br />
The first case of 2019-2020 coronavirus pandemic in India was reported on 30th January, 2020,
Originating from China. Experts suggest the number of infections could be much higher as India’s
testing rates are among the lowest in the world. The infection rate of COVID-19 in India is reported
to be 1.7, significantly lower than in the worst affected countries.

#### Symptoms of Coronavirus
![COVID19 Symtoms Image](https://github.com/shivamkasat/Predicting-COVID19-Active-Cases-/blob/master/ProjectDetails/corona_1_symptoms.png?raw=true)
The above graph represents the probability of having corona positive given the symptom. e.g., There
is 67.7% probability for a person to be tested positive given he has dry cough as a symptom.

#### Datasets
We have used multiple dataset for our analysis and prediction task, which were taken from kaggle.com
1. ##### COVID19 GLOBAL Forecast
    The White House Office of Science and Technology Policy (OSTP) pulled together a coalition research groups and companies (including Kaggle) to prepare the COVID-19 Open Research Dataset (CORD-19) to attempt to address key open scientific questions on COVID-19.
    Those questions are drawn from National Academies of Sciences, Engineering, and Medicine’s
    (NASEM) and the World Health Organization (WHO).<br />
    It has six columns named Id, Province state, Country Region, Date, Confirmed Cases, Fatalities. <br /> 
    They are currently updating the data daily.
2. ##### COVID-19 in India
    This dataset has information from the states and union territories of India at daily level.
    State level data comes from Ministry of Health & Family Welfare. Individual level data comes
    from covid19india. <br />
    * COVID-19 cases at daily level is present in covid 19 india.csv file.
    * Individual level details are present in IndividualDetails.csv file.
    * Population at state level is present in population india census2011.csv file.
    * Number of COVID-19 tests at daily level in ICMRTestingDetails.csv file.
    * Number of hospital beds in each state in present in HospitalBedsIndia.csv file.

3. ##### Novel Corona Virus 2019 Dataset
    This dataset has daily level information on the number of affected cases, deaths and recovery from 2019 novel coronavirus. Please note that this is a time series data and so the number of 
    cases on any given day is the cumulative number.
    Main file in this dataset is covid_19_data.csv and the detailed descriptions are below
    * Sno - Serial number
    * ObservationDate - Date of the observation in MM/DD/YYYY
    * Province/State - Province or state of the observation (Could be empty when missing)
    * Country/Region - Country of observation
    * Last Update - Time in UTC at which the row is updated for the given province or country.
    * Confirmed - Cumulative number of confirmed cases till that date
    * Deaths - Cumulative number of of deaths till that date
    * Recovered - Cumulative number of recovered cases till that date
#### Exploratory Data Analysis (EDA)
 ##### EDA on COVID19 GLOBAL Forecast dataset
 The dataset covers 163 countries and almost 2 full months from 2020, which is enough data toget some clues about the pandemic. We will see a few plots of the worldwide tendency to see if we can extract some insights: <br />   
 
 ![Global Conifirmed Cases](https://github.com/shivamkasat/Predicting-COVID19-Active-Cases-/blob/master/ProjectDetails/corona_2_global_cases.png?raw=true)

#### Observation

We can see that the global curve shows rich fine structure, but these numbers are strongly affected by the vector zero country, China.  Given that COVID-19 started there, during the initial expansion of the virus there was no reliable information about the real infected cases.
  
  * Both Italy and Spain are experiencing the larger increase in COVID-19 positives in Europe. At the same time, UK is a unique case        given that it’s one of the most important countries in Europe but recently has left the European Union. The fourth country we have      taken is Singapore, since it is closer to China and its socio-economic conditions is different from the other three countries.
    
    ![Analysis output of different countries](https://github.com/shivamkasat/Predicting-COVID19-Active-Cases-/blob/master/ProjectDetails/corona_3_countries.png?raw=true)
    ![Comparative Analysis of different countries](https://github.com/shivamkasat/Predicting-COVID19-Active-Cases-/blob/master/ProjectDetails/corona_4_countries.png?raw=true)

* ###### Italy
    With almost 120,000 confirmed cases, Italy shows one of the most alarming scenarios of COVID-19 with more than 2% of population has     been infected.

* ###### Spain
    Spain has the same number of cumulative infected cases as Italy, near 120,000. However, Spain’s total population is lower (around 42     millions) and hence the percentage of
    population that has been infected rises up to 3%.

* ###### United Kingdom
    Despite not being very far from them, the UK shows less cases. The number of cases is around 40.000, this is, a 0.6% of the total       population.

* ###### Singapore
    Singapore is relatively isolated given that is an island, and the number of international travels is lower than for the other 3         countries. The number of cases is still very low (1000)
    with 0.2% of population being infected.


