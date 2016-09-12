_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates 
are:

   + Something you agreed with / resonates with your own experience
   + Something you disagree with
   + Something that is interesting, a new idea or perspective you'd like to remember
   + Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**
Anthony
1. Cathedral/Bazaar Quote

"The key point is that in the bazaar style of building a program or designing a language or what you will,
the plan can change in real time to meet the needs of those who work on it and use it. 
This tends to make users stay with it as time goes by; 
they will take joy in working hard and helping out if they know that their wants and needs have some weight and their hard work can change the plan for the better"

- The idea from this quote that when designing a language, you should try to be flexible really resonates with me.
It reminds me of the two types of software development strategies, Agile and Waterfall.
With Agile designing, you don't over specify the design from the start so it is able to easily change.
However, when designing a DSL, I almost feel a "Waterfall" approach is better, so that as you implement your language, you dont forget your design goals. 
We have discussed that as too many features are added to a DSL, it becomes so saturated that it essentially becomes a general-purpose language and a "Waterfall" approach might help stop that.


2. Wizard Quote

"The problem is that programming languages are created either by committee or by extreme technical wizards with magical math powers. 
The broad computer science academic community has not paid a tremendous amount of attention to programming language usability."

This quote sums up some of the issues Programming Languages have with fluency and usability.
Essentially, these languages are created by extremely smart people who might not understand how a non-developer might interact with the language.
A simple example of this is reading Racket.
It may seem to make sense after learning about Lambda Calculus and the theory of functional programming;
however, to a regular user, it can be rather complicated esspecially if you want to create usable programs for others.   

 
3. Documentation Quotes from "How to Design a Good API..."

"APIs should be self-documenting: It should rarely require documentation to read code written to a good API. In fact, it should rarely require documentation to write it." & 
"Documentation matters. No matter how good an API, it won't get used without good documentation. Document every exported API element: every class, method, field, and parameter."

We are including this "quote" since we thought it was slightly contradictory. 
Clearly the point is that a language/API should not be complicated to use while still being documented;
however, he states it should rarely require documentation to write it while also requesting very detailed and complete documentation.
Obviously there should be some sort of documentation but maybe it shouldn't be the focus so as to create better self-documenting languages.
Maybe this is a question of trade-offs and what is possible with the fixed budget/time constraints.




---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**
Ross
+ Self-Documenting: cite API design article
   + Cite "Why Aren't Computer Languages Designed Better" (see: section with example
     loop code)
+ Extension should look like it fits; follow a pattern; cite first paper
+ Consistency
+ Efficiency with features: don't overload a language for its use-case
+ cite `gray` example
+ Bad: hard to read
+ Bad: unnatural or unobvious error messages

---

**Question**
How do the themes of _Growing a Language_ relate to the "sound lab" we did this week?

**Response**
Anthony
+ Fluency
+ Creating a pattern: chaining and natural use
+ Mode of discussion

_Growing a Language_ had a few main themes. 
They were that when designing a language, creating a "pattern" is key to usability and speed for programmers. 
Also, that fluency is important and that a language should be well definied. 
This was especially exemplified by the entire talk defining a language made up of single syllable words. 
Lastly, he describes that a language should be a mode of discussion between a user and the bits that the language creates.  

We felt that these themes were the main themes of the sound lab as well. 
One goal of the lab was to allow for a better chaining of commands.
An obvious way to increase the volume and reverse the language helped to design a use pattern for our language.
Also, the old sound code required the addition of out.wav for all function calls but the first one, which does not follow an overall pattern.

Furthermore, when chaining commands, certain groups focused on changing the vocabulary used so as to make a more fluent API.

Lastly, (WHAT EXACTLY DID WE MEAN BY MODE OF DISCUSSION..)

---
 
**Question**


In what way is an API a language? 

