# Midterm-Project-LHL

## Project Motivation and Goals

The goal of this project was to identify trends and gather insights using the available data on Best-selling Amazon books (2009-2023). 

## Key Questions

Studying available datasets to find relationships between different variables. Key questions included:
1. What makes a book highly rated? Do factors like price and review numbers affect rating?
2. What is the general trend of books that make it to the best-selling list?
3. Which authors make it to the best sellers list more often?

## Repository folder guide/order
a. Readme

b. notebooks
   1. Project4_notebook.ipynb

c. data
   1. Best-selling books data 2009-2023-1.csv (raw)
   2. Bestselling_Books_clean.csv (dataset after EDA and data cleaning)
   3. Bestselling_Books_clean - Copy.xlsx (converted to xlsx format for Tableau)


## Process

![image](https://github.com/Zarmeena667/Midterm-Project-LHL/assets/145514413/8ac84cf4-c30d-4039-9f7d-55c5eb0b77ca)


1.	Accessing and Retrieving Data 

Top 100 Best-selling books data was retrived from Kaggle. The composition and key features of the data are shared below: 

![image](https://github.com/Zarmeena667/Midterm-Project-LHL/assets/145514413/65522749-cb46-4408-a86b-c173680558be)


2. Data cleaning and EDA

Data was imported from the csv raw file and converted to dataframe to implement data cleaning and EDA processes. In addition to removing nulls and performing descriptive analysis, we used Visual EDA to check outliers and assess relationship between variables. The clean data was then saved as a CSV file. 

3. Regression Analysis

A Simple Linear Regression was first used to test the relationship between 'Rating' and 'Price'. The relationship of dependent variable 'Rating' was further assessed using multivariate regression where 'Price and Number of Reviews' were selected as the predictor/independent variables. Lastly, the relationship between 'Genre', 'Rating' and 'Price' was assessed using Logistic Regression model. 


6. Visualization and Dashboard in Tableau

We used different Tableau tools to generate meaningful insights from our data. The Tableau tools used are shared below:

    Sets
    Parameters
    Calculated Fields
    Quick table calculation


## Results/Insights

1. In relation to the relationship between Rating, Reviews and Price the low P value of the multivariate regression model revealed that the relationship is statistically significant, however the R-square was quite low that the model might not be explaining a substantial portion of the variance in the dependent variable. There might be other influential factors that weren’t considered.
2. Our second big question with this dataset was to determine if there is a relation between rating and genre. With the help of a logistic model, we were able to determine a statistically significant relationship between the predictors (price and rating) and the dependent variable (genre). Key insights from the model are shared below:
a. The log-likelihood of the model is somewhat higher than the LL-Null which indicates that the model is providing a better fit than a null model.
b. Const (-4.6798) is the log odds of the baseline category Non-Fiction when all predictors are zero. A one unit increae in rating could increase 1.0276 in the log-odds of book being Fiction compared to it being Non-Fiction. Alternatively, a unit increase in price is linked with the decrease of 0.0183 in the log odds of the book being Fiction as opposed to Non-Fiction.
c. P-value lower than 0.05 percent suggests that the model is still statistically significant.
3. Of the top 10 authors who frequently appear on the best-selling list 6 are children and young adult book writers. These authors also happen to be top-rated. 
4. The top reviewed book is 'Where the Crawdads Sing', adult fiction.
5. Although more non-Fiction books make it to the Best-selling list, fiction remains more widely reviewed.
6. The average price of non-Fiction is greater than the average price of fiction indicating there is a statistically significant relationship there though as predicted from the model, it's not enough to explain the variance in the dependent variable. 
7. Interesting fact: Writer Colleen Hoover had 10 best-selling books on the 2022 Best-selling list.

#### Alternate Visuals
The alternate visuals (`Project4_Alt.twbx`) present the data in a alternate way. One major aspect of these visuals is the `Author Score`.
   * Every book is given a `Rank Score`, which is calculated as: 101 - (the book's Ranking).
   * `Author Score` is the sum of an Author's `Rank Score` for every book.
* `Author Score` gives a weighted value that accounts for Ranking and number of Top 100 titles.


## Challenges 

1. Key features that would’ve really helped enhance the analysis or draw concrete conclusion were missing in the data set (such as number of books sold that are trending on the best seller list).
2. Limited related variables made it difficult to test relationships.
3. The amazon best-seller rankings are updated frequently.
4. Getting genre/sub-genre for the data also proved cumbersome. 



## Future Goals
1. Finding a more comprehensive dataset (fetching data through APIs).
2. Comparing to other Best-sellers list (e.g. NY Times Best Seller List). 
3. Might also be interesting to compare data for different regions.
4. Combine data and visuals to have one focused question/goal being explored.


