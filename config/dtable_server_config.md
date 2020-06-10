# DTable Server Config

## private_key

The `private_key` must be the same as the `DTABLE_PRIVATE_KEY` in `dtable_web_settings.py` 

The `dtable_web_service_url` must be the same as the `DTABLE_WEB_SERVICE_URL` in  `dtable_web_settings.py` 

```
{
    "host": "db",
    "user": "root",
    "password": "MYSQL_PASSWORD",
    "database": "dtable_db",
    "port": 3306,
    "private_key": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
    "dtable_web_service_url": "https://example.seatable.com/",
    "redis_host": "redis",
    "redis_port": 6379,
    "redis_password": ""
}

```

The `redis_password` is an empty string.