**Response**
Ross
+ Fluency in expressions
+ Sytematic/Patterns
+ Design of both is an art&mdash;not a science
+ Allows you to interact with another entity
+ Both necessitate good naming choices

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**
Anthony
+ It should be interactive: have users vote (maybe)
+ Names make a huge difference in usability
+ Need to weigh pros and cons&mdash;especially compatibility issues
+ There are many ways to do the same thing

The post on grayscale brought up some unique ideas about API design and its process.
One interesting idea was that maybe API design should be interactive with the user.
When determining if the command should be gray, white, black, or rgb, it might be advantageous to have prospective users vote or survey different communities for input.
We also learned about the process of API naming and how difficult it seems. 
Anthony could personally imagine debating for hours over whether to chose black, white, or rgb due to the different tradeoffs.
This also leads to the idea of weighing pros and cons. 
While designing an API, often there are multiple decisions that might hold benefits over others, like being consistent with the base language, yet have drawbacks, like compatability issues, as discussed in the post.

Overall, I think the post really offers insight on how there are many options to chose from when desiging an API and sometimes you either should pick and deal with the consequences or ask for user input. 





---

**Question**

The Yang and Rabkin article talks mainly about general-purpose languages. In 
what ways do the themes apply to the study and creation of DSLs?

**Response**
Ross
---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other 
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:


> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
[[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**
Anthony
+ There needs to be a good balance
   + It's important to have fluency and naturalness, but also have a very strict
     less optionful language. It doesn't need to read like Shakespeare, but it
     shouldn't read like Perl.
+ Needs to be clear to a user that grammar may be broken
+ Maybe bring up should.js
+ Higher learning curve with non-natural language, but once you learn to think
  in a certain language, it seems more useful.
  + Perhaps bring up last weeks reading (Fowler): it shoud still feel like a
    programming language
+ Frustrating learning new syntax&mdash;especially syntactic "sugar"
+ Functionally meaningless words, although useful in creating a more
  natural read, are not necissarily helpful to programmers writing
   + Find balance between adding keywords to just make sense verse over-clutter
     and vague choices



The two experiences of natural languages are definitely at odds with each other.
If you create too natural of a language then syntax becomes too cluttered and harder to read.
However, a language lacking much resemblance to the english language might as well be greek symbols 
(Anthony speaks greek so maybe he would be able to read it). 

We both decided that some aspect of natural language should be included in the design of a DSL.
The main idea is there needs to be a good balance. 
When designing a Domain Specific Language, fluency and naturalness are extremely important to not only get users using the language but also create an easy way to interact with the code.
There needs to be a balance with this though. There should definitely be a strict syntax that doesnt allow for too many words to be used sequentially.
Essentially, it doesnt need to read like Shakespeare (or a good author) but it definitely shouldn't read like Perl or AWK. 
No matter what, it needs to be clear to the user that to maintain code readability, grammar may be broken sometimes. 

There are benefits of non-natural languages though. 
Even though there might be a higher learning curve with one, once you learn to think in a certain language/style it seems useful and more efficient. 
Even Fowler said a language should still feel like a programming language not just English.

To complicate the issue even more, both natural languages and non-natural languages suffer from syntax obstacles.
One issue we have with Perl is that the following piece of code exists and is expected to be readable:

print((($line=join("",<>))=~s/.*\n/index($`,$&)>=$[?"":$&/ge&&$line));

I am sure with enough time someone could figure out what this says but honestly this shouldnt exist. 
The Natural-language equivalent is adding in so many filler words to create Grammer that the code is cluttered and you cant get a good idea of what is happening without reading a paragraph:

While MyGrades are above an 'A' continue to say "WOOO"
but if MyGrades is below an 'A' cry.

could be rewritten as

while(MyGrades > 'A'){
    print "WOOO"
}
print "Cry"

and the "code" is probably more readable since there are only 7 words compared to 18.

Essentially, both languages have syntax and "Syntactic Sugar" which nead to be understood before it can be written.
The best DSL design might be one that minimizes Syntactic Sugar while keeping the balance between natural and non-natural language in check. 


---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**
Ross

---
