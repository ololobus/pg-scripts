PostgreSQL development scripts
==============================

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
