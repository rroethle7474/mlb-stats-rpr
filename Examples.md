> *Note*: These examples were previously included in the README file.

### Print the number of games won by the Oakland Athletics in 2018

Use `statsapi.schedule()` to retrieve all A's games for 2018,
and use `sum()` to count records in the resultset where the A's were the winning_team.

```
print('The A\'s won %s games in 2018.' % sum(1 for x in statsapi.schedule(team=133,start_date='01/01/2018',end_date='12/31/2018') if x.get('winning_team','')=='Oakland Athletics'))
```
-----
### Print the linescore for all games the Phillies won in July 2008

Use `statsapi.schedule()` to retrieve all games for July 2018,
run the resulting dict through a list comprehension
to iterate over the records where the Phillies are the winning team,
and feed the `game_id` into `statsapi_linescore()`.

```
for x in [y for y in statsapi.schedule(team=143,start_date='07/01/2008',end_date='07/31/2008') if y.get('winning_team','')=='Philadelphia Phillies']:
    print('%s\nWinner: %s, Loser: %s\n%s\n\n' % (x['game_date'], x['winning_team'], x['losing_team'], statsapi.linescore(x['game_id'])))
```
-----
### Print the Phillies 40-man Roster on opening day of the 2018 season

Use `statsapi.get('season')` to retrieve the dates for the 2018 season,
feed the opening day date into `statsapi.roster()`.

```
print('Phillies 40-man roster on opening day of the 2018 season:\n%s' % statsapi.roster(143,'40Man',date=statsapi.get('season',{'seasonId':2018,'sportId':1})['seasons'][0]['regularSeasonStartDate']))
```
-----
### Print the boxscore and linescore from the A's most recent game (which may be in progress or may not have started yet based on MLB response to 'last game' request)

Use `statsapi.last_game()` to retrieve the most recent A's game
and feed the gamePk into `statsapi.boxscore()` and `statsapi.linescore()`.

```
most_recent_game_id = statsapi.last_game(133)
print(statsapi.boxscore(most_recent_game_id))
print(statsapi.linescore(most_recent_game_id))
```
-----
### Find the team with the longest name

Use `statsapi.get('teams')` to retrieve all active team names,
then feed into max() to find the longest value and its length

```
longest_team_name = max([x['name'] for x in statsapi.get('teams',{'sportIds':1,'activeStatus':'Yes','fields':'teams,name'})['teams']],key=len)
print('The team with the longest name is %s, at %s characters.' % (longest_team_name, len(longest_team_name)))
```
-----
### Print the standings from July 4, 2018

Use `statsapi.standings()` with the `date` parameters

```
print(statsapi.standings(date='07/04/2018'))
```
-----
### Print the top 5 team leaders in walks for the 2008 Phillies

Use `statsapi.team_leaders()`

```
print(statsapi.team_leaders(143,'walks',limit=5,season=2008))
```
-----
### Print the top 10 all time career leaders in doubles (NOTE: The extra 8949 records come back in the data from MLB)

use `statsapi.league_leaders()`

```
print(statsapi.league_leaders('doubles',statGroup='hitting',statType='career',limit=10))
```
-----
### Print Chase Utley's career hitting stats

use `statsapi.get()` to call the sports_players endpoint for the 2008 World Series,
lookup Chase Utley's person id from the results, and pass it into `statsapi.player_stats()`
using `type='hitting'` and `group='career'`

```
print( statsapi.player_stats(next(x['id'] for x in statsapi.get('sports_players',{'season':2008,'gameType':'W'})['people'] if x['fullName']=='Chase Utley'), 'hitting', 'career') )
```
-----
### Print a list of scoring plays from the 4/28/2019 Marlins @ Phillies game

```
print( statsapi.game_scoring_plays(567074) )
```
