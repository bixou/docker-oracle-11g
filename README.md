## 🐳 docker-oracle-11g

Oracle Express Edition 11g Release 2 based on official image.
A script to create a custom DB is available in `docker/oracle/startup_scripts`

## ⬇️ Download & Installation

1. Download official Oracle XE from
[Oracle website](https://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/xe-prior-releases-5172097.html)

2. Move it to `docker/oracle`

3. Rename `docker-compose.dev.yml` to `docker-compose.yml`

4. Change SYSTEM password in `docker-compose.yml` as you want (default : PWD) then set your username & password for your DB in `docker/oracle/startup_scripts/01_create_db.sql`

5. Build & Launch Docker container with `docker-compose build && docker-compose up -d`

6. ...

7. Profit 🎉

## 📒 Logs

Access logs with `docker logs oracledb`
## 🚫 Error(s) in logs ?

>DATABASE SETUP WAS NOT SUCCESSFUL!

Maybe you have a rights problem on your docker volume. Execute `chown 1000:1000 .docker-volumes/oracledb` on your host then restart Oracle container

## 📌 TODO

Add possibility to define usernames/passwords in Docker environment variables to create several databases in one shot. 
