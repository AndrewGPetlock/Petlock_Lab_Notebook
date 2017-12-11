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

< = less than
> = greater than
<= less than / equal to
>= greater than / equal too
== equal  to each other
!= not equal to each other











