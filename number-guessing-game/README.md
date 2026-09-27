# Number Guessing Game 🎯

A command-line number guessing game built using Bash and PostgreSQL.

The game generates a random number between 1 and 1000 and asks the player
to guess it. Player information and game statistics are stored in a
PostgreSQL database.

## 🎮 How It Works

1. The player enters their username.
2. The program checks whether the user already exists.
3. New users are added to the database.
4. Returning users can see their previous game statistics.
5. A random number between 1 and 1000 is generated.
6. The player keeps guessing until the correct number is found.
7. The number of guesses is stored in the database.
8. The game provides hints when the guess is too high or too low.

## 🗄️ Database Structure

The PostgreSQL database is named `number_guess`.

It contains two tables:

### `users`

Stores player information.

| Column | Description |
|---|---|
| `user_id` | Unique ID of the user |
| `username` | Player's username |

### `games`

Stores information about completed games.

| Column | Description |
|---|---|
| `game_id` | Unique ID of the game |
| `user_id` | ID of the player |
| `number_of_guesses` | Number of guesses taken |

The `games.user_id` column references `users.user_id` using a foreign key.

## 🛠️ Technologies Used

- Bash
- PostgreSQL
- SQL
- Linux/Unix Command Line

## 📂 Project Files

### `number_guess.sh`

The Bash script that:

- Takes the username as input
- Checks whether the user already exists
- Creates new users
- Retrieves previous game statistics
- Generates a random number
- Validates user guesses
- Provides higher/lower hints
- Counts the number of guesses
- Stores completed game results in PostgreSQL

### `number_guess.sql`

PostgreSQL database dump containing:

- Database creation
- `users` table
- `games` table
- Primary keys
- Foreign key
- Unique constraint on usernames
- PostgreSQL sequences

## 📚 Concepts Practiced

- Bash scripting
- Variables
- User input
- Conditional statements
- Loops
- Regular expressions
- Random number generation
- PostgreSQL database connection
- SQL `SELECT`
- SQL `INSERT`
- `COUNT()`
- `MIN()`
- Primary keys
- Foreign keys
- Unique constraints
- Relational database design

## 🎯 Learning Objective

The goal of this project was to practice integrating a Bash command-line
application with a PostgreSQL relational database while working with
user data and game statistics.

## 🎓 Learning Source

This project was completed as part of the
[freeCodeCamp Relational Database curriculum](https://www.freecodecamp.org/learn/relational-database/).

## 👩‍💻 Author

**Chakshu Karemore**

B.Tech Information Technology  
G. H. Raisoni College of Engineering, Nagpur
