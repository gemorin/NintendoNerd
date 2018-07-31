# Nintendo NERD Challenges

I am not going to post code since that would defeat the purpose but here are some sample solutions

## [Challenge 1](https://www.nerd.nintendo.com/files/HireMe.cpp)
This one is not too difficult. It requires reversing the algorithm then applying a very common linear algebra algorithm.

First key found by my solver: `0x42,0x20,0x06,0x07,0x67,0x5c,0x5c,0x0f,0xee,0x0d,0xe7,0x89,0x60,0x00,0x8a,0x6c,0x25,0x50,0x77,0x60,0x1c,0xe7,0x27,0x31,0xfd,0xe4,0x7b,0x17,0x4e,0x8b,0xea,0x81b`

## [Challenge 2](https://www.codingame.com/open-challenge-go/nintendo)
The first step is to understand exactly what the problem really is and if you
have not taken maths or more theoretical CS classes in college, it might be
hard to figure out.  Here is a
[hint](http://blog.fkraiem.org/2013/11/30/polynomial-factorisation-over-finite-fields-part-1-squarefree-factorisation/) that will get you started if you're stuck.

The coding game website is pretty good but for some reason does not compile C++
with inlining (or any other kind of optimization).  Keep this in mind while
designing your code because it will be much slower on the coding game website.
This can be worked around by simply adding a GCC pragma in the code and
override the optimization options but I think it goes against the spirit.

[My solver](https://www.codingame.com/profile/19ba5595e8c4f25c5ccad920bc80857a3647602) takes about 450ms to run all the test cases on my iMac with -O2:
```
Solving 000073af 00000000
00000001 000073af
00000083 000000e5
000000e5 00000083
000073af 00000001

Solving 738377c1 00000000
00000001 738377c1
0000b0c5 0000cd55
0000cd55 0000b0c5
738377c1 00000001

Solving 46508fb7 6677e201
b0c152f9 ebf2831f
ebf2831f b0c152f9

Solving f3268b49 661859eb 0b324559 65ee6bda
0cf5c2bf 9aba68ef c18fb79b de70eef7
c18fb79b de70eef7 0cf5c2bf 9aba68ef

Solving a91db473 fcea8db4 f3bb434a 8dba2f16 51abc87e 92c44759 5c1a16d3 6111c6f4
a30d28bd bda19675 3f95d074 b6f69434 c58f4047 d73fe36a 24be2846 e2ebe432
c58f4047 d73fe36a 24be2846 e2ebe432 a30d28bd bda19675 3f95d074 b6f69434

Solving 541a4231 5d324646 27219a26 12497b0e 724eddcb 0e131617 9521bedf 55544dc7
c0def00d facef00d fee1dead feedface cafefeed feedf00d f00dfeed feedd00d
cafefeed feedf00d f00dfeed feedd00d c0def00d facef00d fee1dead feedface

Solving 4af6fc33 39029380 465c5267 c72f6a8b 0906e6d0 ca60550f 14a5e47c 42ad10fb 4a3bb446 bb74360a 5ea02b9c 23c68553 3fade253 e270ba24 39e141ad 6c38c43d
320a18d5 b61b13f6 1aaaa61c 0afe2a41 1a4ff107 84cc2efc 956ff31d fa595299 33749a7f 6cc9659d dc503569 ef4d0ef5 73b746c5 b8fb36d3 7616e9d6 b21251c4
33749a7f 6cc9659d dc503569 ef4d0ef5 73b746c5 b8fb36d3 7616e9d6 b21251c4 320a18d5 b61b13f6 1aaaa61c 0afe2a41 1a4ff107 84cc2efc 956ff31d fa595299
```
