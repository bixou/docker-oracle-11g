## 🐳 docker-oracle-11g

Oracle Express Edition 11g Release 2 based on official image.
A to create a custom DB is available in `docker/oracle/startup_scripts`

## ⬇️ Download & Installation

1. Download official Oracle XE from
[Oracle website](https://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/xe-prior-releases-5172097.html)

2. Move it to `docker/oracle`

3. Set your username & password for your DB in `docker/oracle/startup_scripts/01_create_db.sql`

4. Build & Launch Docker container with `docker-compose build && docker-compose up -d`

5. ...

6. Profit 🎉

## 📒 Logs

Access logs with `docker logs oracledb`
## 🚫 Error(s) in logs ?

>DATABASE SETUP WAS NOT SUCCESSFUL!

Maybe you have a rights problem on your docker volume. Execute `chown 1000:1000 .docker-volumes/oracledb` on your host then restart Oracle container