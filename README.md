# LoginCRUDDB
Help me make this example cleaner code, more secure, and possibly done a better way.
To set this site working on a localhost environment, create two databases with one table in each one. Then records will be inserted into the tables. 

In simpler terms, setup your local environment by using XXAMP for Windows, LAMP for Linux, or MAMP for OSX. Once you are in PHPMyAdmin, input this SQL. Copy @ Paste

CRUD database

Step1

CREATE DATABASE IF NOT EXISTS `page_records` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `page_records`; CREATE TABLE `safety` (
  `id` int(11) NOT NULL,
  `ins_n` varchar(4) CHARACTER SET ascii NOT NULL,
  `explanation` text CHARACTER SET ascii NOT NULL,
  `date` date NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Step 2:

INSERT INTO `page_records`.`safety` (`id`, `ins_n`, `explanation`, `date`) VALUES
(1, '001A', 'Employee got injured.. test', '0000-00-00'),
(2, '002B', 'testing', '0000-00-00'),
(3, '003', 'test', '2014-01-28'),
(4, '101', 'Testing', '2016-02-22')


Database for Login/Logout:

Step 3

CREATE DATABASE IF NOT EXISTS `accounts` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
CREATE TABLE `users` (
  `id` int(11) NOT NULL,
  `username` varchar(10) CHARACTER SET ascii NOT NULL,
  `password` varchar(100) CHARACTER SET ascii NOT NULL,
  `active` tinyint(1) NOT NULL DEFAULT '0'
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

Step 4

INSERT INTO `accounts`.`users` (`id`, `username`, `password`, `active`) VALUES
(1, 'test', 'pw', 1);






From here, move all files to the localhost root folder. Depending on your setup the root folder by default is either www or htdocs. Make sure Apache and MySQL is running. Finally in the browser enter the URL localhost/logincrud/login/index.php. 

Username:test
Password:pw

HOW IT WORKS + QUESTIONS

I used MAMP on MAC OSX to make this example to:

1-	Login/Logoff using the same database as the CRUD records displayed after logging in. On same database, using a separate table.
2-	Using CRUD with the option of logging off.

I made this simple login to view records using PHP/HTML pages to connect to an SQL 	
 
Document Root PATHNAME is under logincrud

The example works, however, in order for the user to begin (or sign in) the localhost/login/index.php needs to be in the URL. Basically I made a CRUD PHP system work before the login/out feature. Does this issue come up?
 
Thinking about it I could swap the login/out task (or 
scope) into the main directory- in turn the CRUD PHP system task (or scope) will need to be placed in a subfolder (the login folder from the photo above.). 

The PHP files are over the place. What is the best way to keep PHP files, JavaScript, and CSS designated for the scope or task? Makes since to keep them separated by file type. MVC Model-View-Controller is all about JavaScript, am I correct?

For security purposes on my bout connecting to the database securely? I have read this and public suggested you make a initial file to connect to the database.

I would really like others to me this simple project in a better format-bring up better ideas to make this example perfect for the real world.

