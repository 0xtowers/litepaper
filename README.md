# litepaper

Strategic vision one-pager, version 16th of Feburary 2024.

# Abstract

`Towers` or `0xtowers` is a coordination game played on decentralized smart
contract blockchains. The nature of the Towers game has "capture the flag"
dynamics in which players invest resources to capture more value collectively
than they put in themselves. Towers provides a protocol agnostic game factory so
that anyone can create games, promote them, and earn from their cash flow. The
game can be played with any ERC20 token.

# Game Dynamics

Each game has multiple towers. Each tower has a treasury. Players deposit ERC20
tokens into the tower treasuries. Depositing into a tower's treasury builds the
tower higher. Anyone can deposit any amount of tokens into any tower at any
point in time. The tower having the last deposit for a certain amount of time
wins the game, effectively capturing the treasuries of the losing towers.
Therefore players of a tower have to collaborate in order to fulfil the game's
winning conditions. The amount of time during which no more deposits happen is
configured with a countdown in number of blocks. Anyone making a deposit into
any tower is always resetting the countdown, effectively continuing the game and
preventing the currently leading tower from winning. A game might have different
game modes that modify the winning conditions. There are different game modes
described below.

* **Highest Tower** is the default game mode being played in each game. In this
  mode the highest tower wins. The tower height is determined by the number of
  deposits made into a tower's treasury. A tower is considered to be heighest if
  the second heighest tower has 1 - 3 deposits less for the countdown period.
* **Upside Down** is a game mode that has to be voted on during an ongoing game.
  Votes are bound to all players of the entire game. Every player has one vote.
  The simple majority activates the game mode. In this game mode the lowest
  tower wins. The lowest tower is determined by the fewest deposits made into a
  tower's treasury.
* **Final Rush** is a game mode that has to be voted on during an ongoing game.
  Votes are bound to all players of the entire game. Every player has one vote.
  The simple majority activates the game mode. In this game mode the most
  valuable tower wins. The most valuable tower is the one that contains the most
  amount of value within its treasury. This game mode is final with the
  countdown elapsing.
* **Queen's Gambit** is a game mode that has to be voted on during an ongoing
  game. Votes are bound to the players of the initiating tower. Every player has
  one vote. The simple majority activates the game mode. Players vote to remove
  one player from their own tower. The sacrifice of one of their own players
  effectively removes the player from the entire game. That game mode allows to
  punish mercenaries that try to play multiple sides. Players that get removed
  from the game cannot win and thus cannot claim rewards.

Once a game meets the required conditions for a tower to win the game, the game
can be ended by anyone. The game must be ended by someone in order for the
leading tower to win. The elapsed countdown does not cause the leading tower to
win automatically. Once a game ended, all players of the winning tower can claim
their rewards proportional to the contributions they made to the winning tower's
treasury. As an example, if all funds deposited into all towers add up to 1
million USD, and a single player contributed 10% of all funds to the winning
tower, then this particular player can claim 100 thousand USD in rewards.

# Marketing Utility

Communities of different projects, protocols and dapps may play against one
another as long as all participants can agree on a single token to be used.
Tokens with broader mindshare, memeability and scope may be preferred. For
instance L2 tokens like ARB or OP may be used during games in which Arbitrum
based or Optimism based communities play against one another. Similarly, DEGEN
might be used for Farcaster channel communities who want to compete in
coordination games against one another. Here the "headless marketplace" approach
that Farcaster Frames bring with them might be the optimal distribution
mechanism. `Towers` could be played right within a Frame without ever leaving
clients like Warpcast.

# Revenue Streams

Each game provides different actors with incentives for organizing and playing
the `Towers` game. The beneficiaries here are the winning players, tower owners
and the protocol. Each of these actors can provide a treasury address to capture
their share of deposits generated throughout each game. Note that the described
design enables decentralized frontends, which communities may provide for brand
aware experiences throughout the gameplay. Funds are distributed with each
deposit that is made within a game. One example of possible fund distribution
might be as follows.

* 90% of deposits go to the rewards treasury for players to claim
*  5% of deposits go to the tower treasuries as community kickback
*  5% of deposits go to the protocol treasury for further development

# Incentive Design

**DeFi Degens** are the players of the game. They want to play the game because
they can earn **rewards** in a "high risk high reward" fashion, if they manage
to coordinate and win the game. The more funds are deposited into the towers of
a game, the more reason players have to stay and keep playing as the stakes get
higher. This may attract more players until one tower succeeds eventually.

**DeFi Communities** are the partners of the game. They want to partner with
`Towers` because they can gain more additional **utility** for their own ERC20
tokens. Communities may play against one another to showcase the strength of
their community in a battle of coordination. This provides communities with
added **attention** to their own projects. Another benefit is, communities
collect **rewards** from the deposit volume generated by the game, whether their
towers win or lose.

# Technical Details

* Each game must at least have 2 towers. A game having 10 towers might not make
  much sense, but nothing prevents people from creating such games.
* Each deposit into any tower resets the countdown which is measured in a
  predefined amount of blocks. Once the countdown crosses 0 the game can be
  ended by anyone and the winners can claim their rewards.
* Depositing into the highest tower is limited in the default game mode. This is
  to prevent excessive bot activity. This is also to leave the second highest
  tower with a fighting chance to catch up.
* The game is protocol agnostic and therefore may be played with any ERC20
  token. Any game may only be played with a single token.
* There is a specified minimum amount required for deposits made during the
  game. Since Towers can be played indefinitely, the minimum deposit amount can
  be modified by the game owner in order to accommodate fluctuating token values
  over longer periods of time.
* There is no game specific token for the game. `Towers` is a protocol agnostic
  technology provider creating synergies between communities that want to engage
  in coordination battles.
* The game is likely to be played in a low transaction fee environment since the
  game dynamics require continuous contributions to the tower treasuries.
* Tower treasuries may configure zero addresses to effectively burn supply of
  their token if they chose to do so.
* Any technical detail laid out in this litepaper is likely to evolve over time
  as the development of the game platform progresses. That should especially
  hold true for control and voting mechanisms affecting the gameplay.
