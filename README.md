# AN INSIGHT INTO SHORT LET PRICING: AIRBNB SEATTLE CASE STUDY
In this project I would be exploring the dataset of airbnb listings in the Seattle. There are 3 dataset to be explored in this project. The data in this project was downloaded here. The result of this project would give insight to people that want to get into the business of shortlet to understand how prices are determined and factors that affect it
# PROJECT MOTIVATION
This project is meant to answer some questions that potention shortlet owners would have, giving clearity to the pricing system of shortlets using airbnb as a case study. Some of these questions are;

How does prices differ among days of the week?

What room type has the highest price?

What factors affect the price of shortlets?

What are the most popular amenity?

What is the user experience of airbnb users in Seattle?

# DATA UNDERSTANDING

There are three data sets in this project

listings.csv
calendar.csv
reviews.csv

# DATA PREPARATION

Dealing with incorrect data type: The price column and the date column in the calendar were strings. I created a function to convert the price variable to float.

def float_price(x):

‘’’
input: dollar value with string dtype
output: value in float
‘’’
if type(x)==str:
x=x[1:].replace(“,” , ””)
x=float(x)
return x


This function takes the variable and removes the dollar sign and the comma sign then converts the remaining characters to float.

For the date column, I used the PD.to_datetime function to convert it to a DateTime type.

Dealing with missing variables: Missing variables were handled differently depending on the need of the analysis. For some cases I used zeros to fill the nan values other times I filled them with the mean of the column.

Dealing with categorical variables: For categorical variables, I created a dummy variable

# LIBRARIES USED

The following libraries were used to excute this project

> 1. Numpy

> 2. Pandas

> 3. Matplot

> 4. Seaborn

> 5. Scikit Learn

> 6. WordCloud

## Installations
This libraries work in latest python and they can be installed by running this code

pip install -r requirement.txt

# FILE DESCRIPTION

> Airbnb.ipynb: Notebook containing the data analysis

> calendar.csv: csv file containing bookings

> listings.csv: CSV file containing information about listings

> reviewa.csv: CSV file containing reviews

# SUMMARY OF THE RESULTS

> * There are no significant difference between the prices of listings for each day. However, Fridays and Saturday have the highest prices but the numerical difference is not much

> * There is a slight difference of about $5 between weekdays and weekends. Weekdays were encoded with 0s and weekends with 1, from the chart we can see that on weekends the average price is 140.89 and that of the weekdays is 135.75

> * The distribution of the prices in private rooms and shared rooms are almost the same with a large chunk of prices in the two room types are in the same range. However, the price of apartments have a higher range

> * There is a strong positive correlationship in the cases of the number of people the listing can contain (accommodates) and the bedrooms in a particular listing with a correlational coefficient of 0.65 and 0.63 respectively. There is also a positive correlation between price and the amount paid as security deposit. However, the is a negative correlationship between the reviews per month and the price. I would be creating a linear regression to further investigate and validate these claims

> * 51% variability in the price is explain by the independent variables I used. Also I would like to make further investigations to understand the model I created to see if the independent variables have a statistical significant effect on the dependent variables

> * From the word cloud, we can see that words like internet, washer, dryer, smoke detector, and fire extinguisher stands out among other.

> * There are more positive words used by the users in the comments section words like nice, perfect, easy, thank and great stands out. This indicated that users have a positive experience using Airbnb in Seattle.
