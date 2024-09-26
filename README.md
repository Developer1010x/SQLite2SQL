# SQLite to MySQL SQL Dump Converter

## Overview
This script provides a utility to convert an SQLite database into a MySQL-compatible SQL dump file. It supports the conversion of table structures and data, with options to customize the output according to your needs.

## Features
- **Converts** SQLite database tables to MySQL format.
- **Exports** table structures and data in a single SQL dump file.
- **Supports options to:**
  - Include or exclude `DROP TABLE IF EXISTS` statements.
  - Export only the structure, only the data, or both.
- **Graceful handling** of user interruptions (Ctrl+C).

## Requirements
- **Python 3.x**
- **SQLite3 module** (included with Python standard library)
- A **MySQL database** to import the generated SQL dump.

## Installation
1. Clone or download this repository.
2. Ensure you have Python 3.x installed on your system.
3. Navigate to the directory containing the script.

## Usage
To run the script, use the following command:

```bash
python sqlite_to_mysql.py <sqlite_db_file> [mysql_dump_file] [--no-drop] [--export-mode MODE]
```



Parameters
<sqlite_db_file>: Path to the SQLite database file you want to convert.
[mysql_dump_file]: (Optional) Path to the output MySQL SQL dump file. If not provided, it will use the SQLite database filename with a .sql extension.
--no-drop: (Optional) Prevents the inclusion of the DROP TABLE IF EXISTS statement in the SQL dump. By default, this statement is included.
--export-mode MODE: (Optional) Choose the export mode:
structure: Only exports the table structure.
data: Only exports the data.
both: Exports both structure and data (default mode).
Example
To convert an SQLite database named example.db to a MySQL dump named example.sql, run:

bash
```
python sqlite_to_mysql.py example.db example.sql
```
To export only the structure without the DROP TABLE statements, use:

bash

$ ```python sqlite_to_mysql.py example.db --no-drop --export-mode structure```


Handling Interruptions

If you need to stop the conversion process, you can press Ctrl+C. The script will detect this and exit gracefully without leaving the output file in an inconsistent state.

License

This project is licensed under the MIT License. See the LICENSE file for more information.

Contributing

Contributions are welcome! If you have suggestions for improvements or find bugs, please submit an issue or pull request.

Contact

For any questions or feedback, please contact me

m

