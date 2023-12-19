# Project Configuration

1. Clone the project using `git clone`.

2. Ensure that Apache 2.4 and PHP 8.2 (or another version) are installed on your PC.

3. Create a `.conf` file, for example:

    ```bash
    sudo nano /etc/httpd/conf.d/mvc.conf
    ```

4. In the `.conf` file, configure it as follows:

    ```apache
    <VirtualHost *:80>
        ServerName laminas-mvc-tutorial.localhost
        DocumentRoot /path/to/yourproject/public
        SetEnv APPLICATION_ENV "development"
        <Directory /path/to/laminas-mvc-tutorial/public>
            DirectoryIndex index.php
            AllowOverride All
            Require all granted
        </Directory>
    </VirtualHost>
    ```

   Replace `/path/to/yourproject` with the actual path to your project.

5. Open your hosts file, typically located at `/etc/hosts` on Unix-based systems:

    ```bash
    sudo nano /etc/hosts
    ```

6. Add the following line:

    ```plaintext
    127.0.0.1 thenamethatyouwant.localhost
    ```

7. Check if it's accessible by accessing the specified host, and have fun!
