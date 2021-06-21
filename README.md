# The prediction of a bank term subscription for target marketing.. Summary:



This is just the summary of the project, please view the full report 'Target Marketing Estimation for Term Deposit Subscriptions.pdf' for more detail. 
Additionally the code for the project can be found in 'Bank_Term_Deposit_Project.ipynb'


## Abstract:

A term deposit is a fixed-term investment that includes the deposit of money into an account at a financial institution. Term deposit investments usually carry short-term maturities ranging from one month to a few years and will have varying levels of required minimum deposits. A customer will deposit or invest in one of these accounts, agreeing not to withdraw their funds for a fixed period in return for a higher rate of interest paid on the account. If a customer places money in a term deposit, the bank can invest the money in other financial products that pay a higher rate of return (RoR) than what the bank is paying the customer for the use of their funds. The bank can also lend the money out to its other clients, thereby receiving a higher interest rate from the borrowers as compared to what the bank is paying in interest for the term deposit. Net interest income is the amount of money earnt from the offset of the interest from clients borrowing the term deposit money and the interest given to clients for subscribing to a term deposit.

## Introduction:

Target marketing is vital for many businesses that offer products to their customers, to be able to classify whether a customer will or will not respond to an offer has major advantages when it comes to profitability and expenditures. We will use the F-beta metric (weighted harmonic mean of precision and recall) with a weighting of 
1.5 which is weighted more towards recall (reducing false negatives) but with some weighting towards precision (reducing false positives) aswell. Having F-beta weighted this way allows us to gain more in profit by not missing potential subscribers but with a slight trade off in gaining some extra costs, since our profit margin is quite big this allows our model to extract more profit than if we weighted F-beta more towards reducing costs.

## Project Outline:

For this project we chose an arbitrary number of £10000 for the term deposit amount for 2 years earning the client 5% interest. We will assume we will gain 10% interest over the 2 years from borrowers leaving us with 5% profit, which amounts to £500 in net interest income per term deposit subscription over the 2 year term, there will be a cost per targeted client of £30. Another assumption that we have made is that the distribution of the target variable classes are the same as the population, this is so we have class priors for the expected profit calculation.

## Results:

We found that if we target everyone on average we will achieve a profit of £25 per client, with our final model we can achieve on average a profit of approximately £33 per client if we target the top 25% of clients with the highest probability of subscription (modeled for p(S|x), where S is subscription and x is the client), this is a 32% profit increase over the base rate £25.
