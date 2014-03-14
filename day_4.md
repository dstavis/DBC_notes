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

##Afternoon Lecture

###Recursion
Need 3 things to be technically recursive
1. Base case
2. Call to itself
3. Movement toward the base case

recurse_me aha moment:
if you have code in a recursive method that sits after the call to itself, it will run on the way back up the stack once the base case is reached and the calls from deep in the stack start returning.

PRY is a gem. Gives an irb-esque console that you can use from anywhere in your program.

How to make pry happen:
git stash list
gem install pry pry-nav

add 'require "pry"; binding.pry' somewhere in the code
run it, and you end up in a repl

type 'help' to learn how to use pry


################################

MINSYN
Matz is nice so you're nice
Matz almost called it Coral instead of Ruby
but he went with Ruby, because it's kind of like Perl.

Matz announced it to his mailing list and suggested they use it in 1994.
But all the Ruby documentation was in Japanese, so the rest of the world didn't care.
So it was small for many years.
Then Dave Thomas happened.
Dave heard that this interesting language had been around for 5 years, and that it was super cool if you could figure out how to use it.
He downloaded ruby and opened up irb to start trying to use it. He opened up the source code on one side, irb on the other side, and assumed what would work or not based on the source code. He made notes based on the output of how the language worked.
He reverse-engineered everything about Ruby this way.

He wrote a book called "Programming Ruby" that was affectionately called The Pickaxe.
Many other people heard that Ruby was awesome, but were not crazy enough to figure it out. So they bought this book in droves.
That brought Ruby to the English-speaking world.
Matz made this the official documentation of Ruby, and included it in the source.
Thus there was a Cult of Ruby in the English-speaking world. It was similar to Perl but better, so lots of Perl-users started to use it.

Ruby is still extensively used in Japan for everything.
In the Western world, you basically just use Ruby for Rails.
In Japan, it's a source of great pride that a Japanese person contributed so much to the world.

At Rubyworld Conference, they have a PARADE for Matz. He's like the most accomplished person from his prefecture in recent history.
The conference in Matz's hometown is all SALARYMAN in suits.

37signals did client work, and found that it sucked. They designed Basecamp. David Heinemeier Hanson (David HH- he hates this name) was hired as a consultant to build their app. He asked if he could do it in Ruby, and they said yeahsurewhatevs. They loved it. It was the first successful webapp built on Ruby.
David thought others might like to make webapps on Ruby, so he refactored and extracted his code and pushed it out as Rails.

Youtube search "Ruby on Rails demo" to find the Rails announcement video.

David now races sportscars as a hobby.

Ruby is a great language even without Rails.

Shoes is a desktop app-writing suite in Ruby.

Chef is a devops tool in Ruby.

No one knows how programming works. (even our superheroes)

Aaron Patterson (tenderlove) is the primary person behind ActiveRecord. He now texts 

If you meet Aaron at a conference and ask him for a sticker, he'll give you a sticker of his cat.

TenderloveMaking.com is Aaron's blog.

He has a fake company called adequatehq.com

Aaron is incredibly generous and wonderful.

"When I get stuck, I email the author of the gem."
"They suggested I write a patch, so I wrote a patch.
That's how I have these friends."

"If you need help with anything, please email me."

Don't be afraid of talking to, walking up and saying hello to these wonderful programming greats.

We're all just humans.
We're all learning and growing together.

Yehuda Katz maintains Rails 3, the Jquery core team, and EmberJS.
Had a 4-hour argument with Yehuda about how he was right at a conference- eventually Yehuda agreed. Became a human and not a godlike figure in his eyes.

Jim Weirich was this really great and amazing person. He made Rake.
You will live on in the open-source community even if you go away for whatever reason.
The community is strong.
Check out his videos on Youtube. 


##Why The Lucky Stiff
He made "The Poignant Guide to Ruby"
It's both a cartoon webcomic and also about learning Ruby!
Hackety-Hack was Why's most important work, an IDE that helps people learn Ruby.
He offered to HELP anyone who took it on. So they said, great, you're maintaining it now!
Thrust into the Open Source world.

He worked on Hackety-Hack himself for many years. Got burned out. Took 6 months of work to get it to compile.

Just doing stuff is the best way to get involved.

The worst thing that could happen is if Nobody Noticed. In which case, nobody will know that you failed, because nobody cared! That's the worst case scenario, and it's harmless.


How to share your project:!
Newsletter called Ruby Weekly.
Changelog does "What's new in Open Source"
Ruby Subreddit.
Ruby Talk mailing list.
Steve: "Tweet at me and I'll retweet it."
"RequestStore" is the most popular hack I made. It's a Rack Middleware that clears a hash for local storage variables.



Release everything no matter how trivial or dumb it seems- you can't predict what will be useful to others!
Trust, but verify. Do not accept a pull request until you test it thoroughly!

Ruby on Ales (an open bar conference) in Bend, Oregon

Dude is a gem that appends ", dude" to all your exceptions.
It's now the best-tested thing Strand has ever written.

Open Source doesn't even have to be Useful. Figure out a way to make some software that's fun, and share it with the world.

Email: Steve@steveKlabnik.com
Twitter: @klabnik
