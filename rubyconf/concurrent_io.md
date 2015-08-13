# Keeping Your Site Responsive By Offloading I/O

## Track?

Fundamentals

## Abstract

This is a presentation on a few approaches you can use to simultaneously
interact with multiple services that are required to produce output from your
Ruby application to speed things up.

## Description

For this presentation, I'll assume that you know some Ruby, that you
are at least familiar with the terminology of threads, services, and concurrent
programming, and that you want to make your application or web site
much, much faster.

I had a mission at my company, and that was to increase the speed of
our Sinatra application.  SEO implications were at stake!  At the
time, we were querying multiple web services (NoSQL services), and we
were doing them one after another.  What a shame...

I wandered down multiple roads during this journey.  I looked at Threads,
Fibers, Eventmachine, and Curl::Multi.  This talk will touch on the pros and
cons of each approach while running within a Ruby application server.

Mission accomplished!  Our site is much faster now.  Let me show you
the lessons learned and circumstances where you'd want to use each of
them.
