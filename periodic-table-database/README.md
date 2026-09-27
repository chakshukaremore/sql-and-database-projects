# Periodic Table Database 🧪

A command-line application built with Bash and PostgreSQL for looking up
information about chemical elements.

The application accepts an element's atomic number, symbol, or name and
retrieves its details from a relational PostgreSQL database.

## 🔎 How It Works

The user provides an element as a command-line argument.

The program:

1. Checks whether an argument was provided.
2. Determines whether the input is an atomic number or text.
3. Searches the PostgreSQL database.
4. Uses SQL `INNER JOIN` operations to combine element information.
5. Displays the element's details in a readable format.
6. Shows an error message if the element is not found.

### Example

```bash
./element.sh 1
```markdown
## 🛠️ Technologies Used

- Bash
- PostgreSQL
- SQL

## 📚 Concepts Practiced

- Command-line arguments
- SQL queries
- INNER JOIN
- WHERE
- ILIKE
- Primary keys
- Foreign keys
- Unique constraints
- Relational database design

## 🎓 Learning Source

This project was completed as part of the
[freeCodeCamp Relational Database curriculum](https://www.freecodecamp.org/learn/relational-database/).
