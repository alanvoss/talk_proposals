# Art of the State

## Abstract

How does one store state in this immutable language? There are many ways to do so. You could go the traditional route, and utilize a database of some sort, or even built-in ETS.

Processes, though, are a great way to do such thing. You can use a vanilla recursive loop running inside a spawned Process, with some kind of receive block to peer inside, or one of the built-in wrappers around such a Process. This talk will talk about all of these, what is going on behind the scenes, and how and when to use them: Processes, GenServers, and Agents.

## In Two Sentences

How does one store and retrieve state in an immutable language? How can I store state with no assignment operator?

## Target Audience

Beginners to Elixir, who still might be struggling with the concept of immutability and how to store state, but also intermediate users, who wish they understood what was going on in the constructs they already use.

## Length of Talk

20 minutes.

## Given Talk Before?

Partially, at local meetup, though it was a modified version that talked mostly about how state machines are implemented.

## Other Presentation Experience

I have given many talks at local meetups (Perl, Ruby, and Elixir), but I have yet to speak at a national conference, and I welcome the opportunity.
