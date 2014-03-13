##Day 3 Morning Meeting
####Location: The Cave
####Teachers: Brick & Strand
####Cohort: Fiery Skippers

###LECTURE

**PRIMITIVE DATA TYPES**
Boolean
Integer
String
Float (long, large numbers)
Fixnum (bigger than int)
Symbol (can't be ints)

**DATA STRUCTURES**
Hash
Array
Custom object
Set
Matrix

########################################

##Day 3 Afternoon Lecture
####Location: The Cave
Teachers: Brick & Strand
Cohort: Fiery Skippers

Hashes show up everywhere for the rest of our careers. 
Hashes are an object literal in Javascript.

Hashes make great arguments for methods.
Strand likes to use a hash as the argument whenever he's passing more than 2 arguments to a method.
He puts them in a hash and pashes the hash instead.

def bakes_cookies(12, "oatmeal", "medium", "may contain nuts")

instead, do this:

def bakes_cookies(options)  #args is a Hash
	options[:count]
	options[:type]
	options[:allergens]
end

POODIR chapter 4 does a really good job of explaining this

Strand invites us to read POODIR by the end of Week 2.


###AHA MOMENTS
Drew: I can go out with people in the city
David: BasketcasE
Ranges need ()
I can do (range).to_a.sample to get a random number within a range (but not a range of floats)