# Deploy SeaTable Pro with Docker

## Getting started

### Install docker-compose

SeaTable image uses docker-compose. You should first install the docker-compose command.

```bash
# for CentOS
yum install docker-compose -y

# for Ubuntu
apt-get install docker-compose -y

```

### Download the SeaTable images

Login the Seafile private registry and pull the SeaTable image:

```
docker login {host}
docker pull {host}/seafileltd/seatable-server:{tag}

```

You can find the private registry information on the [customer center download page](https://customer.seafile.com/downloads/).

### Download and modify docker-compose.yml

Download [docker-compose.yml](https://docs.seatable.io/f/22cf6f7dc3c84940a1c4/?dl=1) sample file to your host. Then modify the file according to your environtment. The following fields are needed to be modified:

* The password of MySQL root (MYSQL_ROOT_PASSWORD and DB_ROOT_PASSWD)
* The volume directory of MySQL data (volumes)
* The SeaTable image's tag
* The volume directory of SeaTable data (volumes)
* The time zone (Optional)

### Start docker container

Start SeaTable container with the following command:

```bash
docker-compose up -d

```

**NOTE: You should run the above command in a directory with the **`docker-compose.yml`**.**

### **Create databases**

Run the following command to create the required databases in the mysql container : ccnet_db,seafile_db,dtable_db

```
for database in {ccnet_db,seafile_db,dtable_db}; do docker exec -it seatable-mysql /usr/bin/mysql -u root -pMYSQL_ROOT_PASSWORD -e "create database ${database} character set = 'utf8';"; done

```

**NOTE: Replace the "MYSQL_ROOT_PASSWORD" with your MySQL password.**

Then run the following command to create the required data table :

```
docker exec -it seatable /shared/seatable/scripts/run.sh init-sql

```

### Generate configuration files for SeaTable

Run the following command to generate configuration files for SeaTable :

```
docker exec -it seatable /shared/seatable/scripts/run.sh init

```

After running the above command, the following configuration files will be generated in the SeaTable data directory :

* ccnet : `/Your SeaTable data volume/seatable/conf/ccnet.conf`
* seafile : `/Your SeaTable data volume/seatable/conf/seafile.conf`
* dtable-web : `/Your SeaTable data volume/seatable/conf/dtable_web_settings.py`
* dtable-server : `/Your SeaTable data volume/seatable/conf/dtable_server_config.json`
* Nginx : `/Your SeaTable data volume/seatable/conf/nginx.conf`

### Start SeaTable server

Now you can start the SeaTable service.

```
docker exec -it seatable /shared/seatable/scripts/run.sh start       # Start SeaTable service.
docker exec -it seatable /shared/seatable/scripts/run.sh superuser   # Create an admin account.

```

Next you can access SeaTable via the web side.

### Put your licence file(seafile-license.txt)

If you have a `seafile-license.txt` licence file, simply put it in the volume directory of SeaTable data. If the directory is `/opt/seatable/seatable-data` So, in your host machine:

```
cp /path/to/seafile-license.txt /opt/seatable/seatable-data/seatable/
docker exec -it seatable /bin/ln -s /shared/seatable/seafile-license.txt /opt/seatable/

```

Then restart the SeaTable server:

```
docker exec -it seatable /shared/seatable/scripts/run.sh restart

```

## More configuration Options

### Add the SSL certificate

1. Upload the SSL certificate file to the SeaTable data directory : `/Your SeaTable data volume/ssl/`
2. Change the "http" of each URL in ccnet.conf, dtable_web_settings.py and dtable_server_config.json to "https".
3. Restart the SeaTable service : `docker exec -it seatable /shared/seatable/scripts/run.sh restart`
4. Modify the nginx configuration file : `/Your SeaTable data volume/seatable/conf/nginx.conf`

   e.g.

   ```
   server {
       if ($host = example.seatable.com) {
           return 301 https://$host$request_uri;
       }
       listen 80;
       server_name example.seatable.com;
       return 404;
   }

   server {
       server_name example.seatable.com;

       listen 443 ssl;
       ssl_certificate /shared/ssl/<your-ssl.cer>;
       ssl_certificate_key /shared/ssl/<your-ssl.key>;

       proxy_set_header X-Forwarded-For $remote_addr;
       ......

   ```

5. Reload the nginx configuration file : `docker exec -it seatable /usr/sbin/nginx -s reload`

### Advanced Features

All config files are under `/Your SeaTable data volume/seatable/conf/`. 

After modification, you need to restart the SeaTable server.

```bash
docker exec -it seatable /shared/seatable/scripts/run.sh restart

```

### Find logs

The SeaTable logs are under `/shared/seatable/logs` in the docker, or `/Your SeaTable data volume/seatable/logs` in the server that run the docker.

The Nginx logs are under `/shared/nginx-logs`, or `/Your SeaTable data volume/nginx-logs` in the server that run the docker.

## SeaTable directory structure

### Volumes

Placeholder spot for shared volumes. You may elect to store certain persistent information outside of a container, in our case we keep various logfiles and upload directory outside. This allows you to rebuild containers easily without losing important information.

* /shared/seatable: This is the directory for SeaTable server configuration and data.
* /shared/nginx-logs: This is the directory for Nginx logs.
* /shared/ssl: This is directory for SSL certificate.

## Upgrading SeaTable server

To upgrade to latest version of SeaTable server:

```sh
docker login {host}
docker pull {host}/seafileltd/seatable-server:{tag}
docker-compose down

```

Then modify the tag in docker-compose.yml.

Finally start the container.

```
docker-compose up -d
docker exec -it seatable /shared/seatable/scripts/run.sh start

```


