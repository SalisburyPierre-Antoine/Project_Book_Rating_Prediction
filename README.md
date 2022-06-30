Project_Book_Rating_Prediction

From the Goodreads dataset based on real information from readers, we will study and exploit the data in order to propose predictive models concerning the appreciation of books. The goal of this project is to predict the book rating and analysis which factor affect the rating most.

What is our target variable ? What are our explanatory variables ? Target variable : average_rating. Predictors : other variables selected in part 3. 

To do so, it is necessary to proceed in three key steps :

First, we will prepare our dataset to allow data analysis (data processing, data cleaning, exploratory analysis, plot of relevant attributes).

- Data verification                                
- Fixed the error on the num_pages column
- Fixed the error on J.K. Rowling
- Conversion to the appropriate data type on publication_date
- Replacing null values with the correct dates
- Box plot :  verification of extreme values which can bias the average  outliers which are often input errors,  correction on the num_pages column
- 4 histograms on Top 5 (Occurrences, Rates, Publishers, Authors)


In a second step, we will proceed to the feature selection (feature engineering, feature pruning, choice justification)

- Extraction of the year of publication in a new column 
- Add a new feature which has the number of occurrences of each book
- Encoding of the language_code column renamed to language, deletion of under-represented languages
- Pie plot of our new language column with book languages in percentage
- Scatter plot : text_review_count and year
- Creation of categorical columns (text) : average_rating_cat, num_pages_cat, year_cat
- Creation of categorical columns (integer): average_rating_cat_num, num_pages_cat_num, year_cat_num
- Using sns and crosstab to make choice justification
- Correlation : we choose the one that seems to us the most striking : between average_rating and num_pages_cat_num
- Encoding: explicit the "num_pages_cat_num" column by converting it to 3 columns


Finally, we will select models by evaluating them (elvaluation metrics, results interpretation) in order to train the models to better compare them and choose the one that is most appropriate and gives the best results.

- Split the data into Train and Test
- Initialize and train the model
- First model : linear regression
- Evaluate the prediction
- Compare different models

To conclude : 
    
Concerning the models, it is necessary to distinguish between the prediction of 0s and 1s, that is to say books which have rather disappointed readers from books which have rather satisfied readers.
Our different models have a much better ability to predict 1s than 0s.
In addition, the results must be weighted:
There is more data concerning the 1s so on average this will pull up the result of our predictions. Hence the importance of distinguishing between 0, 1, precision, recall, f1-score and support.

When we evaluate our model in the classification task we have to think about many things : choice of features / Dataset (cleaning) / model / model parmeters

Then the question is where we can improve the dataset, the model ?
Do not hesitate to do retro engineering to get better performance.
For the moment we did a lot and had relevant result so we will not do retro engineering.

For further we could add a new category of appreciation of the books or change the limit of our actual categories
