# Lahman Baseball Database Exercise

## 1. What range of years for baseball games played does the provided database cover? 


```js
SELECT namefirst || ' ' || namelast AS player_name,
	height AS height_in,
	g_all AS num_games_played,
	teams.name AS team_name
FROM people
LEFT JOIN appearances 
USING(playerid)
LEFT JOIN teams
USING(teamid, yearid)
WHERE playerid IN (SELECT playerid FROM people ORDER BY height LIMIT 1);

```

## 2. Find the name and height of the shortest player in the database. How many games did he play in? What is the name of the team for which he played?

```js
const { highlight } = require('sql-highlight')

const sqlString = "SELECT `id`, `username` FROM `users` WHERE `email` = 'test@example.com'"

const highlighted = highlight(sqlString)

console.log(highlighted)

```
