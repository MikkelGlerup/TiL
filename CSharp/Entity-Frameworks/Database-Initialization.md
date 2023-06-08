# Code-First Database Initialization
![alt text](https://www.entityframeworktutorial.net/images/codefirst/database-init-fg1.PNG)

There are four different database initialization strategies:

#### CreateDatabaseIfNotExists:
This is the default initializer. As the name suggests, it will create the database if none exists as per the configuration. However, if you change the model class and then run the application with this initializer, then it will throw an exception.
#### DropCreateDatabaseIfModelChanges: 
This initializer drops an existing database and creates a new database, if your model classes (entity classes) have been changed. So, you don't have to worry about maintaining your database schema, when your model classes change.
#### DropCreateDatabaseAlways: 
As the name suggests, this initializer drops an existing database every time you run the application, irrespective of whether your model classes have changed or not. This will be useful when you want a fresh database every time you run the application, for example when you are developing the application.
#### Custom DB Initializer: 
You can also create your own custom initializer, if the above do not satisfy your requirements or you want to do some other process that initializes the database using the above initializer.
