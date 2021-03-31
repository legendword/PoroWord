---
sidebar: auto
---

# Commands

PoroWord's prefix is `lol`. Make sure to use the format `lol [command]` when using commands.

## init

- Usage: `lol init`

Initializes the bot in the text channel of this message.

**Please call this command when running the bot for the first time in your server.**

## join

- Usage: `lol join`

Initializes the user's coins and other data. **Must be run before the user can use any of the rest of the features.**

After joining, the user will receive 1000 coins.

## link

- Usage: `lol link [summonerName]`
- Alternative Usage: `lol add [summonerName]`
- Arguments:
    - `summonerName`: Your summoner name in League of Legends. Currently only supports NA summoners.

Links the summoner with your Discord account. A summoner **must be linked** for the bot to detect your game state and retrieve match information.

## coins

- Usage: `lol coins`
- Alternative Usage: `lol c`, `lol info`

Shows your current number of coins, and your active bets on games.

## leaderboard

- Usage: `lol leaderboard`
- Alternative Usage: `lol lb`

Shows the current server leaderboard: the top 5 users with the most coins.

## list

- Usage: `lol list`

Lists ongoing games and game states. Shows whether a game is currently open for betting or past betting phase. Only games from summoners linked to users in the server will be shown here.

## bet

- Usage: `lol bet [betOption] [amount]`
- Shortcut Usage: `lol bet [w/l] [amount] [answer]`
- Arguments:
    - `betOption`: Can be one of the following
        1. `w`: Bet on Win. (The player's team will win this game.)
        2. `l`: Bet on Loss. (The player's team will lose this game.)
        3. `b`: Answer the bonus question.
        4. The Bonus Question Code: Same as betOption `b`
    - `amount`: The amount of coins to bet (for Win/Loss), or the answer to the bonus question (the answer will always be numeric).
    - `answer`: The answer to the bonus question.

Make a guess at the outcome of the game. Only available at the start of a match, after a notification is sent in the channel.

The coins will be deducted from your pocket and put in the coin pool of this game. If you did not guess correctly, your coins will be lost. If you guessed correctly, you will get all of your betted coins back, plus your share of the coins others have lost. This will happen when the said game ends. The bot will automatically split the winning amount into equal shares for everyone who won.

At the end of the game, the bot will also evenly split the bonus coins between those who got the closest answer to the bonus question. This is the primary source of coins if you lost too much! So always try to guess the answer!

#### Using the Shortcut

The shortcut performs two actions in one command. First, you bet on Win/Loss `[w/l]` with `[amount]` coins. Second, you answer the bonus question `[answer]`.