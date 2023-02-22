# data_manipulations_with_pandas
Data manipulation with Pandas


#Project Requirements
1. 
We’ve provided a csv file containing data about the game show Jeopardy! in a file named jeopardy.csv. Load the data into a DataFrame and investigate its contents. Try to print out specific columns.
Note that in order to make this project as “real-world” as possible, we haven’t modified the data at all — we’re giving it to you exactly how we found it. As a result, this data isn’t as “clean”. More specifically, there’s something odd about the column names. After you figure out the problem with the column names, you may want to rename them to make your life easier the rest of the project.
In order to disply the full contents of a column, we’ve added this line of code to the top of your file:
pd.set_option('display.max_colwidth', -1)

2.
Write a function that filters the dataset for questions that contains all of the words in a list of words. For example, when the list ["King", "England"] was passed to our function, the function returned a DataFrame of 152 rows. Every row had the strings "King" and "England" somewhere in its " Question".
Test your function by printing out the column containing the question of each row of the dataset.

3.
Test your original function with a few different sets of words to try to find some ways your function breaks. Edit your function so it is more robust.
For example, think about capitalization. We probably want to find questions that contain the word "King" or "king".
You may also want to check to make sure you don’t find rows that contain substrings of your given words. For example, our function found a question that didn’t contain the word "king", however it did contain the word "viking" — it found the "king" inside "viking". Note that this also comes with some drawbacks — you would no longer find questions that contained words like "England's".

4.
We may want to eventually compute aggregate statistics, like .mean() on the " Value" column. But right now, the values in that column are strings. Convert the " Value" column to floats. If you’d like to, you can create a new column with the float values.
Now that you can filter the dataset of question, use your new column that contains the float values of each question to find the “difficulty” of certain topics. For example, what is the average value of questions that contain the word "King"?
Make sure to use the dataset that contains the float values as the dataset you use in your filtering function.

5.
Write a function that returns the count of the unique answers to all of the questions in a dataset. For example, after filtering the entire dataset to only questions containing the word "King", we could then find all of the unique answers to those questions. The answer “Henry VIII” appeared 3 times and was the most common answer.
