# Debug containers using EXEC and stop and remove containers

1.  List all running container

    `$ docker ps `

2.  Get INSIDE container `c1`

    ```
    $ docker exec -it c1 bash
    $ curl http://172.17.0.3
    ```

3.  Using new command prompt get INSIDE container `c2`

    ```
    $ docker exec -it c2 bash
    $ curl http://172.17.0.2
    ```

4.  Stop both c1 and c2

    ```
    $ docker stop c1 c2
    $ docker rm c1 c2
    ```