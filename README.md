# express_RecreatingDatabase_Migration
An express app utilizing sequelize cli to connect to mySql workbench and recreating a database migration. 

COMMAND PROMPT

(1) Run the following to navigate to your Desktop: 

    cd Desktop

(2) Create a new folder on desktop: 

    mkdir Express

(3) Navigate to the Express directory: 

    cd Express

(4) Run the following command to install the Express generator globally onto your computer: 

    npm install express-generator -g

(5) Enter the following command to generate the Express starter app. This will set the view to use Handlebars and will name the app express_RecreatingDatabase_Migration: 

    express --view=hbs express_RecreatingDatabase_Migration

(6) Once the process is complete, navigate into the express_RecreatingDatabase_Migration directory: 

    cd express_RecreatingDatabase_Migration

(7) Now in the express_ directory, run the following: 

    npm install

(8) Install Nodemon globally: 

    npm install -g nodemon
    
(9) Install Nodemon as a devDependency in the package.json file within the express_ directory:

    npm install -save-dev nodemon
    
(10) Install mysql2:

    npm install --save mysql2

(11) Install sequelize: 

    npm install --save sequelize@5.15.1

(12) Open in VS code:

    code . 


VS CODE

(13) Navigate to the routes/index.js file: ![open index js file (express_Sequelize_RecreatingDatabase_Migration)](https://user-images.githubusercontent.com/35668707/68538862-10593880-0349-11ea-9d62-2585c802ce9e.JPG)

(14) Require mysql2 in routes/index.js file: ![require mysql2 in index js file (express_Sequelize_RecreatingDatabase_Migration)](https://user-images.githubusercontent.com/35668707/68538886-6ded8500-0349-11ea-9e2a-d8576e04328c.JPG)


COMMAND PROMPT

(15) Install Sequelize CLI commands globally onto your computer: 

    npm install -g sequelize-cli

(16) Create necessary sequelize folders and filed in project:

    sequelize init
 

VS CODE

(17) Open config/config.json file and change settings to connect to the database: ![open config js file (express_Sequelize_RecreatingDatabase_Migration)](https://user-images.githubusercontent.com/35668707/68538907-ad1bd600-0349-11ea-8874-ef37656232bd.JPG)

![update database info in config js file (express_Sequelize_RecreatingDatabase_Migration)](https://user-images.githubusercontent.com/35668707/68538910-d472a300-0349-11ea-94bd-4f251432f141.JPG)

COMMAND PROMPT

(18) Install mysql2 globally so sequelize CLI will be able to connect to the database:

    npm install -g mysql2
    
(19) Install sequelize-auto tool to generate model files: 

    npm install -g sequelize-auto

    
MYSQL WORKBENCH

(20) Open database in mySql workbench to view columns in table: 

COMMAND PROMPT

(21) Generate a model file for the actor table. (-h: IP/Hostname; -d: Database; -u: Username for database; -x: Password for database; -o: directory to place the models; -t: comma-seperated names of tables to import):  

    sequelize-auto -h localhost -d sakila -u root -x Password1! -o "./models" -t actor
    

VS CODE

(22) Open app.js file at the root of the project and include the './model" folder so that the models are available everywhere in the application: 


(23) Add models.sequelize.sync to app.js file: 

COMMAND PROMPT

(24) Globally install sequelize-auto-migrations tool:

    npm install -g sequelize-auto-migration
  
(25) Create initial migration: 

    makemigration --name initial_migration
    

VS CODE

(26) Add new property to models/actor.js file for migration: 

COMMAND PROMPT


NODEMON NOTE

Sometimes nodemon crashes in Windows 10 and there is a simple fix:

(1) Open Task manager (press Ctrl+Alt+Delete)

(2) Select the 'Processes tab'

(3) Search for 'Node.js: Server-side JavaScript'

(4) Select it and click on 'End task' button

Now you can run npm start.
