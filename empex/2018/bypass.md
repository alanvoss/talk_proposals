# Bypass Your External Dependencies

## Abstract

Calling external services during testing is often not practical or even possible. Perhaps your build machine is on an isolated network, the external service has no test environment, or integration tests introduce a latency bottleneck into your tests. Mocking is possible, but part of your production code won't be executed during tests, and you want to ensure everything works. How about using a stand-in local server that will not only properly check and handle your responses, but will also verify certain route requests are performed the appropriate number of times. Bypass to the rescue.

## In Two Sentences

Uncomfortable with mocks for testing calls to external services? Having a simple server emulate responses and count routes is a great alternative.

## Target Audience

Intermediate users of Elixir who've struggled with various mocking strategies.

## Length of Talk

20 or 40 minutes

## Given Talk Before?

No

## Other Presentation Experience

I have given many talks at local meetups (Perl, Ruby, and Elixir), but I have yet to speak at a national conference, and I welcome the opportunity.
