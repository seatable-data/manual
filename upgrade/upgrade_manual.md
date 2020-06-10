# Upgrade manual

## Get latest SeaTable

You can find all versions of SeaTable from [Docker Hub](https://hub.docker.com/r/seafileltd/seatable/tags).

Run the following command to get the latest version of Seatable.

```
docker pull seafileltd/seatable:{tag}

```

Stop the currently running SeaTable container.

```
docker-compose down

```

Then modify the tag in "docker-compose.yml". And start a new SeaTable container.

```
docker-compose up -d

```

## Upgrade database

You need to execute the database upgrade statement one by one.

For example, upgrade from SeaTable 0.9.3 to SeaTable 0.9.6. 

After starting the SeaTable 0.9.6 container, you need to execute the database upgrade statement as follows：

```
docker exec -it seatable /bin/bash # Login to the SeaTable container. Then execute the upgrade statement

mysql -h$DB_HOST -p$DB_ROOT_PASSWD dtable_db </opt/seatable/seatable-server-latest/sql/mysql/upgrade/0.9.4/dtable.sql
mysql -h$DB_HOST -p$DB_ROOT_PASSWD dtable_db </opt/seatable/seatable-server-latest/sql/mysql/upgrade/0.9.5/dtable.sql
mysql -h$DB_HOST -p$DB_ROOT_PASSWD dtable_db </opt/seatable/seatable-server-latest/sql/mysql/upgrade/0.9.6/dtable.sql

```

## Start SeaTable server

Now you can start the SeaTable service. Execute the following command in the SeaTable container :

```
/shared/seatable/scripts/seatable.sh start

```


