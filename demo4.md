    # Demo4 / Persistent Volumes

    1.  Download the MySQL Database Image (mysql:5.7 or mahendrshinde/mysql-sample:employees)

        ```
        $ docker pull mahendrshinde/mysql-sample:employees
        ```

    2.  Create a new directory / folder `d:\db-vol` 
    3.  Right click on Docker desktop icon in system tray and choose option 'Settings'
    4.  Choose "Resources" > "File Sharing"  then use "+" button and add path "d:\db-vol"
    5.  Click "Apply & Restart"

    6.  You need following command to create and start new db container

        ```
        $ docker run --name db1 -d -p 33060:3306 
                -e MYSQL_USER=mahendra -e MYSQL_PASSWORD=pass12334 -e MYSQL_ROOT_PASSWORD=Pass@1234
                -v d:\db-vol:/var/lib/mysql:rw
                mahendrshinde/mysql-sample:employees
        ```

    7.  Using file explorer, visit d:\db-vol and check all the mysql database files.

    8.  Try deleting your database

        ```
        $ docker logs db1
        $ docker stop db1
        $ docker rm db1
        ```

    9.  Try revisiting d:\db-vol, all the files should be still there!

    10. Just repeate the command in step#6 and create new container db1

    11. Verify the logs and then stop and delete.

        ```
        $ docker logs db1
        $ docker stop db1
        $ docker rm db1
        ```
