# Python Dababase Connection Example

A Simple repository to show how to connect to a DB using Python.

## Python DB API

1. Run PostgreSQL docker container
2. Read python source code
3. Execute and test!

### Run DB

Run a Postgres docker container with the following command:

```bash
docker run \
  --name db \  # The name of the database container
  -e POSTGRES_PASSWORD=mysecretpassword \  # The DB superuser password
  -p 5432:5432  # The DB exposed port
  -d postgres:14-alpine
```

Now your DB is running. 
You can check with a database tool like [DBeaver](https://dbeaver.io/). Download it
and test your connection.

![DBeaver Connection Example](/assets/img/dbeaver-connection-example.png)

### Run Python Code

Create a virtualenv and install the Postgres adapter

```bash
pip install "pyscopg[binary]"
```

Execute python code

```bash
python db_example.py
```

Use DBeaver to explore tables and data. And explore `psycopg` to interact with DB and 
python code. 