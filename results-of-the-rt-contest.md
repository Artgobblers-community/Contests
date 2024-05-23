The mechanism for summarizing the results is as follows: from all participants admitted to the contest, we compiled a final list. Each admitted participant is mentioned in it a number of times equal to their multiplier (for example, @Neo_Arts9 (x3) - three times, and @P1u3mm (x1) - once).
The list of participants and their multipliers is in the picture:
![list](https://gyazo.com/d42ccb561dd0500a728b659489e6c05c.png)

We have a total of 20 participants, the sum of their multipliers = 25, which means there are 25 items in the final list,

Here is the final list:
------------
[@Neo_Arts9, @MazzyZhang, @RYuki_79, @victorfuror_eth, @Feld4014, @notablebuyer, @SWHEATZ1, @Lamenthyst, @Sea2538, @luis17284254, @eminnisa_, @SawariART, @merdan_kadyrow, @P1u3mm, @le___Clochard, @uglydewdropper, @being0496, @a..., @d..., @Cherrynekonya, @Neo_Arts9, @Feld4014, @notablebuyer, @a..., @Neo_Arts9]
------------

As a source of randomness, we will use hashes of Ethereum transactions.
We will sign three empty transactions from our multisig. After their confirmation, we will take the hash of each transaction and convert it into a decimal number.

This can be done using Python code:

![python](https://gyazo.com/ee7cfd39804f7b0cc741570137c53d47.png)
![python](https://gyazo.com/0be576dca9454636e30519ed4e76689e.png)

or using any [online converter](https://www.rapidtables.com/convert/number/hex-to-decimal.html):

![converter](https://gyazo.com/eee9d16368507a38d96b754c2b24a985.png)

After that, we will divide this decimal number by the number of items in our list (25), and we will take the remainder of the division as the index of the winner in the list.

For example, if the remainder of the division of the first number is equal to 0, 20, or 24, then @Neo_Arts9 wins, if 13, then @P1u3mm.

Remember: the first index of the list is 0, the last is 24.

After determining the first winner, we will remove all his mentions from our list, recount the number of items, divide the hash of the second transaction by the number of its items, and so on.

In this way, we will determine three winners.

The transactions will be signed shortly. Good luck!

---------
Hashes and results will be listed below:
