# Insertica

Insertica will guess the schema of a JSON object, create a suitable table in the specified database, and then load the data into that table.

This gem could definitely use some optimization - it will probably not work well with a ton of data.

## Usage
```
Usage:
  insertica load FILENAME -p, --password=PASSWORD -u, --user=USER

Options:
  -u, --user=USER          # Specifies the username to use with Vertica.
  -p, --password=PASSWORD  # Specifies the password to use with Vertica.
  -h, [--host=HOST]        # Specifies the host of the Vertica database.
                           # Default: localhost
  -p, [--port=PORT]        # Specifies the port of the Vertica database.
                           # Default: 5433
  -s, [--schema=SCHEMA]    # Specifies which schema to use.

Load a delimited file into Vertica.
```

Example:
```
insertica load ./test/data/testdata.json -u admin -p password -s test_schema
```