
# Partitioning and Law of Total Probability - Lab

## Introduction 
In this lab, you'll practice your knowledge of the law of total probability. In probability theory, the law (or formula) of total probability is a fundamental rule relating **marginal probabilities** to **conditional probabilities**.

## Objectives

You will be able to:
* Understand and explain the concept of event space and partitioning 
* State the law of total probabilities based on a partitioned event space
* Understand and be able to perform partitioning based on known and unknown probabilities to solve a problem

## Exercise 1
Imagine you have two hats: one has 4 red balls and 6 green balls, the other has 6 red and 4 green. We toss a fair coin, if heads, you will pick a random ball from the first hat, if tails you will pick one from the second hat. 

What is the probability of getting a red ball?


```python
hat1 = .4
hat2 = .6
coin = .5
```


```python
hat1* coin + hat2* coin
```




    0.5



## Exercise 2
In games where at least one goal is made, a soccer team wins 60% of its games when it scores the first goal, and 10% of its games when the opposing team 
scores first. 

If the team scores the first goal about 30% of the time, what fraction of the games does it win?


```python
wug= .6
wung= .1
g = .3
wug* g + wung*(1-g)
```




    0.25



## Exercise 3

In Europe, except for regular gas, cars often run on diesel as well. At a gas station in Paris; 


* 40% of the customers fill up with diesel (event G1) 
* 35% with gas "Super 95" (event G2)
* 25% with gas "Super 98" (event G3). 


* 30% of the customers who buy diesel fill their tank completely (event F). 
* For "Super 95" and "Super 98", these numbers are  60% and 50%, respectively.


- Compute the probability that the next customer completely fills their tank and buys Super 95. 
- Compute the probability that the next customer completely fills their tank
- Given that the next customer fills their tank completely, compute the probability that they bought diesel. 

Hint: Consult the theorems for conditional probability, check for dependence or independence of events


```python
g1 = .4
g2 = .35
g3 = .25
fug1 = .3
fug2 = .6
fug3 = .5

```


```python
g2*fug2
```




    0.21




```python
g1*fug1 + g2*fug2 + g3*fug3
```




    0.45499999999999996




```python
g1* fug1/(g1*fug1 + g2*fug2 + g3*fug3)
```




    0.26373626373626374



## Exercise 4

United Airlines operates flights from JFK to Amsterdam, to Brussels, and to Copenhagen. As you may know, flights are overbooked fairly often. Let's denote the probability of the flight to Amsterdam being overbooked equal to 40%, the probability of the flight to Brussels being overbooked equal to 25%, and the probability of the flight to Copenhagen being overbooked equal to 35%. You can assume that these events of overbooking are independent events.

- Compute the probability that all the flights are overbooked.
- Compute the probability of having at least one flight which is not overbooked.
- Compute the probability that exactly one flight is overbooked.


```python
flightA = .4
flightB = .25
flightC = .35

flightA* flightB* flightC
```




    0.034999999999999996




```python
1-flightA* flightB* flightC
```




    0.965




```python
justoneA= 0.4*0.75*0.65 
justoneB = 0.6*0.25*0.65
justoneC = 0.6*0.75*0.35



justoneA+ justoneB+ justoneC, justoneA, justoneB, justoneC
```




    (0.45, 0.19500000000000003, 0.0975, 0.15749999999999997)



## Exercise 5
You have three bags that each contain 100 marbles:

- Bag 1 has 75 red and 25 blue marbles;
- Bag 2 has 60 red and 40 blue marbles;
- Bag 3 has 45 red and 55 blue marbles.

You choose one of the bags at random and then pick a marble from the chosen bag, also at random. 

What is the probability that the chosen marble is red?



```python
bag = 1/3
one = 75/100
two = 60/100
three = 45/100
bag*(one+ two + three)
```




    0.6



## Summary 

In this lab, you practiced conditional probability and its theorem with some simple problems. The key takeaway from this lab is to be able to identify random events as dependent or independent and calculating the probability of their occurrence using appropriate methods. Next, you'll take this knowledge a step further and run simulations with conditional and total probability. 
