
ReadMe

To set this site working on a localhost environment, create 2 new databases in PHPMyAdmin and input this SQL. Copy @ Paste

Login database
Step1
CREATE DATABASE `accounts` DEFAULT CHARACTER SET latin1 COLLATE latin1_swedish_ci; CREATE TABLE `accounts`.`users` ( `id` int( 11 ) NOT NULL , `username` varchar( 10 ) CHARACTER SET ascii NOT NULL , `password` varchar( 100 ) CHARACTER SET ascii NOT NULL , `active` tinyint( 1 ) NOT NULL DEFAULT '0' ) ENGINE = InnoDB DEFAULT CHARSET = latin1; ALTER TABLE `accounts`.`users` ADD PRIMARY KEY ( `id` ) ; ALTER TABLE `accounts`.`users` MODIFY `id` int( 11 ) NOT NULL AUTO_INCREMENT ; SET SQL_MODE='NO_AUTO_VALUE_ON_ZERO'; INSERT INTO `accounts`.`users` SELECT * FROM `accounts`.`users`;


Step 2
INSERT INTO `users` (`id`, `username`, `password`, `active`) VALUES
(1, 'test', 'pw', 1);




 Database for incidents:

Step 1:
CREATE DATABASE `accounts` DEFAULT CHARACTER SET latin1 COLLATE latin1_swedish_ci; CREATE TABLE `saftey` (
  `id` int(11) NOT NULL,
  `ins_n` varchar(4) CHARACTER SET ascii NOT NULL,
  `explanation` text CHARACTER SET ascii NOT NULL,
  `date` date NOT NULL
) ENGINE=InnoDB AUTO_INCREMENT=5 DEFAULT CHARSET=latin1;

Step 2:
INSERT INTO `saftey` (`id`, `ins_n`, `explanation`, `date`) VALUES
(1, '001A', 'Employee got injured.. test', '0000-00-00'),
(2, '002B', 'testing', '0000-00-00'),
(3, '003', 'test', '2014-01-28'),
(4, '101', 'Testing', '2016-02-22')


From here, move all files to the localhost root folder; run Apache and MySQL and it will work. 

Username:test
Password:pw

I am consistently learning languages in programming. Thank you

Todd Hartsfield


CREATE DATABASE `page_records` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci; CREATE TABLE `page_records`.`saftey` (
  `id` int(11) NOT NULL,
  `ins_n` varchar(4) CHARACTER SET ascii NOT NULL,
  `explanation` text CHARACTER SET ascii NOT NULL,
  `date` date NOT NULL
) ENGINE=InnoDB AUTO_INCREMENT=5 DEFAULT CHARSET=utf8;


