# Prosper Loan Data Exploration
## by Satoshi


## Dataset

>The dataset, ProsperLoanData, contains 113,937 loans with 81 variables on each loan. From this dataset, I select 18 variables that may impact on this exploration as a new dataframe, loan. Those variables include loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. Most of them are numeric in nature, but those valuables such as credit grade, income range, loan status, prosper rating, employment status are categorical.

> Before the exploration, following wrangling are made on loan that includes the creation of 5 additional columns;
> - 'IncomeRange' column, 'Not displayed' and '$0' replaced to NaN
> - 'EmploymentStatus' column, 'Not available' replaced to NaN
> - create new column, 'Grade' by combining 'CreditGrade' and 'ProsperRating'
> - create new column, 'GradeNumeric', numeric data of 'Grade'
> - 'EmploymentDuration' cut into 4 group, 'short', 'medium', 'long' and 'very_long'
> - create new column,'LoanStatus1' by putting several Past Dues all together into one single Past Due
> - convert IncomeRange, Grade and LoanStatus1 into ordered categorical types
> - LoanOriginalAmount cut into 4 groups based on those amounts,'small','medium','big' and 'very_big'
> - create a new column 'student' where only 'student' or 'not student' are around.

> The clean dataframe, ‘loan’, that contains 113,937 loans and 23 variables on which exploration is made.

## Summary of Findings

> Occupations of very big loans(those amounts are bigger than  $12,000) are Professional, Executive, Computer Programmer, Analyst etc those are, generally speaking, high earners that were evidenced by the plots of IncomeRange, nearly 70% of very big loan is taken by the people of income above US$50,000.

> In terms of small loans(those amounts are smaller than $4,000), situation is the other way around, more than half of small loans are taken by the income range less than $50,000 whose occupation are professional, Administrative Assistant, Clerical, Teacher that are different from big loan takers. 

> Borrower APR and Grade Numeric are negatively correlated. The better grade borrowers got a low interest rate. And also Borrower APR is negatively correlated with loan original amount. Interest rates of small loans are higher than ones of big loans. Loan Original Amount is positively correlated with Grade Numeric. The better grade can get a bigger amount of loans.

> Borrowers APR and Estimated Loss are positively correlated and also positively correlated with Estimated Return as well. This can be understandable that Estimated Returns are positive correlations with Borrower APR because high interest rates can give a more return to lenders than low interest loans but,  at the same time,  that high interest rate is given to low grade borrowers that should increase the chances of defaults or past due. 

> Grade Numeric is closely linked to income range but,  little link to Employment Status nor to Employment Duration. I assume that borrowers' grades are decided based on income range rather than Employment Duration and Employment Status.
 
>Small loans and lower grades have higher risks  of charge off, defaulted and past due .Middle to lower income range($25000-$74,999) is the highest cases of  Charged Off, Defaulted and Past due. This is a bit surprising at first look because of the higher risk case than that of the lowest income range($1-$24,999), but actually the total numbers of loans in this range are simply bigger than the lowest income range . It can be said that Charged off, defaulted and past due can happen more frequent in the low income range borrowers.

> Employment Status has a significant impact on Loan Original Amount. ‘Employed’ status  occupied the majority part of loans. ‘Employed’ together with ‘Full time’ covers almost all of the loans.
 
> Loan Original Amount and Grade are positive correlations.  The grade is better, the categories of loan amount are bigger. For grade AA, A, B and C, the most frequent categories are very big loans, while HR, E, D, small loans are the most frequent. Particularly in HR almost all of the loans are small categories. 


## Key Insights for Presentation

> Total amounts of loans for big loan categories by homeowners are about  double compared to no home ownership in very big loans, while in small loans, amounts of loans of no homeowners are bigger than those for homeowners. 

> The Income range and Homeownership are main factors for Grades. The Grades is the key factor, and together with Employment status that decide the amounts of loans and interest rate..
