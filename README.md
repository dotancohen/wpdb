# wpdb

Search the Wordpress hierarchy for the config file, and return the MySQL connection string if found. Parses the following WP definitions:

* DB_USER (required)
* DB_USER (required)
* DB_HOST (optional)
* DB_NAME (optional)

Finds the wp-config.php file from any directory in the Wordpress hierarchy:

	$ pwd
	/var/www/wordpress/public_html/wp-content/themes

	$ wpdb
	mysql -h'localhost' -u'AzureDiamond' -p'hunter2' some_db

	$

Supports optionally connecting to MySQL directly:

	$ wpdb -c
	Welcome to the MySQL monitor.  Commands end with ; or \g.
	mysql> SELECT COUNT(*) FROM wp_posts;
	+----------+
	| COUNT(*) |
	+----------+
	|      351 |
	+----------+
	1 row in set (0.01 sec)

Supports returning a mysqldump string, complete with suggested time-based filename:

	$ wpdb -d
	mysqldump -h'localhost' -u'AzureDiamond' -p'hunter2' some_db --skip-opt > some_db_2016-02-10_1602.sql

	$

