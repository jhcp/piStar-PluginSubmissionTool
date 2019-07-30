### piStar Tool - Plugin Submission Tool
This is the tool used to submit new plugins to the [piStar Tool](http://www.cin.ufpe.br/~jhcp/pistar/), an app that let's you build diagrams using iStar language and many more!



Technologies used
- Backend framework: -> **Node.js**
- Database: **Redis** (for login session storage) and **Postgres** (for the rest)
- View: **Nunjucks** and **Materialize CSS**

#How to run locally (with Docker) on WIndows 10
- Install NodeJS and Docker
- Open the command prompt
- install postgres: 'docker run --name EntitiesDB -p 5432:5432 -d -t kartoza/postgis'
- install redis: 'docker run --name MemoryDB -p 6379:6379 -d -t redis'
- run both images: 'docker start EntitiesDB MemoryDB'
- check if both containers are active: 'docker ps'
- Open the project root folder in the command prompt
- run 'node src/index.js'
- access the website through localhost:3000


#How to run locally (without Docker) on WIndows 10
- Install NodeJS

## Set up PostgreSQL
- Install PostgreSQL. Take note of the username and password
- Set your PostgreSQL username and password in src/config/database.js
- Open the project root folder in the command prompt
- create the database: 'npx sequelize-cli db:create'
- create the tables: 'npx sequelize-cli db:migrate'

## Set up Redis
- how to install Redis??
- If needed, change its settings at src/server.js

## Run
- run 'node src/index.js'
- access the website through localhost:3000




todo:  --ignore './tmp/'  ???
