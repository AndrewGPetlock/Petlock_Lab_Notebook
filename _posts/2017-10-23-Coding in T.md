---
layout: post
title: Coding in R
date: '2017-10-23'
categories: R
tags: 
---

This post contains a series of helpful tutorials / examples how to code in the programming language R.

# assign variables 

* variable_name <-- (data; numbers ie., 420 or string ie., "hello")

# vectors

* variable_name <-- c(data)

# give names to elements of a vector

* some_vector <-- c("John Doe", "Poker Player")

* names(some_vector) <-- c("Name", "Profession")

# sum in a vector

* sum(vector_example)

# selection within a vector

* use square brackets[..]

ie., first element in vector --> poker_vector [1] or poker_vector ["monday"]

ie., third element in vector --> poker_vector [3]

ie., find elements on tues, wed, thurs --> poker_vector [c(2,3,4)] (also written as [2:4]

ie., find average winnings from mon - wed:

poker_start <-- poker_vector [c("Monday", "Tuesday", "Wednesday")]
mean(poker_start)
poker_start

ie., find which values in poker_vector are positive:

selection_vector <-- poker_vector > 0
selection_vector
[returns TRUE for positive, FALSE for negative

# logical comparison operators 

* < = less than
* >= greater than
* <= less than / equal to
* >= greater than / equal too
* "==" equal  to each other
* != not equal to each other

ie., find profits (positive values) from different days

(roulette winnings from mon - fri)

roulette_vector <-- c(-24,-50,100,-350,10)

days_vector <-- c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday")

names(roulette_vector) <-- days_vector

(which days did you make money on roulette)

selection_vector <-- roulette_vector > 0

(select from roulette_vector these days)

roulette_winning_days <-- roulette_vector [selection_vector]

roulette_winnings_days #prints results#

# Matrix

* matrix (..) 

ie., matrix(1:9, by row = TRUE, nrow = 3)

1:9 = collection of elements that will be put into rows and columns

byrow = matrix is filled by rows (if matrix is filled by columns, then [byrow = FALSE]

* rownames(my_matrix) <-- row_names_vector

* colnames(my_matrix) <-- col_names_vector

* rowsums(my_matrix) = calculates totals for each row of a matrix / colsums(my_matrix) = totals for columns of a matrix

* add multiple columns to a matrix = cbind(...) / rbind(...) = pastes matrix together

ie., big_matrix <-- cbind(matrix1, matrix2, vector1, ...)

# Selection of matrix elements

* my_matrix[1,2] = selects elents first row and second column

* my_matrix[1:3 , 2:4] = matrix with data in rows 1,2,3 and columns 2,3,4 selected 

* my_matrix[,1] = selects elements of the 1st column

* my_matrix[1,] = selects all elements of the first row

ie., non_us_some <-- all_wars_matrix[1:2 , 2]

# Factors 

* factor(...)

ie., gender_vector <-- c("male", "female", "female", "male", "male")
     factor_gender_vector <-- factor(gender_vector)

* factors level: levels(...) / levels(factor_vector) <-- c("name1", "name2",...)

ie., 

survey_vector <-- c("M", "F", "F", "M", "M")
factor_survey_vector <-- factor(survey_vector)
levels (factor_survey_vector) <-- c("Female", "Male")
factor_survey_vector

[1] male female female male male
Levels: female male

ie.,

factor(some_vector, ordered = TRUE, levels = c("level1", "level2",...)

(ordered = TRUE <-- true indicated that the factor is ordered 

* summary(my_var)

# data frames 

* head(...) = show first observation of data from header (contains names of different variables in data set)

* tail(...) = prints last observation of data set 

* str(...) = structure of data set 

	* total number of observations
	* total number of variables
	* a full list of variables 
	* data type of each variable 
	* first observation
	
# Selection of data frame elements

* my_dataframe[1,2] = selects value at the first row and select element in my_dataframe

* my_dataframe[1:3 , 2:4] = selects rows 1,2,3 and columns 2,3,4 

* my_dataframe[1,] = select all elements of first row

* my_dataframe[,1] = select all elements of first column 

ie., 

planets_df[1:5, "diameter"]

ie.,

rings_vector <-- plants_df$rings = short cut to planets_df[,4] (4th column aka rings)

* subset(my_df, subset = some_condition) 

ie.,

subset(planets.df subset = rings)

* order(...) = ranked position of each element when it is applied on a variable

ie.,

> a <-- c(100, 10, 1000)
> order a
[1] 2 1 3 

ie., 

> a [order (a)]
[1] 10 100 1000     (reshuffles data)

ie.,

positions <-- order (planets_df$diameter)
planets_df[positions,]


# Lists


* lists(...)

my_list <-- list(comp1, comp2...)

my_list <-- list(name 1 = your_comp1, name 2 = your_comp2)

My_list <-- list(your_comp1, your_comp2)
names(my_list) <-- c("name1", "name2")

shining_list[1] = grab first component or shining_list$reviews 

c(...) = add elements to the list / ext_list <-- c(my_list, my_val)

# Importing data into R

* variable_1 <-- read.csv("swimming_pools.csv." StringsAsFactors = TRUE)

(StringsAsFactors --> TRUE = imports strings as integer values 
                  --> False = import files as characters 



















