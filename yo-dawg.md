# Yo Dawg

I herd u liek computers so I put a computer in your computer
so you can program while you program

???

First I'm going to define what I mean by personal computing.
Then I'm going to tell you that personal computing is terrible.
Then I'm going to talk about how we can fix it.

---

[citation needed]

???

I'm going to say a bunch of unsubstantiated stuff that's hopefully also
uncontroversial.

---

1. Personal computers are way faster than humans at data processing (4-7 decimal orders of magnitude)
1. Computers are going to get faster
1. Software is going to get slower

???

Why are we plowing all the performance gains of hardware back into higher-level
programming languages? Well, the advantage of higher-level languages is that
software can change faster, and it's more reliable. But the fact that we can
stomach the performance cost leads to the conclusion that...

---

Personal computing is as fast as it will ever *need to* be.

???

And therefore,

---

Personal computing is as fast as it will ever be.

???

The reason for this is pretty simple. Computers are getting more powerful,
but humans aren't. Information that humans interact with directly isn't getting
bigger or more complex.

We interact indirectly with a lot of very complex information, of course, but
when it comes to the types of media that individual humans can author with their
brains and comprehend with their brains, we're basically doing the same kinds of
stuff we were doing in the early 90s.

I'm talking about these types of media:

---

- Documents
- Spreadsheets (and other structured data)
- Drawings
- Photos
- Music
- Programs

???

We've been creating all of these things with personal computers for the last
30-ish years. And if all you do is the first 5, the last 30 years have been great,
right? But if you're a hobbyist programmer, or even a professional programmer,
you know that in those 30 years, the task of programming has become
grotesquely complex. As we've developed higher-level languages
and platforms, we've piled abstractions on top of abstractions with the goal
of minimizing the amount of attention we have to devote to lower-level stuff.
The problem is that those abstractions leak, and they're not balanced.

---

# Git

???

So, for example, Git. We often like to think that we can treat Git as this black box,
where you just memorize a set of commands and then you can magically track your
project's history and revert changes when stuff breaks. And that's great, but
the abstraction leaks, and sooner or later, you're going to run into a situation
where Git doesn't behave according to your mental model, and then you actually
have to understand how Git thinks about your data and how it works under the hood.

---

# Homebrew (or any package manager)

???

Or, another example, Homebrew, or insert your favorite package manager here.
Package managers present this great abstraction, where you can just name any
piece of software and they'll go get it for you and install it. But when they
don't work, because of misconfiguration or missing DLLs or whatever, you still
have to understand the underlying system or you don't have a hope of figuring out
what the problem is.

It seems like no matter how many abstractions we layer on, in order to really
be a competent programmer, you can't just master the top level.
You have to have some level of understanding of the
entire stack.

---

# Programming used to be a tool for the masses

```
10 PRINT BEN IS A POOPY HEAD
20 GOTO 10
```

???

I think this is really problematic, because programming used to be instantaneously
accessible to anyone who had access to a computer. Pretty much every computer
in the 80s came with some kind of interpreted language with a REPL where you
just type in commands and make stuff happen.

As the state of the art advanced, programming became less democratic.

---

> Look, it’s easy. Code everything in Typescript. All modules that use Fetch compile them to target ES6, transpile them with Babel on a stage-3 preset, and load them with SystemJS. If you don’t have Fetch, polyfill it, or use Bluebird, Request or Axios, and handle all your promises with await.
> —Jose Aguinaga, "How it feels to learn JavaScript in 2016"

???

This is nowhere more apparent than in the state of web programming today, where
a new tool or framework lands on Hacker News' desk every 6 hours, and it sometimes
feels like people will think less of you if you don't know them all.

It's all to easy to knee-jerk react to BS like this and say "abstraction is awful,
our tooling is awful, let's just burn it all down and go back to writing machine code."
Which I don't think is productive. The problem is not that abstraction is bad,
or that tools are bad. The problem is that *these particular abstractions are bad*.
They're leaky and unbalanced because there's no unifying vision
dictating how they should interoperate.

If you doubt this, you should read the article, and note how many of the tools
that Jose mentions are introduced to patch over shortcomings of other tools.

We're still do most of our programming on an OS that was designed for
mainframes. We've poured so much effort and care into creating amazing software
development tools, often on our personal time, but we haven't addressed the
elephant in the room: software development is complex because it happens atop
this precarious pile of unbalanced abstractions.

---

???

It's ironic that web programming should be in this state, because I think
the web browser is our greatest hope for rebalancing our abstractions. It's
a platform that runs everywhere, everyone has one, they're rock solid, and
these days their APIs are pretty consistent.

Not only that, but their APIs are powerful. Modern web browsers are very nearly
capable of anything that a desktop OS is capable of. That's the whole concept
behind Chrome OS.



---



---
