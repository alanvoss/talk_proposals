# Better Regular Expressions (from a Perl Guy)

## Track?

Beyond Ruby (because this isn't really limited to Ruby) or Fundamentals

## Abstract

Do you think regular expressions are black magic? Do you do a
lot of string manipulation, parsing, or searching? Ever cared
to know what is happening behind-the-scenes with your regular
expression engine, or how you can make your expressions better?

## Details

Any developer with beginning to intermediate regular expression
knowledge would likely benefit in knowing how it all works, how
one can improve expressions to be more readable and predictable,
and how to have fun by exploring this (not so ancient) art.

In this discussion, I'll show you the basics of how a regular
expression engine generally functions, when to use it (and as
importantly, when not to do so), and some tricks you can employ
(hopefully mostly non-production ones) to get thing finished
quickly.

General outline:
- how the engines basically work
- modifiers
- anchors
- greed
- backreferences
- backtracking
- efficiency considerations
- readability
- tools available to help write better regular expressions
- tools which utilize regular expressions (sed, vim,
  language-du-jour, etc.)
- other tips and tricks

I'll gladly share the slides from the last time I did a similar
talk at a PerlMongers group upon request.

## Pitch

In general, I think Regular Expressions aremisunderstood and
misused frequently.  In the Perl community, where I came from
immediately prior to Ruby, they are much more a part of the
culture than in Ruby, in my admittedly small experience.  I
think Ruby developers would appreciate knowing how the engine
works and how they can utilize them better.

I've spoken on this topic multiple times at multiple regional
meetups, and I've given lightning talks focusing on tips and
tricks of regular expressions at a few YAPCs.  I'm an outgoing
guy, with little stagefright (former karaoke performer, but keep
that on the down-low), and I love teaching others how to do
things better and generally giving back to the communities that
have given me so much.
