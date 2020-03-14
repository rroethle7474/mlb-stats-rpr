Get notes for a given endpoint.

`statsapi.notes(endpoint)`

The result will include a list of required parameters, as well as hints for some endpoints.

If the specified endpoint has more than one distinct parameter requirement, for example one of teamId, leagueId, or leagueListId must be included for the attendance endpoint, the required query parameters list will contain separate sublists for each independent set of requirements:

`'required_params': [['teamId'],['leagueId'],['leagueListid']]`

Path parameters are part of the URL itself, for example the `teamId` parameter in the team endpoint (143 in the example):
`https://statsapi.mlb.com/api/v1/teams/143`

Query parameters are appended on to the URL after the question mark (`hydrate` in the example):
`https://statsapi.mlb.com/api/v1/teams/143?hydrate=league`

There is no difference in the way path and query parameters are passed into [statsapi.get()](https://github.com/toddrob99/MLB-StatsAPI/wiki/Function:-get).