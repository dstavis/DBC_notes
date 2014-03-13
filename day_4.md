##Day 4 Notes

###MORNING MEETING

```
David Stavis:
An open-source version of Ruby-doc.org done in the EXPLAIN LIKE I'M FIVE format.
Brick & Strand: We don't know of one. That's a REALLY GOOD project.

My idea: Set it up on github. Create a framework for it. Go into the ELI5 forum and introduce the project.

Each method in Ruby will get its own Thread on Reddit.
Anyone on ELI5 can write a ELI5-esque explanation of the method, using understandable language and real-world logic examples and post it as a comment. The one that gets the most upvotes will be pulled into the project.

If the entry with the most upvotes is a joke entry, it will still be included, but another high-upvote entry will be the primary entry for that method.

sensiblerubydocs.org
rubydocslikeimfive.org/.com
understandablerubydocs.org
rubydocsli5.org

float between 1 and 5 = (Math.rand * 5).round(2)
```

```
Chris Cooper:
Recursive Prime Number Prime Factorization Method
def primenum (number, divisor = 2, array_of_primes = [])
	until number % divisor 
		divisor += 1
	if #number is prime number % divisor == 0 && some other test
		array_of_primes << number
	primenum (number, divisor, array_of_primes)
end

Brick: Takeaway= Solving for "any case" is much harder to think of than solving for a specific case.

i.e., solving for primenum(8) #=> [2, 2, 2] is much easier to do than 
Working with a particular test case is key to solving your complex problem.
```

```Ruby Racer
Two files. Using require and require relative.
```

################################

##Morning Coding

###Questions:
####1. player_positions worked in a class method without an @. Why? Should it have an @?
####Answer: @pp references the instance variable. pp calls the method created by attr_reader- that method, how it works, and what it does, can be changed if necessary, so the pp call is resilient. @pp is NOT resilient- if the accessor method changes, @pp will break.
Aha moment: I'm going to use pp from now on, and create attr_accessors for the instance variables I want to reference.

################################

