# Students Database

## Project Overview

This project uses Bash scripting and PostgreSQL to import student, major, and course data from CSV files into a relational database.

The script automates data insertion, checks for existing records, retrieves database IDs, and establishes relationships between majors and courses.

## Technologies Used

- Bash
- PostgreSQL
- SQL
- CSV files

## Database Structure

The project uses four tables:

- **students** — Stores student names, majors, and GPAs.
- **majors** — Stores academic majors.
- **courses** — Stores course names.
- **majors_courses** — Establishes relationships between majors and courses.

## Project Files

| File | Description |
|---|---|
| `insert_data.sh` | Bash script for importing data into PostgreSQL. |
| `students.csv` | Contains student names, majors, and GPAs. |
| `courses.csv` | Contains majors and their associated courses. |
| `README.md` | Documents the project and its usage. |

## How It Works

The Bash script performs the following operations:

1. Connects to the PostgreSQL `students` database.
2. Clears existing records from the relevant tables.
3. Reads `courses.csv` using a Bash `while` loop.
4. Checks whether majors and courses already exist.
5. Inserts missing majors and courses.
6. Retrieves their IDs and creates relationships in the `majors_courses` table.
7. Reads `students.csv` and extracts student
