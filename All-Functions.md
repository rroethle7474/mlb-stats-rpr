## Core functions
* [statsapi.get](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-get) - make calls directly to MLB StatsAPI endpoints; supports the most flexibility in request parameters, and returns raw json data
* [statsapi.meta](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-meta) - retrieve available values from StatsAPI for use in other queries, or look up descriptions for values found in API results
* [statsapi.notes](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-notes) - retrieve notes for a given endpoint, including a list of required parameters, as well as hints for some endpoints (returns info from MLB-StatsAPI module only, no calls to StatsAPI endpoints)

## Functions that return formatted text
* [statsapi.boxscore](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-boxscore) - generate a formatted boxscore for a given game
* [statsapi.game_highlights](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-game_highlights) - generate a formatted list of highlights with video links for a given game
* [statsapi.game_pace](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-game_pace) - generate a formatted list of pace of game information for a given season (back to 1999)
* [statsapi.game_scoring_plays](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-game_scoring_plays) - generate a formatted list of scoring plays for a given game
* [statsapi.last_game](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-last_game) - get the game id for the given team's most recent game
* [statsapi.league_leaders](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-league_leaders) - generate a formatted list of stat leaders for current or specified season
* [statsapi.linescore](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-linescore) - generate a formatted linescore for a given game
* [statsapi.next_game](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-next_game) - get the game id for the given team's next game
* [statsapi.player_stats](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-player_stats) - generate a formatted list of a player's career or season stats
* [statsapi.roster](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-roster) - generate a formatted list of players on a team's roster
* [statsapi.standings](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-standings) - generate a formatted list of standings for a given league/date
* [statsapi.team_leaders](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-team_leaders) - generate a formatted list of a team's leaders for a given stat

## Functions that return data in a Python dictionary
* [statsapi.boxscore_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-boxscore_data) - generate a dict containing boxscore data for a given game
* [statsapi.game_highlight_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-game_highlight_data) - returns a python list of highlight data, including video links, for a given game
* [statsapi.game_pace_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-game_pace_data) - returns a python dict of pace of game information for a given season (back to 1999)
* [statsapi.game_scoring_play_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-game_scoring_play_data) - returns a python dict of scoring play data for a given game
* [statsapi.league_leader_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-league_leader_data) - returns python list of stat leader data for current or specified season
* [statsapi.lookup_player](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-lookup_player) - get a list of player data based on first, last, or full name, jersey number, current team Id, position, etc.
* [statsapi.lookup_team](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-lookup_team) - get a list of teams' info based on the team name, city, abbreviation, or file code
* [statsapi.player_stat_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-player_stat_data) - returns a python dict of a player's career or season stats, along with some biographical information
* [statsapi.schedule](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-schedule) - retrieve a list of games on a given date/range and/or team/opponent
* [statsapi.standings_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-standings_data) - returns a python list of standings data for a given league/date
* [statsapi.team_leader_data](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-team_leader_data) - returns a python list of a team's leader data for a given stat