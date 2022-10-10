# **RethinkDB GUIDE** 
# What is RethinkDB?
* **Open-source** database for building realtime web applications
* **NoSQL** database that stores schemaless JSON documents
* **Distributed** database that is easy to scale
* **High availability** database with automatic failover and robust fault tolerance 

RethinkDB is the first open-source scalable database built for realtime applications. It exposes a new database access model, in which the developer can tell the database to continuously push updated query results to applications without polling for changes. RethinkDB allows developers to build scalable realtime apps in a fraction of the time with less effort.
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
## If you want shutdown DB
* **Do Ctrl+C**

## To use DB you need go to your browser
In search line you need to write that stroke
```
http://localhost:8080/
```
after those steps u can add some tables and databases.

# **Workspace will look like that:**
![](https://rethinkdb.com/assets/images/docs/administration/webui.png)

# **Common commands for using the database**
## **To start editing you need to click on "Data Explorer"**
![](https://res.cloudinary.com/practicaldev/image/fetch/s--cg3IdP62--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/ojn9qt9slg0qokzeamym.png)
&nbsp;
## **Commands to work with Database**
### Create Database
```javascript
r.dbCreate('Ta20v');
```
### Drop Database
```javascript
r.dbDrop('Ta20v');
```
### List all Databases
```javascript
r.dbList();
```
&nbsp;
## **Commands to work with Tables**
### Create Table
```javascript
r.db('Ta20v').tableCreate('Class');
```
### Drop Table
```javascript
r.db('Ta20v').tableDrop('Class');
```
### List all tables in selected daatabase
```javascript
r.db('Ta20v').tableList();
```
### Create index in table / Also you can drop index etc.
```javascript
r.db('Ta20v').table('Class').indexCreate('Name');
```
&nbsp;
## **Commands to Writing Data**
### Insert data into table
```javascript
r.db('Ta20v').table("Class").insert({
    id: 1, // if you want set ur id / or u can remove those stroke to set primary key
    Name: "Aleksander",
    Age: "18"
})
```
### Update data in table
```javascript
r.db('Ta20v').table("Class").get(1).update({Name: "Sasha"});
```
### Replace data in table
```javascript
r.db('Ta20v').table("Class").get(1).replace({
    id: 1,
    Name: "Kolja",
    Age: "17",
});
```
### Delete data in table
```javascript
r.db('Ta20v').table("Class").get("1").delete(); // get(1) its id of element
```
# What kind of data can be inserted?
## State of ReQL data types
Official RethinkDB docs: https://rethinkdb.com/docs/data-types/

# What is the advantage of this database?
Rethink is a document-oriented database and it is a free and open-source distributed database. Basically, it is a JSON document with dynamic schemas, normally JSON is used to store the dynamic data that provides the real-time facility to update the database by using the query.

I’ll add on my own that it has a very user-friendly interface and you won’t get lost in it.They have very clear documentation on their website. And writing code is a pleasure because it is simple and somewhat similar to mysql.
# Conclusion
I really liked this database, and probably I will use it in the future to store information. :) \
If you missed something and didn’t add it, you can always go to their official website and read the documentation.
