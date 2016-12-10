---
layout: post
title:  Effective JavaScript & How to behave when you sit next to Douglas Crockford
date:   2014-04-26 00:00:00 -0800
excerpt: Before I go into the most unique experience I had with Douglas Crockford, I want to put down the real essence of this post, which is the notes I took in the Effective JavaScript session that I attended. The most important thing I learnt in the training is the first line in my notes (the rest is secondary and you can actually skip it and move on to other things if you like).
---
Before I go into the most unique experience I had with Douglas Crockford, I want to put down the real essence of this post, which is the notes I took in the Effective JavaScript session that I attended. The most important thing I learnt in the training is the first line in my notes (the rest is secondary and you can actually skip it and move on to other things if you like).

> All work you do must stem from Service to Humanity

And,

* Programming Style is important. But style is not about personal expression via code.
* Write code that is easy to read, share, improve and expand upon.
* Look at programs as literary work
* We are paid to write programs that work well and are free of errors
* Read Thinking fast & slow by Daniel Kahneman
* There is no way of testing a program to check if it s 100% perfect, hence it’s all about perfection for programmers
* When people argue about something technical, they speak from an inner emotional space which may not be necessarily logical
* If someone says, “That hardly happens…“, they actually mean, “It happens!“
* The origin of word processing: Authors had no control over presentation
* CSS has lead to classitis and iditis
* In JavaScript, if you take this out, what you are left with is a functional programming language, which is great
* Use TitleCase only for constructor functions
* An activation record is created every time a variable is needed
* Closures are great coz they don’t keep variables in the stack, instead they keep it in the heap
* Avoid globals. In this statement, b is a global: var a = b = 0;
* Doug feels, Ken Thompson is the most amazing programmer ever. He created B, C, Regular Expressions, Unix, UTF-8 etc.
* Buffer overruns come from using ++. Hence use += instead.
* The Mosaic browser was instrumental in popularizing the world wide web. It was graphical, had support for multiple internet protocols, it displayed images inline (instead of separate windows)
* Objects in JavaScript work by the principle of differential inheritance where an object maintains a reference to its prototype from a table of properties. It creates a new property in the table only if it is different than its reference
* The splice command is slow
* 0.1 + 0.2 === 0.3 // this returns false as it s really difficult for the computer to represent certain floating point numbers. In this example, adding 0.1 and 0.2 actually results in 0.30000000000000004 which is not 0.3
* Choose to loop over Object.keys instead of for (var i in obj)
* Choose function expression over function statement
* JavaScript has function scope (not block scope) but block scope will be added in ES6
* Binding of this happens late (at invocation point) This is done to preserve memory
* If you do something like arr.push(fn), fn has access to arr as this (as arr is to the left of the period) This can be a security loophole
* Look up and read about Auguste Kerckhoff and his work
* Look up waterken which makes web services using the Actor model
* Learn about the Actor model
* The law of turns must be respected, hence avoid using the sync counterparts of the async functions of node.
* Douglas Crockford has created a new number type DEC64 which can represent decimal fractions with 16 decimal places which makes it well suited to apps that are concerned with money

OK, so here is the unique experience.

Firstly it was a 3 day event. On all 3 days, Douglas came in way before time and stood behind the podium and he looked like Gandalf was checking his email. At the beginning of day 2, he encountered some issues with his tablet and needed to replace it with his laptop which was at his residence. He looked around and asked most politely if anybody had a car and was willing to take him home to get his laptop and get it back just in time for the training. Now this is enough to prompt all the JavaScript programmers in the room to literally go into a frenzy. I mean this was not about 2 spaces in a tab OR 4... it was not about soft tabs OR hard, it was not about === OR == and it was certainly not about Angular OR React! This was about getting the opportunity to take Douglas Crockford to ‘his’ house and getting his laptop back in ‘your’ car.

I instantly raised both of my hands (and feet - conceptually) and screamed, 'Me! Pick Me!'. Rest of the people in the room were still adjusting to their seats and werent really aware what they had just lost by my instant response. Ok, needless to add but Doug did agree to let me drive him home. I had a bouncier bounce to my step while escorting him to my car. A million questions were racing through my mind. JavaScript questions, software questions... do you use Sublime or Atom or are you more of a emacs dude? Vim maybe? Do you think the framework that I am good at is the best framework of them all? Node.js or io.js? Should I start using ES6 right away or should I wait for this year to end? Is there a God? No kidding!

When we started toward his house I noticed there was some traffic on the freeway! Never was I so happy to be stuck in traffic!
So I started thinking on the lines of which question to ask first. As some time went by, the questions started melting away or falling apart. I told myself, this guy must’ve been asked all these questions so many times and in so many different ways by so many different people. No amount of rephrasing is going to add any novel juice to any of them. Besides how does it matter? All these  preferences and opinions that developers have. Why should one be better than the other. And even if it is, how much sense does it make to apply any of it without fully realizing it for your self. At the end of the day it’s all about how genuine you are as a human being.

I looked at him. Sitting there. Staring out of the window. I said to myself, **‘Fuck it!‘** I m not asking anything. He s probably going to be asked a whole lot of questions by the folks waiting back at the event anyway. One less inquisitive questioner may not make a massive difference but these 15 – 20 minutes can be made better for him instead of me. I just drove quietly. We went to his house. He picked his laptop and we drove back. No fanfare, no guru-disciple kinda drama. Nothing. Just a quiet drive. I cannot speak for him, but I had the most amazing time of my computing life for those 3 days.

There are some smart people out there who like to challenge Douglas Crockford’s opinions about JavaScript. In fact they use it as a tool to pronounce their smartness. They cannot create a [data exchange format](http://json.org/) that the world will adopt unanimously. Nor can they create [a number type that can aid in applications dealing with finances](http://dec64.com/). And of course they cannot possibly have the first hand [historic context](https://www.youtube.com/watch?v=v2ifWcnQs6M&list=PL62E185BB8577B63D) that he has. But they continue to think their understanding is way better than his. And I m not going to refute that. I m just gonna save up my questions for them :D