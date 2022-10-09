# **RethinkDB GUIDE** 

# **Installation Guide**
## First of all you must download the docker 

You need to visit website : https://www.docker.com/ \
And download the docker.

After installation docker, you need to open it. \
If you want do same steps like me just follow my steps.

If you dont have git and any terminal. I would recommend to donwload. \
Git: https://git-scm.com/download/win \
Terminal: https://github.com/Eugeny/tabby/releases/tag/v1.0.184 

After you downloaded docker, git and terminal.\
You can start using the RethinkDB.

# **How to run RethinkDB?**
## Open terminal and make  directory, and follow the directory 
**make directory:**
```shell
mkdir nosql
```
**follow the directory:**
```shell
cd nosql
```
After those steps you must make file with name: 
**docker-compose.yaml**\
Into that file you need to write those strokes:
```yaml
version: '3.9'

services:
  rethinkdb:
    image: rethinkdb:2.4
    ports:
      - 8080:8080
    volumes:
      - ~/apps/rethinkdb/data:/app
```
**Dont forget save the file** 

## Now you can switch to terminal
and write that stroke into terminal:
```shell
docker compose up
```
**Congratulations now your database works**
## To use DB you need go to your browser
In search line you need to write that stroke
```
http://localhost:8080/
```
after those steps u can add some tables and databases.