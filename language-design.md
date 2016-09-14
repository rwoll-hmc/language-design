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

1. Finding the Balance in Creation: Cathedral versus Bazaar

> The key point is that in the bazaar style of building a program or designing a
> language or what you will, the plan can change in real time to meet the needs
> of those who work on it and use it. This tends to make users stay with it as
> time goes by;they will take joy in working hard and helping out if they know
> that their wants and needs have some weight and their hard work can change the
> plan for the better [Steele, 1998]

The idea from this quote that when designing a language, you should try to be
flexible really resonates with me. It reminds me of the two types of software
development strategies, Agile and Waterfall. With Agile designing, you don't
over specify the design from the start so it is able to easily change. However,
when designing a DSL, I almost feel a "Waterfall" approach is better, so that as
you implement your language, you dont forget your design goals. We have
discussed that as too many features are added to a DSL, it becomes so saturated
that it essentially becomes a general-purpose language and a "Waterfall"
approach might help stop that.

2. Technical Wizards: The Dangers of Magic

> The problem is that programming languages are created either by committee or
> by extreme technical wizards with magical math powers. The broad computer
> science academic community has not paid a tremendous amount of attention to
> programming language usability. [Pavlus, 2012]

This quote sums up some of the issues Programming Languages have with fluency
and usability. Essentially, these languages are created by extremely smart
people who might not understand how a non-developer might interact with the
language. A simple example of this is reading Racket. It may seem to make sense
after learning about Lambda Calculus and the theory of functional programming;
however, to a regular user, it can be rather complicated esspecially if you want
to create usable programs for others.   

3. Documention: Need versus Purpose

> **APIs should be self-documenting**: It should rarely require documentation to
> read code written to a good API. In fact, it should rarely require
> documentation to write it. [Bloch, 2006]

> **Documentation matters.** No matter how good an API, it won't get used
> without good documentation. Document every exported API element: every class,
> method, field, and parameter. [Bloch, 2006]

We are including this "quote" since we thought it was slightly contradictory.
Clearly the point is that a language/API should not be complicated to use while
still being documented; however, he states it should rarely require
documentation to write it while also requesting very detailed and complete
documentation. Obviously there should be some sort of documentation but maybe
it shouldn't be the focus so as to create better self-documenting languages.
Maybe this is a question of trade-offs and what is possible with the fixed
budget/time constraints.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

It is much easier to spot a poorly-designed language than a well-designed
language. While there are certain principles that can help you spot a
well-designed language there is a variable of time that can lessen its "wellness".

A well designed language should be approchable and "self-documenting". Just like
APIs you should be able to understand the code without constantly looking at
documentation once you know the pattern. This leads me to a second point:
well-designed languages must have an overall pattern as the first paper mentioned.
Extensions and built-in flexibility/customization of a language should be natural
and fit in with the rest of the language.

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

_Growing a Language_ had a few main themes They were that when designing a
language, creating a "pattern" is key to usability and speed for programmers.
Also, that fluency is important and that a language should be well definied.
This was especially exemplified by the entire talk defining a language made up
of single syllable words. Lastly, he describes that a language should be a mode
of discussion between a user and the bits that the language creates.  

We felt that these themes were the main themes of the sound lab as well. One
goal of the lab was to allow for a better chaining of commands. An obvious way
to increase the volume and reverse the language helped to design a use pattern
for our language. Also, the old sound code required the addition of `out.wav`
for all function calls but the first one, which does not follow an overall
pattern.

Furthermore, when chaining commands, certain groups focused on changing the
vocabulary used so as to make a more fluent API.

Lastly, (WHAT EXACTLY DID WE MEAN BY MODE OF DISCUSSION..)

---

**Question**

In what way is an API a language?

**Response**

Application Programming Intefaces are fundamentally subsets of a language. APIs
serve to act as a (limited) system of communication&mdash;the definition of a
language itself. It's not strictly about the end result either&mdash;there needs
be a sense of flucency and "APIs should be self documenting" and "should rarely"
require documentation to read code written in a good API" [Bloch, 2006]. If you
think about natural language, this is also true: once you have a basic
understanding of a language, you rarely need to look words up in a dictionary
since context most of the time can give you enough information to figure out the
definition you are after. APIs (or at least good ones) being languages have this
property.

The way APIs generally come to be reflects their nature as languages: we rarely
coin words we don't need or have nothing to describe; new features of APIs
usually come from a repeated pattern that could otherwise be said more
succinctly with a single API call&mdash;of course there are verbose ways to
circumlocute, but the API removes that need.

