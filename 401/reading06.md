
# READING 06

---

## [Using RandomModule](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

this mopdule is very handy when you just need something random

|function|description|syntax
---|---|
|Randint|prints a random number beween two integers| random.randomint(0,5)|
|Random| If you want a large number you can ,multiply it| random.random() *100 #1-100|
Choice| Generate a selection from a  list | random.choice([red,blue,black])|
shuffle| shuffles element list in place| shuffle(x) where x is a list|


## [Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/) 

Risk analysis helps highlight potential problems before they appear. GHelping devs and managers mitigate the risks. When a test plan is created, riskes involved in the testing product are to be taken into consideration along with the possible damage to your product with teh solution.  

### Some factors

1. Use of new hardware
2. Use of nreew technology
3. Use of new automation tool
4. Code sequence
5. Availibility of test resources. 

Some of these are unavoidable

1. Testing time allocation
2. A defect leakage due to size and scope. 
3. Clients urgency and pushing to release an incomplete product.
4. incomplete reqs. 

In these cases you should Conduct an assesment review meeting, use maximum resources on difficult or high problem areas. Create a risk database for future reference. 

Don't forget to identify risk magnitude when evaluating and reporting. 

### Risk analysis process 

1. Forcast the unwanted situation of the project
2. Estimating potential loss in sucha situation
3.  MAking a decision to deal with situation
4. Avoid future concequences. 

### Perspectives

- Effect - Identify a condition or event to determine impact
- Cause - To assess risk by cause is reactionary from effect, you scan the issue to find the propable point of interaction.
- likelyhood -  To say there is a probability of a requirement not being satisifed

## [Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)

TDD is something that is useful but not sufficient to get you good tests. If you test thoughtful and well, coverage should be in the 80-90% range.   

You really are only doing enough testing if the following are ture
- You rarely get bugs into production and you aren't afraid of changing code because it might cause them. 

CAn you overtest - YES - If testing is slowing you down and you acan remove tests and still have enough you are overtesting. 

Some poeple think taht if testing takes a long time then you have too many tests. You can always move these tests down your development pipeline if they take to long.  

## Big O Notation

How runtime scales with input 

## Things I'd like to know more about. 

How to develop better tests for your programs to make sure that it is operating as intended, especially once your programs start to get more complicated. Like how to tests for GUI look?