# litepaper

Strategic vision one-pager, version 31st of August 2021.

# Abstract

`Towers` or `0xtowers` is a coordination game played on decentralized smart
contract blockchains. The nature of the Towers game has "capture the flag"
dynamics in which players invest resources to capture more value collectively
than they put in themselves. Towers provides a protocol agnostic game factory so
that anyone can create games, promote them, and earn from their cash flow. The
game can be played with any ERC20 token and provides unique incentives for
ERC721 tokens that can be embedded into the game play.

# Game Dynamics

Each game has multiple "towers". Each tower has a treasury in which ERC20 tokens
can be deposited. Anyone can deposit any amount of tokens in any tower at any
point in time. The goal of the game is to capture the treasury of the other
towers. Therefore players of a tower have to collaborate in order to fulfil the
game's conditions to win the game. A game has different game modes that define
the conditions that have to be met in order to win the game. There are three
different game modes.

* **Highest Tower** is the default game mode being played in each game. In this
  mode the highest tower wins. The tower height is determined by number of
  deposits into the tower. A tower is considered to be heighest if the second
  heighest tower has exactly one deposit less for a certain amount of time in
  which no more deposits are made to the game.
* **Upside Down** is a game mode that has to be voted on in a blind auction. In
  this game mode the lowest tower wins. The lowest tower is determined by the
  fewest deposits into a tower. After a certain amount of time without any more
  deposits to the game the lowest tower wins.
* **Final Rush** is a game mode that has to be voted on in a blind auction. In
  this game mode the most valuable tower wins after a certain amount of time.
  Here inactivity of deposits is no condition to win. All that matters is how
  much value a tower's treasury accrued.

Once a game meets the required conditions for a tower to win the game, the game
can be ended by anyone. Once a game ended all players of the winning tower can
claim their rewards proportional to the contributions they made to the winning
tower throughout the game. As an example, if all funds within a game's towers
deposited after fees amount to 1 million USD and a single player contributed 10%
of funds within the winning tower, then this particular player can claim 100
thousand USD in rewards. As another example, if there was a total volume of 1
million USD deposited into the tower's of a game, then the game creator has
earned 20 thousand USD given a 2% fee configured for the game creator.

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

Each game provides different actors with a share of the generated fees of the
played game. One beneficiary here is the protocol, another is the creator of the
game and the creators of the towers can provide a beneficiary address each. The
fee distribution for a game may look like this.

* 90% of deposits go to players who win the game
*  5% of deposits go to the protocol as a management fee
*  2% of deposits go to the game creator for promoting the game
*  1% of deposits go to the each tower creator given 3 towers

```
90 + 5 + 2 + (3 * 1) = 100
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
* The time it takes to determine a winning tower is measured in blocks. A number
  of blocks after which verification can happen is called an epoch.
* The game is protocol agnostic and therefore may be played with any ERC20
  token. Any game may only be played with a single token.
* There is no game specific token for the game. Towers is a protocol agnostic
  technology provider creating synergies between existing projects.
