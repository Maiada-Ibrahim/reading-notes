# Room
## Save data in a local database using Room
## What is Room?
Room is an ORM (object relational mapper) for SQLite database in Android. It is part of the Architecture Components released by Google. At its core, all the code that you write related to Room will eventually be converted to SQLite code. Room allows you to create and manipulate database in Android more quickly. See it as an abstraction layer on top of inbuilt SQLite database.
so the benift Compile-time verification of SQL queries,Convenience annotations that minimize repetitive and error-prone boilerplate code,Streamlined database migration paths


to use Room

- add the dependencies
The database class that holds the database and serves as the main access which The class must be annotated with a @Database,and must be an abstract class that extends RoomDatabase.

- Data entities that represent tables in your app's database.

- Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database

- create an instance of the database
AppDatabase db = Room.databaseBuilder(getApplicationContext(),
        AppDatabase.class, "database-name").build();

        UserDao userDao = db.userDao();
       List<User> users = userDao.getAll();




# Defining data using Room entities
- use Room entities to define the database schema without writing any SQL code

- define each Room entity as a class using @Entity

- If you want the table to have a different name use @ColumnInfo annotation to the field and set the name property

- annotate a single column with @PrimaryKey or define a composite primary key by listing those columns in the primaryKeys property of @Entity

- If an entity has fields that you don't want to persist use @Ignore

- for search for details in your database's tables. Use full-text search

- add the @Fts3 or @Fts4 annotation to a given entity for very quick access to database information through full-text search (FTS)

- In cases where a table supports content in multiple languages, use the languageId


# Define relationships between objects
- we can use the @Embedded annotation to represent an object that you'd like to decompose into its subfields within a table. You can then query the embedded fields just as you would for other individual columns

- you can use the @Embedded annotation to represent an object that you'd like to decompose into its subfields within a table. You can then query the embedded fields just as you would for other individual columns.

## relationships
- one-to-one and one-to-many and many-to-many

 create a class for each of your two entities. One of the entities must include a variable that is a reference to the primary key of the other entity.

## model the one-to-one relationship between the two entities 
by create a new data class where each instance holds an instance of the parent entity and the corresponding instance of the child entity

- Add the @Relation annotation to the instance of the child entity, with parentColumn set to the name of the primary key column of the parent entity and entityColumn set to the name of the column of the child entity that references the parent entity's primary key

- add a method to the DAO class that returns all instances of the data class by add the @Transaction annotation to this method to ensure that the whole operation is performed atomically
## in many-to-many 
- model the relationship between the entities by using the associateBy property in the @Relation annotation in each of these classes to identify the cross-reference entity providing the relationship between classes

- add a method to the DAO class to expose the query functionality your app needs.

- nested relationships between the tables to query a set of three or more tables that are all related to each other

------------------------------------------------------

# Accessing data using Room DAOs
## Insert
allows you to define methods that insert their parameters into the appropriate table in the database

         @Insert(onConflict = OnConflictStrategy.REPLACE)
         public void insertUsers(User... users);
             @Insert
       public void insertBothUsers(User user1, User user2);
## Update
allows you to define methods that update specific rows in a database table

          @Update
        public void updateUsers(User... users);
## Delete
allows you to define methods that delete specific rows from a database table.

         @Delete
            public void deleteUsers(User... users);





Accessing data with Room
Accessing data using Room DAOs

- Data access objects(DOA) - Each DAO includes methods that offer abstract access to your app's database. At compile time, Room automatically generates implementations of the DAOs that you define.
- Can define each DAO as either an interface or an abstract class.
- Annotate your DAOs with @Dao
- Convenience methods - that let you insert, update, and delete rows in your database without writing any SQL code.
Query methods - that let you write your own SQL query to interact with the database.

- @Query annotation - allows you to write SQL statements and expose them as DAO methods.
- DAOs can return PagingSource objects for use with Paging 3.
- Can write your DAO methods to return a Cursor object.