README

Tech stack:
  Front end:
    Framework: Angular 17
    Runtime: Node 20.10.0
   
  Back end:
    Framework: ASP dot net core 8
    Runtime: dotnet core 8.0.204

  Data:
    Database: Postgresql
    Proxy: Pgadmin4

CLI: [npm, ng, dotnet]

Bootstrapped UI: PRIMENG


1. To start front end server
  - Open VS Code, load front end project
  - Make sure download all dependencies
       run
          npm install
  - Then to start server, in CLI, type 
      ng serve

2. To start back end server
  - Open Visual Studio (preferably), or VS Code
  - In CLI, type
      dotnet run

3. Install postgresql, and its proxy, Pgadmin4. 
   If you have your own db, ignore this step.

4. Change the connection string at the backend if you are using a different db
   Connection string is at
     appsettings.json
       Then in
         DefaultConnection
       Change all its value as necessary, google for documentation to connect to the db of your choice
     


Optional (if your postgres database is empty):

To create migration file, where ORM maps the object from your source code and creates the tables in the database

1. Go to package manager console in Vs code/Visual Studio
   And add in this line
     Add-Migration InitialCreate
2. A folder will appear called "Migration"
3. To use the migration files to update your database, key into the Package Manager Console
     Update-Database
    

Documentation on migration:
https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=vs


