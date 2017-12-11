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
* > = greater than
* <= less than / equal to
* >= greater than / equal too
* == equal  to each other
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