APIs, although ultimately consumed by computers, need to have some human element
to them, and with that point: **words matter**. Just because we can use the word
`cats` to mean `dog`, it wouldn't make much sense. It breaks a pattern, which
APIs being languages *should* have, and it's confusing to a human who already
has a set of associations in their head. In Verou's article about a choice for
a CSS "grayness" function, we can see this play out in a more applicabale
scenario.

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

The post on grayscale brought up some unique ideas about API design and its
process. One interesting idea was that maybe API design should be interactive
with the user. When determining if the command should be gray, white, black, or
rgb, it might be advantageous to have prospective users vote or survey different
communities for input. We also learned about the process of API naming and how
difficult it seems. Anthony could personally imagine debating for hours over
whether to chose black, white, or rgb due to the different tradeoffs. This also
leads to the idea of weighing pros and cons. While designing an API, often there
are multiple decisions that might hold benefits over others, like being
consistent with the base language, yet have drawbacks, like compatability
issues, as discussed in the post.

Overall, I think the post really offers insight on how there are many options to
chose from when desiging an API and sometimes you either should pick and deal
with the consequences or ask for user input.

---

**Question**

The Yang and Rabkin article talks mainly about general-purpose languages. In
what ways do the themes apply to the study and creation of DSLs?

**Response**

Yang and Rabkin make a point how "[o]ur stereotypes are often wrong" with the
example assumption "older developers are outmoded–and that they know older,
outmoded languages" which they point is statistically incorrect based off of
Ari and Meyerovich 2011 study. When designing and creating DSLs, we must be
extremelely aware of who are users are and not assume that we know anything
about them. Just because we think something may be more intuitive for them, does
not, by any means, mean that it will be. This is definitely one of the most
critical yet challenging principles of design. As we discussed in the Hive
workshop, we naturally jump to associations and personal experiences when
listening to the experiences and desires of others&mdash;Yang and Rabkin remind
us to step back from these stereotypes.

This quote captures this sentiment quite succinctly:

> These stereotypes come about because programmers confuse their strong views
> about languages with their views about the *users* of the languages.

The theme of practicality also is raised: people learn languages based off a
necissity be it an institutional curriculum or a financial incentive. DSLs by
extension must be created with the domain of the domain in mind.

---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other
words, people found it easier to work with code that looks more like a human
language (e.g. English). Consider the following quote by William R. Cook, one of
the creators of AppleScript:


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

The two experiences of natural languages are definitely at odds with each other.
If you create too natural of a language then syntax becomes too cluttered and
harder to read. However, a language lacking much resemblance to the english
language might as well be greek symbols (Anthony speaks greek so maybe he would
be able to read it).

We both decided that some aspect of natural language should be included in the
design of a DSL. The main idea is there needs to be a good balance. When
designing a Domain Specific Language, fluency and naturalness are extremely
important to not only get users using the language but also create an easy way
to interact with the code. There needs to be a balance with this though. There
should definitely be a strict syntax that doesnt allow for too many words to be
used sequentially. Essentially, it doesnt need to read like Shakespeare (or a
good author) but it definitely shouldn't read like Perl or AWK. No matter what,
it needs to be clear to the user that to maintain code readability, grammar
may be broken sometimes.

There are benefits of non-natural languages though. Even though there might be a
higher learning curve with one, once you learn to think in a certain
language/style it seems useful and more efficient. Even Fowler said a language
should still feel like a programming language not just English.

To complicate the issue even more, both natural languages and non-natural
languages suffer from syntax obstacles. One issue we have with Perl is that the
following piece of code exists and is expected to be readable:

```
print((($line=join("",<>))=~s/.*\n/index($`,$&)>=$[?"":$&/ge&&$line));
```

I am sure with enough time someone could figure out what this says but honestly
this shouldnt exist. The Natural-language equivalent is adding in so many filler
words to create Grammer that the code is cluttered and you cant get a good idea
of what is happening without reading a paragraph:

While MyGrades are above an 'A' continue to say "WOOO"
but if MyGrades is below an 'A' cry.

could be rewritten as:

```
while(MyGrades > 'A'){
    print "WOOO"
}
print "Cry"
```

and the "code" is probably more readable since there are only 7 words compared
to 18.

Essentially, both languages have syntax and "Syntactic Sugar" which nead to be
understood before it can be written. The best DSL design might be one that
minimizes Syntactic Sugar while keeping the balance between natural and
non-natural language in check.

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**
Ross

Both Ross and Anthony completed the reading independently and then met up to
have an offline conversation about the readings. During this conversation, we
brainstormed some responses to the above questions and then divided the actual
expansion of that brainstorm session to be done independently with the plan
to peer review eachother's works ammending and appending to the answers.

---
