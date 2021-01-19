# Docker Run Daemon mode / Detached mode

1. Start the new container with Port forwarding on host port 8080 to guest port 80

    ```
    $ docker run -d -p 8080:80 --name c1 nginx:latest
    $ docker logs c1
    $ curl http://localhost:8080
    ## Incase curl gives an error 
    $ start http://localhost:8080
    $ docker logs c1
    ```

2.  Stop and Remove the container (-f is force delete)

    ```
    $ docker rm -f c1
    ```

