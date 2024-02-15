# litepaper

Strategic vision one-pager, version 15th of Feburary 2024.

# Abstract

`Towers` or `0xtowers` is a coordination game played on decentralized smart
contract blockchains. The nature of the Towers game has "capture the flag"
dynamics in which players invest resources to capture more value collectively
than they put in themselves. Towers provides a protocol agnostic game factory so
that anyone can create games, promote them, and earn from their cash flow. The
game can be played with any ERC20 token and provides unique incentives for
ERC721 tokens that can be embedded into the game play.

# Game Dynamics

Each game has multiple towers. Each tower has a treasury in which ERC20 tokens
can be deposited. Depositing into a tower's treasury builds the tower higher.
Anyone can deposit any amount of tokens in any tower at any point in time. The
tower having the last deposit for a certain amount of time wins, effectively
capturing the treasuries of the other towers. Therefore players of a tower have
to collaborate in order to fulfil the game's winning conditions. The amount of
time during which no more deposits happen is configured with a countdown in
number of blocks. Anyone making a deposit into any tower is always resetting the
countdown, effectively continuing the game and preventing the currently leading
tower to win. A game might have different game modes that modify the winning
conditions. There are three different game modes.

* **Highest Tower** is the default game mode being played in each game. In this
  mode the highest tower wins. The tower height is determined by the number of
  deposits made into a tower's treasury. A tower is considered to be heighest if
  the second heighest tower has 1 - 3 deposits less for a certain amount of time.
* **Upside Down** is a game mode that has to be voted on during an ongoing game.
  In this game mode the lowest tower wins. The lowest tower is determined by the
  fewest deposits made into a tower's treasury.
* **Final Rush** is a game mode that has to be voted on during an ongoing game.
  In this game mode the most valuable tower wins. The most valuable tower is the
  one that contains the most amount of value within its treasury.

Once a game meets the required conditions for a tower to win the game, the game
can be ended by anyone. Once a game ended, all players of the winning tower can
claim their rewards proportional to the contributions they made to the winning
tower's treasury throughout the game. As an example, if all funds deposited into
all towers add up to 1 million USD, and a single player contributed 10% of the
funds within the winning tower, then this particular player can claim 100
thousand USD in rewards.

# Marketing Utility

NFT creators and NFT collectors can promote their art on the Towers platform.
One idea is to pledge an NFT to a particular game and in return earn fees on the
volume of the game being played. This provides artists and communities with two
particular benefits. First, exposure to a diverse audience, and second, an
additional revenue stream to their own discrecion. The NFT pledged to a game can
be claimed by a player of that particular game once it ended, given the player
became eligible for the claim.

Generative NFTs may be created and mutated by the "proof of work" that the game
play provides. As games are being played a lot of random data is produced which
can in theory be used to create generative art of a particular theme. That way
art may evolve on each deposit or on each epoch of the game.

Any form of utility may be combined with the NFTs associated with the game. More
creative ways of collaboration may be developed if certain synergies help our
ecosystem flourish.

# Revenue Streams

Each game provides different actors with incentives for organizing and playing
the towers game. The beneficiaries here are the winning players, tower owners
and the protocol. Each of these actors can provide a treasury address to capture
their share of deposits generated throughout each game. Note that the described
design enables decentralized frontends, which communities may provide for brand
aware experiences throughout each game. One example fund distribution, applied
to each deposit made within a game, might be as follows.

* 90% of deposits go to the rewards treasury for players to claim
*  5% of deposits go to the tower treasuries as community kickback
*  5% of deposits go to the protocol treasury for further development

```
90 + 5 + 5 = 100
```

# Incentive Design

**DeFi Degens** are the players of the game. They want to play the game because
they can earn **rewards** on a high risk high reward ratio if they win a game.
Further **NFTs** may be claimed. The more funds deposited into the towers of a
game the more reason people have to stay and keep playing as the stakes get
higher. This may attract more players until all but one tower of the game fall.

**DeFi Protocols** are the partners of the game. They want to partner with
Towers because they can **earn** fees from every game being played through their
own interfaces. Partner protocols can redirect attention of their own users to
playing the Tower game. They can then earn frees as the game creator in order to
bolster their own treasuries.

**DeFi Communities** are the partners of the game. They want to partner with
Towers because they can gain more additional **utility** for their own ERC20
token. Communities may play against one another where different communities own
different towers and thus play against one another. This provides communities
with added **attention** to their own project. Additional benefit for
communities owning towers of a game is that they collect **fees** from the
volume generated by the game.

**NFT artists** are the partners of the game. They want to partner with Towers
because they can get more **exposure** to a diverse audience for their art. Here
a little network effect may attract a greater **audience** because of the
additional benefit of claiming the game's NFT additional to the chance of
winning the game. For pledging NFTs to games NFT creators may become game or
tower owners in order to **earn** fees from the game being played.

# Technical Details

* Each game must have >= 2 towers. A game having 10 towers might not make much
  sense but nothing prevents people from creating such scenarios.
* Each deposit into any tower resets a countdown which is measured in a
  predefined amount of blocks. Once the countdown crosses 0 the game can be
  ended by anyone.
* The game is protocol agnostic and therefore may be played with any ERC20
  token. Any game may only be played with a single token.
* There is no game specific token for the game. `Towers` is a protocol agnostic
  technology provider creating synergies between existing projects.
* The game is likely to be played in a low transaction fee environment since the
  game dynamics require continous contributions to the tower treasuries.
* Tower treasuries may configure zero addresses to effectively burn supply if
  they chose to do so.
