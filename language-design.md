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

***Finding the Balance in Creation: Cathedral versus Bazaar***

> The key point is that in the bazaar style of building a program or designing a
> language or what you will, the plan can change in real time to meet the needs
> of those who work on it and use it. This tends to make users stay with it as
> time goes by; they will take joy in working hard and helping out if they know
> that their wants and needs have some weight and their hard work can change the
> plan for the better [Steele, 1998]

While flexibility as emphasized in this quote and throughout Steele's paper
are foundational to good software development and general-purpose programming
language development, we feel that a stricter approach when building out a DSL
is essential in avoiding feature-bloat. Anthony pointed out an analagous duality
of development styles prompted by this quote: Cathedral-Style is to Bazaar-Style
as the [Waterfall Model](https://en.wikipedia.org/wiki/Waterfall_model) is to
the [Agile Model](https://en.wikipedia.org/wiki/Agile_software_development).
The former one, through a deep design and requirement definition process,
produces a sort of master plan while the other is a more itereative,
adaptive approach even once building (or coding) has started. While the Agile
model can be extremley useful in more general software projects, for a DSL a
so-called "master plan" can be extemely useful.

While Ross mostly agrees with this analogy, he argues that the actual look and
feel of the developing DSL should be up for debate and evolving&mdash;especially
in its early days. Defining clear features and overall goals of what should be
"easy, difficult, and impossible" is important, but the syntax decisions should
be a more evolving component. As Steele mentioned in the quote above, the
iterative process, if done with care, not only serves to better the final
product, but it also serves to provide users "joy"!

***Technical Wizards: The Dangers of Magic***

> The problem is that programming languages are created either by committee or
> by extreme technical wizards with magical math powers. The broad computer
> science academic community has not paid a tremendous amount of attention to
> programming language usability. [Pavlus, 2012]

This quote embodies a fundamental issue with the devlopment of Programming
Languages: many programming languages were designed without the many possible
end-users who may use them. Instead, people build what they are comfortable with
and assume others are also comfortable with it. A simple example of this is
reading Racket. It may seem to make sense after learning about Lambda Calculus
and the theory of Functional Programming; however, to a non-expert user it can
be complicated, especially if you want to create usable *and* readable programs
for others.

Many times, it seems like programming languages are decorated with syntactic
*aspartame*&mdash;it's not syntactic *sugar* since it is just a language creator
adding unnatural, obfuscated, horn-tooting code (although some may argue it is
meant to write code more succinctly).

This dichotomy of committee-design versus technical wizard-design parallels the
first quote in which Steele contrasts Cathedral-style and Bazaar-style
development.

***Documention: Need versus Purpose***

> **APIs should be self-documenting**: It should rarely require documentation to
> read code written to a good API. In fact, it should rarely require
> documentation to write it.  
> [...]  
> **Documentation matters.** No matter how good an API, it won't get used
> without good documentation. Document every exported API element: every class,
> method, field, and parameter. [Bloch, 2006]

Anthony and Ross found these points regarding good API creation to be nearly
paradoxical. The point remains that APIs (or, in the more general case,
languages) should be easy and clear to use and read with and without
documentation. Is it better to invest time in designing self-documenting code
at the expense of thorough documentation, or vice versa?

Anthony and Ross suspect there is a trade-off between the two when given
budget and time constaints. In an ideal world, we would have perfectly
self-documenting code along with great documentation, but this may not always
be practical.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

It is much easier to spot a poorly-designed language than a well-designed
language. While there are certain principles that can help you spot a
well-designed language, time may be a factor in discovering a languages
shortcomings.

A well designed language should be approchable and "self-documenting." Just like
APIs you should be able to understand the code without constantly looking at
documentation once you know the pattern. This leads me to a second point:
well-designed languages must have an overall pattern as the first paper
mentioned [Steele, 1998]. Furthermore, as Steele explained, language extenstions
should feel natural and fit within the rest of the language. This provides a way
of future-proofing a language. It also serves to make the language more readable
and writable since patterns can be better maintained.

Bad languages are either hard to read or hard to write. For example, in Verou's
article regarding the choice of naming a "grayness" function, they raised the
issue of calling such a function `gray` with a percentage value since it is
not obviuous which means white and which means black. A lack of intuitiveness
in language makes it bad; intuitiveness coupled with expected behavior can make
it better.

Efficiency with features is key to a well-designed language. It's not helpful
to have 47 ways to express a for-loop since it makes the language inconsistent
and harder to read. In the case of AppleScript (see the quote in the
question below), there exist keywords solely to make things read more naturally,
but this serves to make it harder to write. In should.js, a JavaScript test
library that employs method chaining, one can add pointless keywords or omit
them; this is an interesting idea, but does not necessarily make the language
better. Here the flexibility has a trade-off with consistency of expression.

Anthony slightly disagrees with the statement on should.js. He really likes
the idea of a language where you can use optional statements to make it
more readable without the "syntactic aspartame" being necessary.

Well-designed languages should have errors in mind: not every program is going
to be perfect, so there needs to be an elegant way of handling errors. It should
not be an afterthought. However, this verges on prgamming language design versus
compiler design.

---

**Question**
How do the themes of _Growing a Language_ relate to the "sound lab" we did this week?

**Response**

In _Growing a Language_, there was an emphais on "patterns": creating a language
and use pattern is essential to usability, learnability, and extensibility. This
relates to the other theme of fluency. This was especially exemplified by the
entire talk defining a language made up of single syllable words. Steele
describes that a language should be a mode of discussion between a user and the
bytes that language creates.

We felt that these themes were the main themes of the sound lab as well. One
goal of the lab was to allow for a better chaining of commands: an obvious way
to increase the volume and reverse the sound helps to design a use pattern
for the language. Also, the old sound code required the addition of `out.wav`
for all function calls but the first one, which does not follow an overall
pattern&mdash;or at the very best creates an unfriendly pattern. Bad patterns
are worse than no patterns.

In the "sound lab", as partners attempted to redesign the language in a very
rushed amount of time, it felt as if we were coming up with a "master plan", or
in Steele's words a "Cathedral-style" design.

_Growing a Language_ also discussed the ability to extend a language which may
or may not produce natural-feeling results depending on the original language
design. When completing the "sound lab," groups seeemed to be thinking about
adding new types of functions/sound manipulations and how that would feel or
look in the API.

---

**Question**

In what way is an API a language?

**Response**

Application Programming Intefaces are fundamentally subsets of a language. APIs
serve to act as a (limited) system of communication&mdash;the definition of a
language itself. It's not strictly about the end result either&mdash;there needs
be a sense of flucency and "APIs should be self documenting" and "should rarely
require documentation to read code written in a good API" [Bloch, 2006]. If you
think about natural language, this is also true: once you have a basic
understanding of a language, you rarely need to look words up in a dictionary
since context (most of the time) can give you enough information to figure out the
definition you are after. APIs (or at least good ones) being languages have this
property. Context should be enough once you are somewhat familiar with other
parts of the API.

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

Furthermore, APIs are like languages in that they both require a unique grammar.
There needs to be a consistent way of communicating with the program throughout
the entire language or API.

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**


In Verou's post, the *process* of API design itself is extremely important and
must consider the user's intuition and ability to deduce functionality from
function names. It should be an interactive process that involves discussions
and polls of potential users. For example, when determining if the command
should be `gray`, `white`, `black`, or `rgb`, it might be advantageous to have
prospective users vote and survey different communities for input. Names in APIs
are difficult to create well and could have significant consequences in the
understandability of the API which extends to its adoption by developers.

Anthony could personally imagine debating for hours over whether to choose
`black`, `white`, or `rgb` due to the different tradeoffs. While designing an
API, often there are multiple decisions that might hold benefits over others.
For example, being consistent with the base language is valuable yet there might
be compatiability issues as discussed in the post.

Overall, I think the post really offers insight on how there are many options to
choose from when desiging an API: sometimes you either should pick an option and
deal with the consequences but we think gathering information from users is
essential as long as you are generally willing to consider it. Sometimes it is
impractical to please every user but as Bloch says "aim to displease everyone
equally. Most APIs are overconstrained."

---

**Question**

The Yang and Rabkin article talks mainly about general-purpose languages. In
what ways do the themes apply to the study and creation of DSLs?

**Response**

Yang and Rabkin make a point how "[o]ur stereotypes are often wrong" with the
example assumption "older developers are outmoded–and that they know older,
outmoded languages" which they point is statistically incorrect based off of
Ari and Meyerovich's 2011 study. When designing and creating DSLs, we must be
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
extension must be created with the domain *of* the domain in mind. Although we
can specify a domain like music composition or database programming, these
themselves are part of something larger.

Yang and Rabkin also shed light on how programmers have managed to "gender"
certain languages like C. Gendering a language makes no sense and is extremelely
harmful to many. It creates a divided and an unwelcoming environment for women,
who have&mdash;as the article points out&mdash;developed many iconic and widely
used programming languages. Also, Yang and Rabkin mention that "despite higher
numbers of women earning technical degrees, women make up 25% of the tech
workforce and less than 15% of the technical positions."

When we study DSLs and their design, we must be sure to build up a community
that genuinely reflects the potential users and not just the skewed representation
in industry. That community should value ideas and respect and hold eachother
accountable; the vulgar and mysogynistic comments in the article must be
condemned by the community at large and even the creators to dispel
language stereotypes.

Anthony wonders if we are requesting too much from a community of a DSL.

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
harder to read. However, a language lacking much resemblance to the English
language might as well be greek symbols. (Anthony speaks greek so maybe he would
be able to read it).

> As a side note, are there localized versions of programming languages that
> don't use English or have multiple options?

We both decided that some aspect of natural language should be included in the
design of a DSL. The main idea is there needs to be a good balance. When
designing a Domain Specific Language, fluency and naturalness are extremely
important to not only get users using the language but also create an easy way
to interact with the code. There
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
words to create grammar that the code is cluttered and you cant get a good idea
of what is happening without reading a paragraph:

While MyGrades are above an 'A' continue to say "WOOO"
but if MyGrades is below an 'A' "Cry".

could be rewritten as:

```
while(MyGrades > 'A'){
    print "WOOO"
} else {
  print "Cry"  
}
```

and the "code" is probably more readable since there are only 8 words compared
to 18.

Essentially, both languages have syntax and "syntactic sugar" which need to be
understood before it can be written. The best DSL design might be one that
minimizes syntactic sugar while keeping the balance between natural and
non-natural languages in check.

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

Both Ross and Anthony completed the reading independently and then met up to
have an offline conversation about the readings. During this conversation, we
brainstormed some responses to the above questions and then divided the actual
expansion of that brainstorm session to be done independently with the plan
to peer review eachother's works ammending and appending to the answers.

We then met again offline, and in a more pair-programming style, cleaned up and
added to the responses.

---
