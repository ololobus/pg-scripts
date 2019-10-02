PostgreSQL development scripts
==============================

### Dependencies

Install dependencies (Ubuntu)
```shell
sudo apt-get install bison flex build-essential gcc make zlib1g-dev libreadline7 libreadline-dev
```

You may require some extra deps:
```shell
sudo apt-get install libicu-dev libgss-dev libkrb5-dev libxml2-dev libxslt1-dev libldap2-dev tcl-dev \
                     lcov libzstd-dev libssl-dev \
                     python-dev libpython-dev \
                     perl libperl-dev libdbi-perl cpanminus
```

### PG build

Get Postgres sources
```shell
git clone https://github.com/postgres/postgres.git
```

Go to your working directory
```shell
cd postgres
```

Set up `ENV`
```shell
. pg-env set
```

Do some stuff
```shell
pg-configure
make -j -s && make -j -s install
pg-initdb
pg-server start
```

Clean up and rebuild everything
```shell
pg-rebuild
```

### Out-of-source build
Get Postgres sources
```shell
git clone https://github.com/postgres/postgres.git
```

Go to your working directory
```shell
mkdir postgres_build && cd postgres_build
```

Set up `ENV`
```shell
. pg-env set
```

Do some stuff
```shell
pg-configure /path/to/postgres/sources
make -j4 -s install
initdb
pg-server start
```

```shell
createdb
psql
```
