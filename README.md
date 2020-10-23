![Lending Club](lendingclub.jpg)
# Predicting default clients of Lending Club Loans
LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission (SEC), and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform.

LendingClub enabled borrowers to create unsecured personal loans between $1,000 and $40,000. The standard loan period was three years. Investors were able to search and browse the loan listings on LendingClub website and select loans that they wanted to invest in based on the information supplied about the borrower, amount of loan, loan grade, and loan purpose. Investors made money from the interest on these loans. LendingClub made money by charging borrowers an origination fee and investors a service fee.

Description: In this project, we worked with the public LendingClub data, with a size of 2.5+ GB, containing 2.26 million loans from 2007 to 2018, each of which has 151 associated features. We also used another file which has meta data for all the columns that are in the input file.

Our Goal: Given historical data on loans given out with information on whether or not the borrower defaulted (charge-off), can we build a model that can predict whether or not a borrower will pay back their loan? This way in the future when we get a new potential customer we can assess whether or not they are likely to pay back the loan. 

- Data Source: Kaggle (https://www.kaggle.com/wordsforthewise/lending-club). 

- Analysis: We analyzed useful features and investigated the correlations among the features and between the features and the target variable. According to the Pearson correlations between the features and the target variable, the most important variables for predicting charge-offs include the loan interest rate, loan term, the FICO score, and debt-to-income ratio. From feature importance analysis using the lightGBM classifier, we found that the most important features are revoloving line utilization rate, debt-to-income ratio, Months since oldest bank installment account opened, revolving balance, annual income, loan amount and interest rate.

- Steps:
    - Import required packages like pandas, matplotlib, seaborn, scipy stats, sklearn, lightgbm, keras, tensorflow etc.
    - Read the input files
    - Identify the target variable
    - Feature selection
        - Drop feature missing a lot of data
        - Drop the data that will not be available before the loan approval
        - Inspect the remaining features one by one
            - Visualization with count distributions, bar plot & KDE plot with faceting on the loan status
            - Cleaning and formatting
            - Keeping the relevant features and drop the rest
        - Statistical overview 
    - Feature Engineering
      - Encoding
      - Train-test split
      - Balancing the class
      - Sclaing
    - Modeling
      - Random Forest
      - Logisitic Regression model using tensorflow, sklearn and keras libraries
      - LightGBM with stratified Kfold cross validation procedure
      



