PostgreSQL development scripts
==============================

### Dependencies

#### Linux (Debian)

Install dependencies:
```shell
sudo apt install bison flex build-essential gcc make zlib1g-dev libreadline7 libreadline-dev
```

You may need some extra deps:
```shell
sudo apt install libicu-dev libgss-dev libkrb5-dev libxml2-dev libxslt1-dev xsltproc \
                     lcov tcl-dev libzstd-dev libssl-dev libldap2-dev gettext \
                     python-dev libpython-dev \
                     perl libperl-dev libdbi-perl cpanminus
```

Packages for documentation:
```shell
sudo apt install libxml2-utils docbook docbook-xml fop dbtoepub
```

#### macOS

Minimal dev dependencies:
```shell
brew install bison flex make perl
```

```shell
cpan IPC::Run
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
