# dtable-event.conf settings

## Database configuration

The configuration of database is in the `[DATABASE]` section of the file `dtable-events.conf`

```
[DATABASE]
type = mysql
host = db
port = 3306
username = root
password = seatable_db
db_name = seafile_db

```

## Redis configuration

The configuration of redis is in the `[REDIS]` section of the file `dtable-events.conf`

```
[REDIS]
host = redis
port = 6379

```

## Email notifications configuration

The configuration of email notifications is in the `[EMAIL SENDER]` section of the file `dtable-events.conf`

```
[EMAIL SENDER]
enabled = true

```


