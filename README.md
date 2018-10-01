PostgreSQL development scripts
==============================

### PG Build
Install dependencies (Ubuntu):
```shell
sudo apt-get install bison flex wget build-essential git gcc make zlib1g-dev libreadline7 libreadline-dev
```

### Usage

Go to your working directory
```shell
cd /home/username/dev/postgres
```

Set up `ENV`
```shell
. pg-set-env
```

Do some stuff
```shell
pg-configure
pg-initdb
pg-server start
```

Clean and rebuild all:
```shell
pg-rebuild
```
