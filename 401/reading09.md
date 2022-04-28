
# [The magic of Dunder](https://dbader.org/blog/python-dunder-methods)

## KID DUNDER~

Dunder, short for double under are also known as special methods.

They let you emulate behaviours of built-in types. Normally in a class they do not have access rto these.

`__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__` is to be unambiguous.

`__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser.

`self.__class__.__name__`: The class name programatically. This can be helpful if the class name might change. This way it'll always reference itself regardless of name. 

`__len__` length of

`__getitem__` - dunder of `for x in y`

`__reversed__` What it sounds like `[::-1]`

## Stats

Ok let's get real here stats is such a complicated topic that it takes decades to wrap your head full around, people take classes and get masters degrees in this. 

### Probability 

Sample Space - The set of possible events that have a probability of occouring

Normal Distribution - the defining qualities are symmetry and shape.

Normal distribution is significant to probability and stats thanks to: The Central Limit Theorem and the three Sigma Rule

Central Theorem states the more trials that are conducted the closer to the true probability we will reach

If we make many estimates, the Central Limit Theorem dictates that the distribution of these estimates will look like a normal distribution

Three Sigma Rule

The Three Sigma rule, also known as the empirical rule or 68-95-99.7 rule, is an expression of how many of our observations fall within a certain distance of the mean.

By taking advantage of the Three Sigma Rule and the Z-score we can find out how different certain things are from the average case.

Z-Score - how many standard deviations is the thing away from the MEAN 

Z-score doesn’t provide much information to you. It gains the most value when compared against a Z-table, which tabulates the cumulative probability

### Things I'd like to know more about

How does one simply walk into mordor?

I really bailed on my statistics in college, and AP stats I didn't do well in highschool.  Ishould probalby try and apply myself a bit more if I'm going to be using thids. Thoughh stats is important in data science, I'm pretty determined IMO to stay away from it in programming. XD.