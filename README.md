# Wordpress
An Ansible role for installing and configuring wordpress on CentOS/RHEL 7 by using WP-CLI.  
For more info about WP-CLI, visit http://wp-cli.org/.

After installing, you should be able to see your Wordpress application under the URL that you've specified and you can login as an admin user with the username and password of your choice.

## Requirements

None

## Role variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| `wordpress_database_address`| 'localhost' | The address of the database host |
| `wordpress_database` | 'wp_db' | The name of the database for Wordpress.           |
| `wordpress_user`     | 'wp_user' | The name of the database user.                    |
| `wordpress_password` | 'wppassword' | The password of the database user.                |
| `wordpress_home_url` | 'http://www.example.com' | The home url of the wordpress application.               |
| `wordpress_admin_user` | 'admin' | The admin user of the wordpress application.               |
| `wordpress_admin_user_pass` | 'admin' | The admin user's password.              |
| `wordpress_admin_email` | 'toon.lamberigts@gmail.com' | The email address of the admin user.               |
| `wordpress_dir` | '/usr/share/wordpress' | The home directory of the wordpress application.              |
| `wordpress_site_title` | 'Test Site' | The title of your wordpress application |

## Dependencies

This role requires a database server (local or remote) such as MariaDB to store the Wordpress data.  
The database service must have a user and password for Worpress which is exactly the same as defined in the variables of this role.  

This role also requires an Apache webservice to be running.  

## Defining your database host

This role allows you to easily configure the host of your database storing the Wordpress data.  
You can choose to use either a local or remote database by specifying your database's address as shown in this example:  
```Yaml
wordpress_database_address: yourdatabaselocation
```

## License

MIT

