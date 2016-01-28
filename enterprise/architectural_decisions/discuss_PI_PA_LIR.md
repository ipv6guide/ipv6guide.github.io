---
title: Pros and cons of different address types
---
We have discussed different ways of getting IPv6 addresses to use in your
deployment: [from your ISP](use_PA), [provider independent](use_PI) or
[becoming an ISP for your own organisation](use_LIR). Here we put those
different options side by side and discuss why you would choose one or the
other.

The first thing to realise is that technically all these addresses are
equal. An address is just a number to use as source and destination in an
IP packet. The differences discussed here are only related to who is
responsible for addresses. These different responsibilities can affect
the way you use addresses, whether you are allowed to keep using addresses
after your contracts with ISPs change and whether it is possible to share
responsibility for routing between multiple ISPs. But in the end they are
all just numbers and one type of addresses is not better than another.

Because the choice of where to get your addresses is dependent on policies
and responsibilities there are many things influencing that choice. We
tried to put the most important aspects into one table to help you to
make the right choice.

In the table below
PI refers to [getting provider independent addresses](use_PI),
PA refers to [using addresses from your ISP](use_PA) and
LIR refers to [becoming an ISP for your internal organisation](become_LIR).

| Aspect                                              | PI  | PA  | LIR |
|:----------------------------------------------------|:---:|:---:|:---:|
| Connect to one ISP                                  |     |  +  |  -  |
| Connect to multiple ISPs                            |  +  |  -  |  +  |
| Change ISP often                                    |  +  |  -  |  +  |
| Don't change ISP often                              |     |  +  |     |
| Don't mind renumbering your network                 |     |  +  |     |
| You want to connect 3rd parties / customers         |  -  |     |  +  |
| You need a small block of addresses                 |  +  |  +  |     |
| You need a large block of addresses                 |  -  |  -  |  +  |
