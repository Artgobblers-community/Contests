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

first tx: https://etherscan.io/tx/0x7ed9504fae2ed75aa5fbc0fbe36009e13511e1adcbbadbaec18fd4ff0dc1dbb1
hash: 0x7ed9504fae2ed75aa5fbc0fbe36009e13511e1adcbbadbaec18fd4ff0dc1dbb1
decimal: 57375379022435612397988675978967748143970989204556517738954035121126360865713
remainder of the division: 57375379022435612397988675978967748143970989204556517738954035121126360865713 % 25 = 13, first winner - @P1u3mm

---------

New list (without @P1u3mm): [@Neo_Arts9, @MazzyZhang, @RYuki_79, @victorfuror_eth, @Feld4014, @notablebuyer, @SWHEATZ1, @Lamenthyst, @Sea2538, @luis17284254, @eminnisa_, @SawariART, @merdan_kadyrow, @le___Clochard, @uglydewdropper, @being0496, @a..., @d..., @Cherrynekonya, @Neo_Arts9, @Feld4014, @notablebuyer, @a..., @Neo_Arts9] (indexes from 0 to 23)

second tx: https://etherscan.io/tx/0xf1fff37dfac52a3358ccd5d4ce654a2318306d2ffba83e57f84c621845f5c10e
hash: 0xf1fff37dfac52a3358ccd5d4ce654a2318306d2ffba83e57f84c621845f5c10e
decimal: 109459623030850472933139970945407045061303252476663494741369798308414906286350
remainder of the division: 109459623030850472933139970945407045061303252476663494741369798308414906286350 % 24 = 22, second winner - @a... | ilidan.eth

---------

New list (without @a...): [@Neo_Arts9, @MazzyZhang, @RYuki_79, @victorfuror_eth, @Feld4014, @notablebuyer, @SWHEATZ1, @Lamenthyst, @Sea2538, @luis17284254, @eminnisa_, @SawariART, @merdan_kadyrow, @le___Clochard, @uglydewdropper, @being0496, @d..., @Cherrynekonya, @Neo_Arts9, @Feld4014, @notablebuyer, @Neo_Arts9] (indexes from 0 to 21)

third transaction: https://etherscan.io/tx/0xab57516626d65f7b90b2a1c8d689740173d82f07eb94f67322c5017757d5128c
hash: 0xab57516626d65f7b90b2a1c8d689740173d82f07eb94f67322c5017757d5128c
decimal: 77499774597832976945511774490584846488702132563841240445369894381787416957580
remainder of the division: 77499774597832976945511774490584846488702132563841240445369894381787416957580 % 22 = 4, third winner - @Feld4014 | mrbayc.eth

Each winner will receive 0.1 eth. Thank you all for participating in the contest!



