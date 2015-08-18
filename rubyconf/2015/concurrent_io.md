# Keeping Your Site Responsive by Offloading I/O

## Track?

Fundamentals

## Abstract

Feeling like your Ruby application could use a speed boost?
Sometimes, the hare does beat the tortoise.  We'll look at interfacing 
with external services via Threads, Fibers/EventMachine, and Curl::Multi,
and reasons for using each of them to help win the race.

## Details

For this presentation, I'll assume that you know some Ruby, that
you are at least familiar with the terminology of threads, services,
and concurrent programming, and that you want to make your
application or web site much, much faster.

I had a mission at my company, and that was to increase the
speed of our Sinatra application. SEO implications were at stake!
At the time, we were querying multiple web services (NoSQL services),
and we were doing them one after another. What a shame...

I wandered down multiple roads during this journey. I looked at
Threads, Fibers, Eventmachine, and Curl::Multi. This talk will
touch on the pros and cons of each approach while running within
a Ruby application server.

Mission accomplished! Our site is much faster now. Let me show you
the lessons learned and circumstances where you'd want to use each of them.

General outline:
1. Threads
  - MRI considerations
    - timeslicing
    - GIL
  - Can execute code while waiting on requests
2. Reactor Pattern
  - Eventmachine
    - Only one event loop per process
    - Recommended separate thread in applications
      - Lose a lot of gains due to timeslicing in MRI
  - Fibers
  - can execute code while waiting on requests
3. Curl::Multi (via the Curb gem)
  - uses lightning-fast curl c library
  - can't execute any other code while waiting
  - can only do http requests
4. Trade-off discussion

## Pitch

Most companies and developers desire a site that is fast and responsive.
There are lots of ways to approach this, and I've taken a deep-dive
into several of them, as I was given a lot of research latitude in
order to improve performance.  Our site was slow, and we needed to
speed things up.
