# Keeping Your Site Responsive By Offloading I/O

## Track?

Fundamentals

## Abstract

This is a presentation on a few approaches you can use to
simultaneously query multiple services that are required to produce
output from your Ruby application to speed things up.

## Description

For this presentation, I'll assume that you know some Ruby, that you
are at least familiar with the ideas of Threads and concurrent
programming, and that you want to make your application or web site
much, much faster.

I had a mission at my company, and that was to increase the speed of
our Sinatra application.  SEO implications were at stake!  At the
time, we were querying multiple web services (NoSQL services), and we
were doing them one after another.  What a shame...

At first, I approached with Threads. Why not try to take advantage of
Threads, even with the limitations of MRI and the Global Interpreter
Lock?  Executing each one of the requests in a separate Thread and
then joining afterward should do the trick.  Pros: works, fairly fast,
can do all of your I/O simultaneously, and can perform some Ruby
processing while waiting for other requests to finish.  Cons:
Timeslicing in MRI.

Next, I tried using Eventmachine to implement a Reactor Pattern along
with Ruby Fibers.  Why not throw all of your requests in an event
loop, and then finish executing code once all are finished?  Pros:
works, fast, as you aren't waiting for a timeslice before finishing,
can do most of your I/O simultaneously, and you can still execute some
Ruby code while other requests finish.  Cons: Eventmachine only allows
one loop per process, which is a real problem in application server
environments.

My final effort was to use Curl::Multi via the Curb gem.  Instead of
using Threads or Fibers, use the Curl libraries to fetch everything,
and then once all of the requests are finished, resume the code.
Pros: works, very fast, and cooperates with Ruby application servers
and Sinatra.  Cons: can't do any Ruby processing while waiting, and
can only do http-type requests simultaneously.

Mission accomplished!  Our site is much faster now.  Let me how you
the lessons learned and circumstances where you'd want to use each of
them.
