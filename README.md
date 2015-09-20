# MySQL Workshop 1 - Databases & Data Types


## Workshop Contents


### Common MySQL Data Types

* [INT](https://dev.mysql.com/doc/refman/5.7/en/integer-types.html)
* [BOOLEAN](https://dev.mysql.com/doc/refman/5.7/en/numeric-type-overview.html) aka TINYINT(1)
* [VARCHAR](https://dev.mysql.com/doc/refman/5.7/en/char.html)
* [DATETIME](https://dev.mysql.com/doc/refman/5.7/en/datetime.html)
* [ENUM](https://dev.mysql.com/doc/refman/5.7/en/enum.html)


### Connecting to MySQL

```
# Start MySQL Instance
$ mysql-ctl start

# Connect to the MySQL Instance
$ mysql -u<USERNAME> -p<PASSWORD>
```

### Database Statements

* [Show Databases](https://dev.mysql.com/doc/refman/5.7/en/show-databases.html)
* [Select Database](https://dev.mysql.com/doc/refman/5.7/en/use.html)
* [Show Tables](https://dev.mysql.com/doc/refman/5.7/en/show-tables.html)
* [Create Database](http://dev.mysql.com/doc/refman/5.7/en/create-database.html)
* [Drop Database](http://dev.mysql.com/doc/refman/5.7/en/drop-database.html)

### Table Statements

* [Create Table](http://dev.mysql.com/doc/refman/5.7/en/create-table.html)
* [Alter Table](http://dev.mysql.com/doc/refman/5.7/en/alter-table.html)
* [Truncate Table](http://dev.mysql.com/doc/refman/5.7/en/truncate-table.html)
* [Drop Table](http://dev.mysql.com/doc/refman/5.7/en/drop-table.html)
* [Describe Table](https://dev.mysql.com/doc/refman/5.7/en/show-columns.html)

## Workshop Instructions

* Create a new Cloud9 Workspace
* Fork this repository to your new Workspace

* For every exercise in this Workshop:
  * Create a new branch off from "master" named "exercise-n"
  * Create a new file named "exercise-n.txt", containing:
    * The SQL Query used, when applicable
    * The SQL Query results, when applicable
  * Create a pull request


### Exercise 1
* Connect to the MySQL instance within your Workspace using your Cloud9 username

### Exercise 2
* Create a database named ```decodemtl_test``` within MySQL
* Create a database named ```decodemtl_addressbook``` within MySQL

### Exercise 3
* Remove database named ```decodemtl_test``` from MySQL

### Exercise 4
* Return the list of databases within MySQL

### Exercise 5
* Create table ```Account``` for database ```decodemtl_addressbook```
* Create table ```AddressBook``` for database ```decodemtl_addressbook```
* Create table ```Entry``` for database ```decodemtl_addressbook```
* Create table ```Test``` for database ```decodemtl_addressbook```

### Exercise 6
* Remove table ```Test``` for database ```decodemtl_addressbook```

### Exercise 7
* Return list of tables within database ```decodemtl_addressbook```

### Exercise 8
* Reflect the data model shown in ```schema/addressbook_denormalized.png``` within database ```decodemtl_addressbook```
  * ```Account.id``` is a primary auto-increment key
  * ```AddressBook.id``` is a primary auto-increment key
  * ```Entry.id``` is a primary auto-increment key
  * ```Entry.type``` is an ENUM column permitting ```home```, ```work``` and ```other```
  * ```Entry.subtype``` is an ENUM column permitting ```phone```, ```address``` and ```email```

### Exercise 9

* Create a data model representing a Barn with Chickens :hatching_chick:
* This model should provide answers to the following questions:
  * How many rooster, hen and chicks existed in the Barn on a specific date
  * How many chicks will come to age on a specific date

### Exercise 10 (Workshop Challenge)

* Create a data model representing a Hotel with Floors and Rooms :hotel:
* This model should provide answers to the following questions:
  * The list of Rooms available for rent on a specific date
  * The list of Rooms which can be occupied by at least 3 people on a specific date
  * The amount of unrentable Rooms (janitor closets, public laundry room, gym, etc.)
  * The amount of Rooms having a private Kitchen
  * The average amount of windows per Floor
  * The amount of Floors having Rooms with carpets