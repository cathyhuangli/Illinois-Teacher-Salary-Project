# Capstone Project

## Illinois Public School Teacher Salary Prediction & Fairness Assessment
Group Members: Lukasz Filipek, Ki Young Han, Li Huang, Robin Wilcox

Salary across genders appears to be a topic of great interest and controversy recently.  We see examples such as Google analyzing salaries paying out $9.7million, to even the playing field, of additional compensation to 10,677 employees where a higher percentage of the money went to men.  If Google found something interesting in their dataset of candidates, it is compelling to analyze other datasets containing salary information for inequity.  What makes such an analysis interesting, yet challenging, is that inequity itself is not necessarily anything meaningful, and that is why an analysis has to take into consideration any variable available to make sure one is comparing like populations and isolating only one variable, in this case, gender and ethnicity.

## Models Construction
We constructed 7 different models to predict salary within a ten year Illinois public school dataset.  Our best model uses XGBoost algorithm and is able to predict within $7,000 88% of the time.  Predictability results within different slices of the data is below.  We obtain the best predictability outside Chicago, among middle & high school teachers,  and among female teachers with bachelor degrees, and least predictability inside Chicago, among elementary & special education teachers, and among teachers with graduate degrees.

Models Constructed
![models](https://github.com/cathyhuangli/Illinois-Teacher-Salary-Project/blob/master/models.png)



Predictability by Data Slices using our best Model XGBoost.  Scored using Root Mean Squared Error.
![predictability](https://github.com/cathyhuangli/Illinois-Teacher-Salary-Project/blob/master/Predictability.png)

## Assessment of Fairness

While we did assess fairness, we must present our findings with a few words of caution.  There is not necessarily one story to take away from this analysis.  When looking at a dataset, one must be careful not to draw premature conclusions.  With a different set of filters, one may draw different conclusions.  To analyze fairness, we filtered the dataset to include only full time teachers, percent employed 100%, full time equivalent 100%, working exactly 9 months.  We evaluated the data using our most important variables, years of experience, advanced degree (binary - teacher has one or does not), and year.  We explored variables where fairness was most interesting, namely, gender, race, location, and teaching position (elementary school, middle school, high school and special education teachers).  

Middle School teachers starting salary was higher than elementary school teachers and high school teachers in 2003, but incurred the slowest growth as years of experience increased.  In 2004 through the remaining years in the dataset, Middle School teachers starting salary was lowest of the four positions, and remained the lowest salary with increasing years of experience.

In **2003**, the starting average salary among male teachers was within $1k-4k higher than female teachers, with the exception of high school teachers with a bachelor degree.  The starting salary gap varied across positions, with the largest discrepancies occurring among Elementary and Special Ed teachers.  By 2012, there is no discrepancy across genders among teachers with a bachelor degree, but a gender salary gap continues to exist for teachers with a graduate degree (males still earning more).  In 2012, salaries among males with a graduate degree increases faster than females with a graduate degree, with the exception of high school teachers.  A salary gap also widens with increase in years of experience for Special Ed teachers with a bachelor degree.  The largest salary gap discrepancy across genders exists among Special Ed teachers.

In **2003**, the overall starting salary among race Black females was $2.5k more than race Black males, which is an exception to all other gender slices of data we explored.  In 2012, this gap has widened, with race Black females earning $5k more than race Black males. 

In **2009**, the US experienced an economic recession, which resulted in decreased average salary for all races except White and Native American.  The most significant decrease was among Junior High school teachers, and teachers of race Black.  However, teachers of race Black still maintained the highest average salary.  While we do see an overall salary decrease, it appears that this is largely within the Chicago area, whereas teachers outside of Chicago received an average increase in salary in 2009.  The race least impacted by the 2009 recession was Native American.
Overall, the dataset contains 77% female teachers and 23% male teachers.  As salary increases, the distribution of of males to females also increases.  The distribution of teachers making $84k and above is 44% male and 56% female.  The overall average salary for all teachers in our dataset is 48.5k and overall median is 51.7k.





