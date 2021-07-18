# Prosper Loan Exploratory Data Analysis
 
### Dataset
This investigation is based on a dataset from Prosper, which is America’s first marketplacelending platform, with over 12 billion dollars in funded loans. This data set contains 113,937
loans with 81 variables on each loan. For this project, I have focused on 17 variables, which I
selected based on my assumptions. The variables include loan amount, borrower rate (or
interest rate), ProsperRating (Alpha), ListingCategory (numeric), Term, current loan status,
borrower employment status, StatedMonthlyIncome, DelinquenciesLast7Years,
LoanOriginationDate, Recommendations, Investors and TotalProsperLoans.
There are a lot of nulls for most of the variables in the dataset, so a lot of data wrangling was
done to clean the data. Prosper starting using Prosper Rating from 2009,so for this analysis,
only the datapoints after 2009 have been considered and the data before 2009 has been
dropped. Also, most of the loans in dataset are actually current loans and hence cannot be used
to predict default on credit. For this project, Loan Status has been split into just two categories :
Completed and Defaulted. So, all the current loans are removed and the chargedoff and
defaulted credits are merged together as defaulted.
Stated monthly income is highly skewed and had an unusually high number of outliers and very
large range of values from 0 to 1,750,000. So, all such outliers that are above three standard
deviations from the mean are removed.
ListingCategory (numeric) is a numeric variable according to the dataset and has less count for
most of the categories making it difficult to visualize. So, the categories have been reduced and
the datatype of variable is changed to categorical from numeric.
### Summary of Findings
Prosper ratings are almost normally distributed with AA rating as the highest and HR as the
lowest. The Prosper rating C is the most common rating.
Distribution of monthly stated income is highly spread with a wide range and lot of outliers.
Prosper rating D is the most frequent rating among defaulted credits.For Term, the loans time periods, there are three options: 36, 60 and 12 months. Again, the
most popular term for the loans among the borrowers in this dataset is 36 months. Also, Longterm (60 months) have the greatest proportion of defaulted credits.
The LoanOriginalAmount plot indicates that borrowers usually ask for an amount less than
15.000 USD, even though there are also loans with much higher amounts. Especially 5,000,
10,000 and 15,000 USD loans are very popular on Prosper.
Default credits tend to be given to individuals with lower rating. Business and home
improvement seems to represent a higher risk. The borrower rate tends to be higher for
defaulted credits. Long term (60 months) credits are riskier than short term (12 months).
Borrower rate for individuals with low rating is higher. High monthly income corresponds to
higher rating. Employment status of individuals with lower ratings tends to be 'Not employed',
'Self-employed', 'Retired' or 'Part-time'.
Borrowers with high Prosper rating tend to borrow more and the ones with low rating on the
other hand tend to borrow less. Also, among the high rating borrowers, the defaulted loan
amount is higher than the completed, whereas among the low rating borrowers, defaulted
credits usually are almost equal as completed.
### Key Insights for Presentation
For the presentation, I focus on just the factors affecting a loan’s outcome status, borrower
characteristics and best features for predicting default on credit. I start by introducing the
variables such as Borrower income, Employment status, loan amount and status,
followed by plotting them and analyzing the distributions.
Later I used clustered bar charts to analyze the relationship between Loan Status with Prosper
Rating and Listing category. I also used violin plots of Prosper Rating with Borrower's monthly
income, Investors and Loan amount.
I have made sure to use different palettes for each quality variable to distinguish between
plots.
### Resources:
https://knowledge.udacity.com/questions/444389
https://seaborn.pydata.org/tutorial/categorical.html?highlight=bar%20plot
https://stattrek.com/statistics/charts/histogram.aspx
https://eazybi.com/blog/data-visualization-and-chart-types