PostgreSQL development scripts
==============================

### PG build
Install dependencies (Ubuntu):
```shell
sudo apt-get install bison flex wget build-essential git gcc make zlib1g-dev libreadline7 libreadline-dev
```

### Usage

Go to your working directory:
```shell
cd /home/username/dev/postgres
```

Set up `ENV`:
```shell
. pg-env set
```

Do some stuff:
```shell
pg-configure
make -j -s && make -j -s install
pg-initdb
pg-server start
```

Clean up and rebuild everything:
```shell
pg-rebuild
```
