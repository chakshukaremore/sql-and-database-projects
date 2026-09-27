# World Cup Database ⚽

A PostgreSQL database project that stores FIFA World Cup game and team
information and uses Bash scripts to import data and run SQL queries.

## 📌 Project Overview

The project contains World Cup data for the 2014 and 2018 tournaments.

Bash scripts are used to insert game data into PostgreSQL and retrieve
different statistics using SQL queries.

## 🔄 How It Works

1. The database tables are created using `worldcup.sql`.
2. `insert_data.sh` reads game data from `games.csv`.
3. Teams are added to the `teams` table if they do not already exist.
4. Game information is inserted into the `games` table.
5. `queries.sh` runs SQL queries to calculate World Cup statistics.
6. The results are displayed in the terminal.

## 🗄️ Database Structure

The PostgreSQL database is named `worldcup`.

It contains two tables:

### `teams`

Stores information about participating teams.

| Column | Description |
|---|---|
| `team_id` | Unique team ID |
| `name` | Team name |

### `games`

Stores information about World Cup games.

| Column | Description |
|---|---|
| `game_id` | Unique game ID |
| `year` | Tournament year |
| `round` | Tournament round |
| `winner_id` | ID of the winning team |
| `opponent_id` | ID of the opponent team |
| `winner_goals` | Goals scored by the winner |
| `opponent_goals` | Goals scored by the opponent |

## 🔗 Database Relationships

```text
Teams
  │
  ├── winner_id ───┐
  │                ↓
  │              Games
  │                ↑
  └── opponent_id ─┘

## 📊 SQL Analysis

The project uses SQL queries to calculate:

- Total goals scored by winning teams
- Total goals scored by both teams
- Average goals
- Maximum goals in a game
- Number of games where the winning team scored more than two goals
- 2018 tournament winner
- Teams that played in the 2014 Eighth-Final
- Unique winning teams
- Champions by year
- Teams starting with a specific prefix

## 📂 Project Files

### `insert_data.sh`

Bash script used to import World Cup game data into the PostgreSQL database.

### `queries.sh`

Bash script containing SQL queries used to analyze the World Cup data.

### `worldcup.sql`

PostgreSQL database dump containing the `teams` and `games` tables,
data, primary keys, foreign keys, and constraints.

## 🛠️ Technologies Used

- Bash
- PostgreSQL
- SQL

## 🎓 Learning Source

This project was completed as part of the
[freeCodeCamp Relational Database curriculum](https://www.freecodecamp.org/learn/relational-database/).
