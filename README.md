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
	mysql -u"AzureDiamond" -p"hunter2" -h"localhost" some_db

